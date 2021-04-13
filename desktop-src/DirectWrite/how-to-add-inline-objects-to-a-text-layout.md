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
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Cómo agregar objetos alineados a un diseño de texto

Proporciona un breve tutorial sobre cómo agregar objetos insertados a una aplicación de [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

El producto final de este tutorial es una aplicación que muestra texto con una imagen insertada incrustada, tal como se muestra en la siguiente captura de pantalla.

![captura de pantalla de "ejemplo de objeto en línea" con una imagen incrustada](images/inlineobject.png)

Este tutorial contiene las siguientes partes:

-   [Paso 1: crear un diseño de texto.](#step-1-create-a-text-layout)
-   [Paso 2: definir una clase derivada de la interfaz IDWriteInlineObject.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Paso 3: implementar la clase de objeto insertado.](#step-3-implement-the-inline-object-class)
    -   [Constructor.](#the-constructor)
    -   [Método draw.](#the-draw-method)
    -   [El método GetMetrics.](#the-getmetrics-method)
    -   [El método GetOverhangMetrics.](#the-getoverhangmetrics-method)
    -   [El método GetBreakConditions.](#the-getbreakconditions-method)
-   [Paso 4: cree una instancia de la clase InlineImage y agréguela al diseño de texto.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Paso 1: crear un diseño de texto.

Para empezar, necesitará una aplicación con un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Si ya tiene una aplicación que muestra texto con un diseño de texto, vaya al paso 2.

Para agregar un diseño de texto, debe hacer lo siguiente:

1.  Declare un puntero a una interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Al final del método CreateDeviceIndependentResources, cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
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

    

3.  A continuación, debe cambiar la llamada al método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) a [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), como se muestra en el código siguiente.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Paso 2: definir una clase derivada de la interfaz IDWriteInlineObject.

La interfaz [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) proporciona compatibilidad con los objetos insertados en [DirectWrite](direct-write-portal.md) . Para usar objetos alineados, debe implementar esta interfaz. Controla el dibujo del objeto insertado, así como proporcionar métricas y otra información al representador.

Cree un nuevo archivo de encabezado y declare una interfaz denominada InlineImage, derivada de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

Además de QueryInterface, AddRef y Release heredados de IUnknown, esta clase debe tener los siguientes métodos:

-   [**Dibujar**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Paso 3: implementar la clase de objeto insertado.

Cree un nuevo archivo de C++, denominado InlineImage. cpp, para la implementación de la clase. Además del método LoadBitmapFromFile y los métodos heredados de la interfaz IUnknown, la clase InlineImage se compone de los siguientes métodos.

### <a name="the-constructor"></a>Constructor.


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



El primer argumento del constructor es el ID2D1RenderTarget en el que se representará la imagen insertada. Se almacena para su uso posterior al dibujar.

El destino de representación, IWICImagingFactory y el identificador URI del nombre de archivo se pasan al método LoadBitmapFromFile que carga el mapa de bits y almacena el tamaño del mapa de bits (ancho y alto) en la \_ variable miembro de Rect.

### <a name="the-draw-method"></a>Método draw.

El método [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) es una devolución de llamada a la que llama el objeto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) cuando es necesario dibujar el objeto insertado. El diseño de texto no llama directamente a este método.


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



En este caso, el dibujo del mapa de bits se realiza mediante el método [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) . sin embargo, se puede usar cualquier método de dibujo.

### <a name="the-getmetrics-method"></a>El método GetMetrics.


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



En el caso del método [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , almacene el ancho, el alto y la línea base en una estructura de [**\_ \_ \_ métricas de objeto en línea DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llama a esta función de devolución de llamada para obtener la medición del objeto insertado.

### <a name="the-getoverhangmetrics-method"></a>El método GetOverhangMetrics.


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



En este caso, no es necesario sobresalir, por lo que el método [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) devuelve todos los ceros.

### <a name="the-getbreakconditions-method"></a>El método GetBreakConditions.


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Paso 4: cree una instancia de la clase InlineImage y agréguela al diseño de texto.

Por último, en el método CreateDeviceDependentResources, cree una instancia de la clase InlineImage y agréguela al diseño de texto. Dado que contiene una referencia a [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que es un recurso dependiente del dispositivo, y el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) se crea mediante el destino de representación, el InlineImage también es dependiente del dispositivo y debe volver a crearse si se vuelve a crear el destino de representación.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



El método [**IDWriteTextLayout:: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) toma una estructura de intervalo de texto. El objeto se aplica al intervalo especificado aquí y se suprimirá cualquier texto del intervalo. Si la longitud del intervalo de texto es 0, el objeto no se dibujará.

En este ejemplo, hay un asterisco ( \* ) como marcador de posición en la posición donde se mostrará la imagen.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Dado que la clase InlineImage depende de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), debe liberarla al liberar el destino de representación.


```C++
SafeRelease(&pInlineImage_);
```



 

 