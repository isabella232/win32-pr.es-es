---
title: Cómo agregar objetos alineados a un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar objetos insertados a una aplicación de DirectWrite que muestra texto mediante la interfaz IDWriteTextLayout.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568487"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="5b91d-103">Cómo agregar objetos alineados a un diseño de texto</span><span class="sxs-lookup"><span data-stu-id="5b91d-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="5b91d-104">Proporciona un breve tutorial sobre cómo agregar objetos insertados a una aplicación de [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5b91d-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="5b91d-105">El producto final de este tutorial es una aplicación que muestra texto con una imagen insertada incrustada, tal como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5b91d-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![captura de pantalla de "ejemplo de objeto en línea" con una imagen incrustada](images/inlineobject.png)

<span data-ttu-id="5b91d-107">Este tutorial contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="5b91d-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="5b91d-108">Paso 1: crear un diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="5b91d-109">Paso 2: definir una clase derivada de la interfaz IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="5b91d-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="5b91d-110">Paso 3: implementar la clase de objeto insertado.</span><span class="sxs-lookup"><span data-stu-id="5b91d-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="5b91d-111">Constructor.</span><span class="sxs-lookup"><span data-stu-id="5b91d-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="5b91d-112">Método draw.</span><span class="sxs-lookup"><span data-stu-id="5b91d-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="5b91d-113">El método GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="5b91d-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="5b91d-114">El método GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="5b91d-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="5b91d-115">El método GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="5b91d-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="5b91d-116">Paso 4: cree una instancia de la clase InlineImage y agréguela al diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="5b91d-117">Paso 1: crear un diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="5b91d-118">Para empezar, necesitará una aplicación con un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5b91d-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="5b91d-119">Si ya tiene una aplicación que muestra texto con un diseño de texto, vaya al paso 2.</span><span class="sxs-lookup"><span data-stu-id="5b91d-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="5b91d-120">Para agregar un diseño de texto, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b91d-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="5b91d-121">Declare un puntero a una interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase.</span><span class="sxs-lookup"><span data-stu-id="5b91d-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="5b91d-122">Al final del método CreateDeviceIndependentResources, cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="5b91d-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="5b91d-123">A continuación, debe cambiar la llamada al método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) a [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5b91d-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="5b91d-124">Paso 2: definir una clase derivada de la interfaz IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="5b91d-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="5b91d-125">La interfaz [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) proporciona compatibilidad con los objetos insertados en [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5b91d-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="5b91d-126">Para usar objetos alineados, debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="5b91d-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="5b91d-127">Controla el dibujo del objeto insertado, así como proporcionar métricas y otra información al representador.</span><span class="sxs-lookup"><span data-stu-id="5b91d-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="5b91d-128">Cree un nuevo archivo de encabezado y declare una interfaz denominada InlineImage, derivada de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span><span class="sxs-lookup"><span data-stu-id="5b91d-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="5b91d-129">Además de QueryInterface, AddRef y Release heredados de IUnknown, esta clase debe tener los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="5b91d-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="5b91d-130">**Dibujar**</span><span class="sxs-lookup"><span data-stu-id="5b91d-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="5b91d-131">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="5b91d-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="5b91d-132">**GetOverhangMetrics**</span><span class="sxs-lookup"><span data-stu-id="5b91d-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="5b91d-133">**GetBreakConditions**</span><span class="sxs-lookup"><span data-stu-id="5b91d-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="5b91d-134">Paso 3: implementar la clase de objeto insertado.</span><span class="sxs-lookup"><span data-stu-id="5b91d-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="5b91d-135">Cree un nuevo archivo de C++, denominado InlineImage. cpp, para la implementación de la clase.</span><span class="sxs-lookup"><span data-stu-id="5b91d-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="5b91d-136">Además del método LoadBitmapFromFile y los métodos heredados de la interfaz IUnknown, la clase InlineImage se compone de los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="5b91d-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="5b91d-137">Constructor.</span><span class="sxs-lookup"><span data-stu-id="5b91d-137">The Constructor.</span></span>


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



<span data-ttu-id="5b91d-138">El primer argumento del constructor es el ID2D1RenderTarget en el que se representará la imagen insertada.</span><span class="sxs-lookup"><span data-stu-id="5b91d-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="5b91d-139">Se almacena para su uso posterior al dibujar.</span><span class="sxs-lookup"><span data-stu-id="5b91d-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="5b91d-140">El destino de representación, IWICImagingFactory y el identificador URI del nombre de archivo se pasan al método LoadBitmapFromFile que carga el mapa de bits y almacena el tamaño del mapa de bits (ancho y alto) en la \_ variable miembro de Rect.</span><span class="sxs-lookup"><span data-stu-id="5b91d-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="5b91d-141">Método draw.</span><span class="sxs-lookup"><span data-stu-id="5b91d-141">The Draw Method.</span></span>

<span data-ttu-id="5b91d-142">El método [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) es una devolución de llamada a la que llama el objeto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) cuando es necesario dibujar el objeto insertado.</span><span class="sxs-lookup"><span data-stu-id="5b91d-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="5b91d-143">El diseño de texto no llama directamente a este método.</span><span class="sxs-lookup"><span data-stu-id="5b91d-143">The text layout does not call this method directly.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



<span data-ttu-id="5b91d-144">En este caso, el dibujo del mapa de bits se realiza mediante el método [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) . sin embargo, se puede usar cualquier método de dibujo.</span><span class="sxs-lookup"><span data-stu-id="5b91d-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="5b91d-145">El método GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="5b91d-145">The GetMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



<span data-ttu-id="5b91d-146">En el caso del método [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , almacene el ancho, el alto y la línea base en una estructura de [**\_ \_ \_ métricas de objeto en línea DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="5b91d-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="5b91d-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llama a esta función de devolución de llamada para obtener la medición del objeto insertado.</span><span class="sxs-lookup"><span data-stu-id="5b91d-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="5b91d-148">El método GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="5b91d-148">The GetOverhangMetrics Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



<span data-ttu-id="5b91d-149">En este caso, no es necesario sobresalir, por lo que el método [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) devuelve todos los ceros.</span><span class="sxs-lookup"><span data-stu-id="5b91d-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="5b91d-150">El método GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="5b91d-150">The GetBreakConditions Method.</span></span>


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="5b91d-151">Paso 4: cree una instancia de la clase InlineImage y agréguela al diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="5b91d-152">Por último, en el método CreateDeviceDependentResources, cree una instancia de la clase InlineImage y agréguela al diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="5b91d-153">Dado que contiene una referencia a [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que es un recurso dependiente del dispositivo, y el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) se crea mediante el destino de representación, el InlineImage también es dependiente del dispositivo y debe volver a crearse si se vuelve a crear el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="5b91d-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="5b91d-154">El método [**IDWriteTextLayout:: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) toma una estructura de intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="5b91d-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="5b91d-155">El objeto se aplica al intervalo especificado aquí y se suprimirá cualquier texto del intervalo.</span><span class="sxs-lookup"><span data-stu-id="5b91d-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="5b91d-156">Si la longitud del intervalo de texto es 0, el objeto no se dibujará.</span><span class="sxs-lookup"><span data-stu-id="5b91d-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="5b91d-157">En este ejemplo, hay un asterisco ( \* ) como marcador de posición en la posición donde se mostrará la imagen.</span><span class="sxs-lookup"><span data-stu-id="5b91d-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="5b91d-158">Dado que la clase InlineImage depende de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), debe liberarla al liberar el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="5b91d-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 