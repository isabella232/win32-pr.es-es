---
title: Representación mediante un representador de texto personalizado
description: Un representador de texto personalizado derivado de IDWriteTextRenderer puede dibujar un diseño de texto de DirectWrite \ 160;.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420998"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="520fd-103">Representación mediante un representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="520fd-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="520fd-104">Un representador de texto personalizado derivado de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)puede dibujar un  [**diseño de texto**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) de [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="520fd-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="520fd-105">Se requiere un representador personalizado para aprovechar algunas características avanzadas de DirectWrite, como la representación en un mapa de bits o una superficie de GDI, objetos insertados y efectos de dibujo de cliente.</span><span class="sxs-lookup"><span data-stu-id="520fd-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="520fd-106">En este tutorial se describen los métodos de **IDWriteTextRenderer** y se proporciona una implementación de ejemplo que usa [Direct2D](../direct2d/direct2d-portal.md) para representar texto con un relleno de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="520fd-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="520fd-107">Este tutorial contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="520fd-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="520fd-108">Constructor</span><span class="sxs-lookup"><span data-stu-id="520fd-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="520fd-109">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="520fd-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="520fd-110">DrawUnderline () y DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="520fd-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="520fd-111">Ajuste de píxeles, píxeles por DIP y transformación</span><span class="sxs-lookup"><span data-stu-id="520fd-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="520fd-112">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="520fd-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="520fd-113">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="520fd-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="520fd-114">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="520fd-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="520fd-115">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="520fd-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="520fd-116">El destructor</span><span class="sxs-lookup"><span data-stu-id="520fd-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="520fd-117">Usar el representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="520fd-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="520fd-118">El representador de texto personalizado debe implementar los métodos heredados de IUnknown además de los métodos enumerados en la página de referencia de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) y a continuación.</span><span class="sxs-lookup"><span data-stu-id="520fd-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="520fd-119">Para ver el código fuente completo del representador de texto personalizado, consulte los archivos CustomTextRenderer. cpp y CustomTextRenderer. h del [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="520fd-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="520fd-120">Constructor</span><span class="sxs-lookup"><span data-stu-id="520fd-120">The Constructor</span></span>

<span data-ttu-id="520fd-121">El representador de texto personalizado necesitará un constructor.</span><span class="sxs-lookup"><span data-stu-id="520fd-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="520fd-122">En este ejemplo se usan pinceles sólidos y de mapa de bits [Direct2D](../direct2d/direct2d-portal.md) para representar el texto.</span><span class="sxs-lookup"><span data-stu-id="520fd-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="520fd-123">Por este motivo, el constructor toma los parámetros que se encuentran en la tabla siguiente con descripciones.</span><span class="sxs-lookup"><span data-stu-id="520fd-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="520fd-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="520fd-124">Parameter</span></span>       | <span data-ttu-id="520fd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="520fd-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520fd-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="520fd-126">*pD2DFactory*</span></span>   | <span data-ttu-id="520fd-127">Un puntero a un objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se usará para crear los recursos de Direct2D necesarios.</span><span class="sxs-lookup"><span data-stu-id="520fd-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="520fd-128">*pRT*</span><span class="sxs-lookup"><span data-stu-id="520fd-128">*pRT*</span></span>           | <span data-ttu-id="520fd-129">Un puntero al objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) en el que se representará el texto.</span><span class="sxs-lookup"><span data-stu-id="520fd-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="520fd-130">*pOutlineBrush*</span><span class="sxs-lookup"><span data-stu-id="520fd-130">*pOutlineBrush*</span></span> | <span data-ttu-id="520fd-131">Un puntero a la [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) que se usará para dibujar el contorno del texto.</span><span class="sxs-lookup"><span data-stu-id="520fd-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="520fd-132">*pFillBrush*</span><span class="sxs-lookup"><span data-stu-id="520fd-132">*pFillBrush*</span></span>    | <span data-ttu-id="520fd-133">Un puntero a la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que se usará para rellenar el texto.</span><span class="sxs-lookup"><span data-stu-id="520fd-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="520fd-134">Estos se almacenarán en el constructor tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="520fd-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="520fd-135">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="520fd-135">DrawGlyphRun()</span></span>

<span data-ttu-id="520fd-136">El método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) es el método de devolución de llamada principal del representador de texto.</span><span class="sxs-lookup"><span data-stu-id="520fd-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="520fd-137">Se pasa una ejecución de glifos que se va a representar además de información como el origen de la línea base y el modo de medición.</span><span class="sxs-lookup"><span data-stu-id="520fd-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="520fd-138">También pasa un objeto de efecto de dibujo de cliente que se va a aplicar a la ejecución del glifo.</span><span class="sxs-lookup"><span data-stu-id="520fd-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="520fd-139">Para obtener más información, vea el tema [Cómo agregar efectos de dibujo de cliente a un diseño de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="520fd-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="520fd-140">Esta implementación de representación de texto representa ejecuciones de glifos convirtiéndolos en geometrías de [Direct2D](rendering-by-using-direct2d.md) y, a continuación, dibujando y rellenando las geometrías.</span><span class="sxs-lookup"><span data-stu-id="520fd-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="520fd-141">Este proceso consta de los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="520fd-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="520fd-142">Cree un objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y, a continuación, recupere el objeto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) mediante el método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="520fd-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="520fd-143">La [**\_ \_ ejecución del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que se pasa a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contiene un objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominado *fontFace*, que representa el tipo de fuente para toda la ejecución del glifo.</span><span class="sxs-lookup"><span data-stu-id="520fd-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="520fd-144">Coloque el contorno de la ejecución del glifo en el receptor de geometría mediante el método [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="520fd-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="520fd-145">Después de rellenar el receptor de geometría, ciérrelo.</span><span class="sxs-lookup"><span data-stu-id="520fd-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="520fd-146">El origen de la ejecución del glifo se debe traducir para que se represente desde el origen de base de referencia correcto, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="520fd-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="520fd-147">*BaselineOriginX* y *baselineOriginY* se pasan como parámetros al método de devolución de llamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="520fd-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="520fd-148">Cree la geometría transformada mediante el método [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) y pase la geometría de trazado y la matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="520fd-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="520fd-149">Por último, dibuje el contorno de la geometría transformada y rellénelo mediante los métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) y los pinceles de [Direct2D](../direct2d/direct2d-portal.md) almacenados como variables de miembro.</span><span class="sxs-lookup"><span data-stu-id="520fd-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="520fd-150">Ahora que ha terminado de dibujar, no olvide limpiar los objetos que se crearon en este método.</span><span class="sxs-lookup"><span data-stu-id="520fd-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="520fd-151">DrawUnderline () y DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="520fd-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="520fd-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) también tiene devoluciones de llamada para dibujar el subrayado y el tachado.</span><span class="sxs-lookup"><span data-stu-id="520fd-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="520fd-153">En este ejemplo se dibuja un rectángulo sencillo para un subrayado o tachado, pero se pueden dibujar otras formas.</span><span class="sxs-lookup"><span data-stu-id="520fd-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="520fd-154">Dibujar un subrayado mediante [Direct2D](../direct2d/direct2d-portal.md) consta de los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="520fd-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="520fd-155">En primer lugar, cree una estructura [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) del tamaño y la forma del subrayado.</span><span class="sxs-lookup"><span data-stu-id="520fd-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="520fd-156">La estructura de [**\_ subrayado DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) que se pasa al método de devolución de llamada [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) proporciona el desplazamiento, el ancho y el grosor del subrayado.</span><span class="sxs-lookup"><span data-stu-id="520fd-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="520fd-157">A continuación, cree un objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) mediante el método [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) y la estructura [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) inicializada.</span><span class="sxs-lookup"><span data-stu-id="520fd-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="520fd-158">Al igual que con la ejecución del glifo, el origen de la geometría de subrayado se debe traducir, en función de los valores de origen de la línea base, mediante el método [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="520fd-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="520fd-159">Por último, dibuje el contorno de la geometría transformada y rellénelo mediante los métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) y los pinceles de [Direct2D](../direct2d/direct2d-portal.md) almacenados como variables de miembro.</span><span class="sxs-lookup"><span data-stu-id="520fd-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="520fd-160">Ahora que ha terminado de dibujar, no olvide limpiar los objetos que se crearon en este método.</span><span class="sxs-lookup"><span data-stu-id="520fd-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="520fd-161">El proceso para dibujar un tachado es el mismo.</span><span class="sxs-lookup"><span data-stu-id="520fd-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="520fd-162">Sin embargo, el tachado tendrá un desplazamiento diferente y probablemente un ancho y un grosor distintos.</span><span class="sxs-lookup"><span data-stu-id="520fd-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="520fd-163">Ajuste de píxeles, píxeles por DIP y transformación</span><span class="sxs-lookup"><span data-stu-id="520fd-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="520fd-164">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="520fd-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="520fd-165">Se llama a este método para determinar si está deshabilitado el ajuste de píxeles.</span><span class="sxs-lookup"><span data-stu-id="520fd-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="520fd-166">El valor predeterminado recomendado es **false** y es el resultado de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="520fd-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="520fd-167">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="520fd-167">GetCurrentTransform()</span></span>

<span data-ttu-id="520fd-168">Este ejemplo se representa en un destino de representación de Direct2D, por lo que reenvía la transformación del destino de representación mediante [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span><span class="sxs-lookup"><span data-stu-id="520fd-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="520fd-169">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="520fd-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="520fd-170">Se llama a este método para obtener el número de píxeles por píxel independiente del dispositivo (DIP).</span><span class="sxs-lookup"><span data-stu-id="520fd-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="520fd-171">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="520fd-171">DrawInlineObject()</span></span>

<span data-ttu-id="520fd-172">Un representador de texto personalizado también tiene una devolución de llamada para dibujar objetos insertados.</span><span class="sxs-lookup"><span data-stu-id="520fd-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="520fd-173">En este ejemplo, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="520fd-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="520fd-174">Una explicación de cómo se dibujan los objetos insertados queda fuera del ámbito de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="520fd-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="520fd-175">Para obtener más información, vea el tema [Cómo agregar objetos insertados en un diseño de texto](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="520fd-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="520fd-176">El destructor</span><span class="sxs-lookup"><span data-stu-id="520fd-176">The Destructor</span></span>

<span data-ttu-id="520fd-177">Es importante liberar los punteros usados por la clase de representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="520fd-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="520fd-178">Usar el representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="520fd-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="520fd-179">Se representa con el representador personalizado mediante el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que toma una interfaz de devolución de llamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como argumento, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="520fd-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="520fd-180">El método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) llama a los métodos de la devolución de llamada del representador personalizado que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="520fd-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="520fd-181">Los métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritos anteriormente realizan las funciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="520fd-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 