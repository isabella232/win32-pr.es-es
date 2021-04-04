---
title: Cómo agregar efectos de dibujo de cliente a un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente a una aplicación de DirectWrite que muestra texto mediante la interfaz IDWriteTextLayout y un representador de texto personalizado.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078007"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="60901-103">Cómo agregar efectos de dibujo de cliente a un diseño de texto</span><span class="sxs-lookup"><span data-stu-id="60901-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="60901-104">Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente a una aplicación de [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y un representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="60901-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="60901-105">El producto final de este tutorial es una aplicación que muestra texto con intervalos de texto con un efecto de dibujo de color diferente en cada, tal como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="60901-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![captura de pantalla de "ejemplo de efecto de dibujo de cliente"](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="60901-108">Este tutorial pretende ser un ejemplo simplificado de cómo crear efectos de dibujo de cliente personalizados, no un ejemplo de un método simple para dibujar texto de color.</span><span class="sxs-lookup"><span data-stu-id="60901-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="60901-109">Vea la página de referencia [**IDWriteTextLayout:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="60901-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="60901-110">Este tutorial contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="60901-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="60901-111">Paso 1: crear un diseño de texto</span><span class="sxs-lookup"><span data-stu-id="60901-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="60901-112">Paso 2: implementar una clase de efecto de dibujo personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="60901-113">Paso 3: implementación de una clase de representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="60901-114">Constructor</span><span class="sxs-lookup"><span data-stu-id="60901-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="60901-115">El método DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="60901-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="60901-116">El destructor</span><span class="sxs-lookup"><span data-stu-id="60901-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="60901-117">Paso 4: crear el representador de texto</span><span class="sxs-lookup"><span data-stu-id="60901-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="60901-118">Paso 5: crear una instancia de los objetos de efecto de dibujo de color</span><span class="sxs-lookup"><span data-stu-id="60901-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="60901-119">Paso 6: establecer el efecto de dibujo para intervalos de texto específicos</span><span class="sxs-lookup"><span data-stu-id="60901-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="60901-120">Paso 7: dibujo del diseño de texto con el representador personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="60901-121">Paso 8: limpieza</span><span class="sxs-lookup"><span data-stu-id="60901-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="60901-122">Paso 1: crear un diseño de texto</span><span class="sxs-lookup"><span data-stu-id="60901-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="60901-123">Para empezar, necesitará una aplicación con un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="60901-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="60901-124">Si ya tiene una aplicación que muestra texto con un diseño de texto, o si está usando el código de ejemplo DrawingEffect personalizado, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="60901-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="60901-125">Para agregar un diseño de texto, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="60901-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="60901-126">Declare un puntero a una interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase.</span><span class="sxs-lookup"><span data-stu-id="60901-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="60901-127">Al final del método **CreateDeviceIndependentResources** , cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="60901-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  <span data-ttu-id="60901-128">Por último, recuerde liberar el diseño de texto en el destructor.</span><span class="sxs-lookup"><span data-stu-id="60901-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="60901-129">Paso 2: implementar una clase de efecto de dibujo personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="60901-130">Aparte de los métodos heredados de IUnknown, una interfaz de efecto de dibujo de cliente personalizado no tiene ningún requisito en lo que se debe implementar.</span><span class="sxs-lookup"><span data-stu-id="60901-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="60901-131">En este caso, la clase **ColorDrawingEffect** simplemente contiene un valor de [**D2D1 \_ color \_ F**](../direct2d/d2d1-color-f.md) y declara métodos para obtener y establecer este valor, así como un constructor que puede establecer el color inicialmente.</span><span class="sxs-lookup"><span data-stu-id="60901-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="60901-132">Una vez que se aplica un efecto de dibujo de cliente a un intervalo de texto en un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , el efecto de dibujo se pasa al método [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de cualquier ejecución de glifo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="60901-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="60901-133">Los métodos del efecto de dibujo están disponibles para el representador de texto.</span><span class="sxs-lookup"><span data-stu-id="60901-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="60901-134">Un efecto de dibujo de cliente puede ser tan complejo como desee hacer, con más información que en este ejemplo, así como proporcionar métodos para modificar glifos, crear objetos que se van a usar para dibujar, etc.</span><span class="sxs-lookup"><span data-stu-id="60901-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="60901-135">Paso 3: implementación de una clase de representador de texto personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="60901-136">Para poder aprovechar el efecto de dibujo de un cliente, debe implementar un representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="60901-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="60901-137">Este representador de texto aplicará el efecto de dibujo que le ha pasado el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) a la ejecución del glifo que se está dibujando.</span><span class="sxs-lookup"><span data-stu-id="60901-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="60901-138">Constructor</span><span class="sxs-lookup"><span data-stu-id="60901-138">The Constructor</span></span>

<span data-ttu-id="60901-139">El constructor del representador de texto personalizado almacena el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se usará para crear objetos de [direct2d](../direct2d/direct2d-portal.md) y el destino de representación de direct2d en el que se dibujará el texto.</span><span class="sxs-lookup"><span data-stu-id="60901-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="60901-140">El método DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="60901-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="60901-141">Una ejecución de glifo es un conjunto de glifos que comparten el mismo formato, incluido el efecto de dibujo del cliente.</span><span class="sxs-lookup"><span data-stu-id="60901-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="60901-142">El método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) se encarga de la representación de texto para una ejecución de glifos especificada.</span><span class="sxs-lookup"><span data-stu-id="60901-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="60901-143">En primer lugar, cree un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)y, a continuación, recupere el esquema de ejecución del glifo mediante [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span><span class="sxs-lookup"><span data-stu-id="60901-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="60901-144">A continuación, transforme el origen de la geometría mediante el método [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="60901-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



<span data-ttu-id="60901-145">A continuación, declare un objeto de pincel sólido de [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="60901-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="60901-146">Si el parámetro *clientDrawingEffect* no es null, consulte el objeto para la interfaz **ColorDrawingEffect** .</span><span class="sxs-lookup"><span data-stu-id="60901-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="60901-147">Esto funcionará porque se establecerá esta clase como el efecto de dibujo del cliente en los intervalos de texto del objeto de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="60901-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="60901-148">Una vez que tenga un puntero a la interfaz **ColorDrawingEffect** , puede recuperar el [**valor \_ \_ F de color D2D1**](../direct2d/d2d1-color-f.md) que almacena con el método **GetColor** .</span><span class="sxs-lookup"><span data-stu-id="60901-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="60901-149">A continuación, use **el \_ color \_ F de D2D1** para crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) en ese color.</span><span class="sxs-lookup"><span data-stu-id="60901-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="60901-150">Si el parámetro *clientDrawingEffect* es **null**, basta con crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)negro.</span><span class="sxs-lookup"><span data-stu-id="60901-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



<span data-ttu-id="60901-151">Por último, dibuje la geometría del contorno y rellénelo con el pincel de color sólido que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="60901-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a><span data-ttu-id="60901-152">El destructor</span><span class="sxs-lookup"><span data-stu-id="60901-152">The Destructor</span></span>

<span data-ttu-id="60901-153">No olvide liberar el destino de representación y el generador de [Direct2D](../direct2d/direct2d-portal.md) en el destructor.</span><span class="sxs-lookup"><span data-stu-id="60901-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="60901-154">Paso 4: crear el representador de texto</span><span class="sxs-lookup"><span data-stu-id="60901-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="60901-155">En los recursos de **CreateDeviceDependent** , cree el objeto de representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="60901-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="60901-156">Depende del dispositivo porque usa **ID2D1RenderTarget**, que depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60901-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="60901-157">Paso 5: crear una instancia de los objetos de efecto de dibujo de color</span><span class="sxs-lookup"><span data-stu-id="60901-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="60901-158">Cree instancias de objetos **ColorDrawingEffect** en rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="60901-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="60901-159">Paso 6: establecer el efecto de dibujo para intervalos de texto específicos</span><span class="sxs-lookup"><span data-stu-id="60901-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="60901-160">Establezca el efecto de dibujo para intervalos de texto específicos mediante el método [**IDWriteTextLayou:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) y un struct de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .</span><span class="sxs-lookup"><span data-stu-id="60901-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="60901-161">Paso 7: dibujo del diseño de texto con el representador personalizado</span><span class="sxs-lookup"><span data-stu-id="60901-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="60901-162">Debe llamar al método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) en lugar de a los métodos [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) o [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="60901-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="60901-163">Paso 8: limpieza</span><span class="sxs-lookup"><span data-stu-id="60901-163">Step 8: Clean up</span></span>

<span data-ttu-id="60901-164">En el destructor DemoApp, libere el representador de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="60901-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="60901-165">Después de eso, agregue código para liberar las clases de efecto de dibujo del cliente.</span><span class="sxs-lookup"><span data-stu-id="60901-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 