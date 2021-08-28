---
title: Cómo agregar objetos en línea a un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar objetos en línea a una DirectWrite que muestra texto mediante la interfaz IDWriteTextLayout.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca4969ded311bbaa4e87e5b70f1df1379c4ca549d2db06c8d1186ba548c77a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902904"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Cómo agregar objetos en línea a un diseño de texto

Proporciona un breve tutorial sobre cómo agregar objetos en línea a una [DirectWrite](direct-write-portal.md) que muestra texto mediante la [**interfaz IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

El producto final de este tutorial es una aplicación que muestra texto con una imagen insertada incrustada en ella, como se muestra en la siguiente captura de pantalla.

![captura de pantalla del "ejemplo de objeto insertado" con una imagen insertada](images/inlineobject.png)

Este tutorial contiene las siguientes partes:

-   [Paso 1: Crear un diseño de texto.](#step-1-create-a-text-layout)
-   [Paso 2: Definir una clase derivada de la interfaz IDWriteInlineObject.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Paso 3: Implementar la clase de objeto en línea.](#step-3-implement-the-inline-object-class)
    -   [The Constructor.](#the-constructor)
    -   [Método Draw.](#the-draw-method)
    -   [Método GetMetrics.](#the-getmetrics-method)
    -   [Método GetOvermetrics.](#the-getoverhangmetrics-method)
    -   [Método GetBreakConditions.](#the-getbreakconditions-method)
-   [Paso 4: Crear una instancia de la clase InlineImage y agregarla al diseño de texto.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Paso 1: Crear un diseño de texto.

Para empezar, necesitará una aplicación con un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Si ya tiene una aplicación que muestra texto con un diseño de texto, vaya al paso 2.

Para agregar un diseño de texto, debe hacer lo siguiente:

1.  Declare un puntero a una [**interfaz IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase .
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Al final del método CreateDeviceIndependentResources, cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)
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

    

3.  A continuación, debe cambiar la llamada al método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) a [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), como se muestra en el código siguiente.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Paso 2: Definir una clase derivada de la interfaz IDWriteInlineObject.

La interfaz IDWriteInlineObject proporciona [DirectWrite](direct-write-portal.md) compatibilidad con objetos en línea en la interfaz [**IDWriteInlineObject.**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) Para usar objetos en línea, debe implementar esta interfaz. Controla el dibujo del objeto en línea, así como proporcionar métricas y otra información al representador.

Cree un nuevo archivo de encabezado y declare una interfaz denominada InlineImage, derivada de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

Además de QueryInterface, AddRef y Release heredados de IUnknown, esta clase debe tener los métodos siguientes:

-   [**Dibujar**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOvermetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Paso 3: Implementar la clase de objeto en línea.

Cree un nuevo archivo de C++, denominado InlineImage.cpp, para la implementación de la clase . Además del método LoadBitmapFromFile y los métodos heredados de la interfaz IUnknown, la clase InlineImage está integrada por los métodos siguientes.

### <a name="the-constructor"></a>The Constructor.


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



El primer argumento del constructor es id2D1RenderTarget en el que se representará la imagen insertada. Se almacena para su uso más adelante al dibujar.

El destino de representación, IWICImagingFactory y el uri de nombre de archivo se pasan al método LoadBitmapFromFile que carga el mapa de bits y almacena el tamaño del mapa de bits (ancho y alto) en la variable miembro \_ rect.

### <a name="the-draw-method"></a>Método Draw.

El [**método Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) es una devolución de llamada a la que llama el objeto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) cuando es necesario dibujar el objeto en línea. El diseño de texto no llama directamente a este método.


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



En este caso, dibujar el mapa de bits se realiza mediante el [**método ID2D1RenderTarget::D rawBitmap;**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) sin embargo, se puede usar cualquier método para dibujar.

### <a name="the-getmetrics-method"></a>Método GetMetrics.


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



Para el [**método GetMetrics,**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) almacene el ancho, el alto y la línea base en una estructura [**DWRITE \_ INLINE \_ OBJECT \_ METRICS.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) [**IDWriteTextLayout llama**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a esta función de devolución de llamada para obtener la medida del objeto en línea.

### <a name="the-getoverhangmetrics-method"></a>Método GetOvermetrics.


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



En este caso, no se necesita ningún sobresalto, por lo que el [**método GetOvermetrics**](idwriteinlineobject-getoverhangmetrics.md) devuelve todos los ceros.

### <a name="the-getbreakconditions-method"></a>Método GetBreakConditions.


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Paso 4: Crear una instancia de la clase InlineImage y agregarla al diseño de texto.

Por último, en el método CreateDeviceDependentResources, cree una instancia de la clase InlineImage y agrégala al diseño de texto. Dado que contiene una referencia a [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), que es un recurso dependiente del dispositivo, y [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) se crea mediante el destino de representación, InlineImage también depende del dispositivo y se debe volver a crear si se vuelve a crear el destino de representación.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



El [**método IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) toma una estructura de intervalo de texto. El objeto se aplica al intervalo especificado aquí y se suprimirá cualquier texto del intervalo. Si la longitud del intervalo de texto es 0, el objeto no se dibujará.

En este ejemplo, hay un asterisco ( ) como un titular de \* posición en la posición donde se mostrará la imagen.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Puesto que la clase InlineImage depende de [**ID2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)debe liberarla al liberar el destino de representación.


```C++
SafeRelease(&pInlineImage_);
```



 

 