---
title: Representación de DirectWrite
description: Representación de DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421023"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="d9464-103">Representación de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9464-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="d9464-104">Opciones de representación</span><span class="sxs-lookup"><span data-stu-id="d9464-104">Rendering Options</span></span>

<span data-ttu-id="d9464-105">El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D](../direct2d/direct2d-portal.md); sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="d9464-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="d9464-106">La cadena descrita por un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d9464-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="d9464-107">1. representar mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="d9464-107">1. Render using Direct2D</span></span>

<span data-ttu-id="d9464-108">Para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante Direct2D, use el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="d9464-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="d9464-109">Para obtener más información detallada sobre cómo dibujar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante [Direct2D](../direct2d/direct2d-portal.md), consulte [Introducción con DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="d9464-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="d9464-110">2. representar mediante un representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="d9464-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="d9464-111">Se representa con un representador personalizado mediante el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que toma una interfaz de devolución de llamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como argumento, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="d9464-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="d9464-112">El método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) llama a los métodos de la devolución de llamada del representador personalizado que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="d9464-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="d9464-113">Los métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) realizan las funciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="d9464-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="d9464-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declara métodos para dibujar una ejecución de glifos, subrayado, tachado y objetos insertados.</span><span class="sxs-lookup"><span data-stu-id="d9464-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="d9464-115">Depende de la aplicación implementar estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d9464-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="d9464-116">La creación de un representador de texto personalizado permite a la aplicación aplicar efectos adicionales al representar texto, como un relleno o un contorno personalizados.</span><span class="sxs-lookup"><span data-stu-id="d9464-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="d9464-117">En el [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)se incluye un representador de texto personalizado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9464-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="d9464-118">3. representar ClearType en una superficie de GDI.</span><span class="sxs-lookup"><span data-stu-id="d9464-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="d9464-119">La representación en una superficie de GDI es, en realidad, un ejemplo del uso de un representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="d9464-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="d9464-120">Sin embargo, parte del trabajo se realiza en forma de la interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="d9464-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="d9464-121">Para crear esta interfaz, use el método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="d9464-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="d9464-122">El método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) del representador de texto personalizado llama al método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar los glifos.</span><span class="sxs-lookup"><span data-stu-id="d9464-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="d9464-123">El representador personalizado debe realizar la representación de los objetos de subrayado, tachado e insertado.</span><span class="sxs-lookup"><span data-stu-id="d9464-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="d9464-124">La interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) se representa en un contexto de dispositivo (DC) en memoria.</span><span class="sxs-lookup"><span data-stu-id="d9464-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="d9464-125">Obtiene un identificador de este controlador de dominio mediante el método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="d9464-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="d9464-126">Una vez realizado el dibujo, el controlador de dominio de memoria del objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) debe copiarse en la superficie GDI de destino.</span><span class="sxs-lookup"><span data-stu-id="d9464-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="d9464-127">También tiene la opción de transferir el mapa de bits a otro tipo de superficie, como una superficie de GDI+.</span><span class="sxs-lookup"><span data-stu-id="d9464-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



> [!Note]  
> <span data-ttu-id="d9464-128">La aplicación tiene la responsabilidad de representar todo en la ventana al final.</span><span class="sxs-lookup"><span data-stu-id="d9464-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="d9464-129">Esto incluye texto y gráficos.</span><span class="sxs-lookup"><span data-stu-id="d9464-129">This includes text and graphics.</span></span> <span data-ttu-id="d9464-130">Esto tiene una penalización del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d9464-130">There is a performance penalty to this.</span></span> <span data-ttu-id="d9464-131">Además, la representación en un controlador de dominio de memoria no es una aceleración del hardware de GDI.</span><span class="sxs-lookup"><span data-stu-id="d9464-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="d9464-132">Para obtener información general más detallada sobre la interoperabilidad con GDI, vea [interoperar con GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="d9464-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="d9464-133">4. representar el texto de escala de grises de forma transparente en una superficie de GDI.</span><span class="sxs-lookup"><span data-stu-id="d9464-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="d9464-134">(Windows 8 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="d9464-134">(Windows 8 and later)</span></span>

<span data-ttu-id="d9464-135">A partir de Windows 8, puede representar texto de escala de grises de forma transparente en una superficie de GDI para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d9464-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="d9464-136">Para ello, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9464-136">To do this you need to:</span></span>

1.  <span data-ttu-id="d9464-137">Borre el DC de memoria para que sea transparente.</span><span class="sxs-lookup"><span data-stu-id="d9464-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="d9464-138">Representar texto en la memoria HDC usando antialiasing de escala de grises (modo de SUAVIZAdo de contorno de \_ texto DWRITE \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="d9464-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="d9464-139">Use la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) para representar la memoria HDC de forma transparente sobre la HDC de destino final.</span><span class="sxs-lookup"><span data-stu-id="d9464-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="d9464-140">Repita tantas veces como sea necesario (por ejemplo, una vez por ejecución del glifo) y entre otros gráficos se puede representar directamente en el destino HDC de destino sin sobrescribirlo con la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="d9464-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="d9464-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9464-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9464-142">Representar mediante Direct2D</span><span class="sxs-lookup"><span data-stu-id="d9464-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="d9464-143">Representación mediante un representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="d9464-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="d9464-144">Representar en una superficie de GDI</span><span class="sxs-lookup"><span data-stu-id="d9464-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="d9464-145">Interoperar con GDI</span><span class="sxs-lookup"><span data-stu-id="d9464-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 