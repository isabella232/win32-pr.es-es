---
title: Cómo agregar efectos de dibujo de cliente a un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente a una aplicación DirectWrite que muestra texto mediante la interfaz IDWriteTextLayout y un representador de texto personalizado.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071719"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Cómo agregar efectos de dibujo de cliente a un diseño de texto

Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente [a](direct-write-portal.md) una aplicación DirectWrite que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y un representador de texto personalizado.

El producto final de este tutorial es una aplicación que muestra texto que tiene intervalos de texto con un efecto de dibujo de color diferente en cada uno de ellos, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de "ejemplo de efecto de dibujo de cliente" en colores diferentes](images/drawingeffects.png)

> [!Note]  
> Este tutorial está pensado para ser un ejemplo simplificado de cómo crear efectos de dibujo de cliente personalizados, no un ejemplo de un método simple para dibujar texto de color. Vea la [**página de referencia IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) para obtener más información.

 

Este tutorial contiene las siguientes partes:

-   [Paso 1: Crear un diseño de texto](#step-1-create-a-text-layout)
-   [Paso 2: Implementar una clase de efecto de dibujo personalizada](#step-2-implement-a-custom-drawing-effect-class)
-   [Paso 3: Implementar una clase de representador de texto personalizado](#step-3-implement-a-custom-text-renderer-class)
    -   [The Constructor](#the-constructor)
    -   [Método DrawGlyphRun](#the-drawglyphrun-method)
    -   [The Destructor](#the-destructor)
-   [Paso 4: Crear el representador de texto](#step-4-create-the-text-renderer)
-   [Paso 5: Crear instancias de los objetos de efecto de dibujo de color](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Paso 6: Establecer el efecto de dibujo para intervalos de texto específicos](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Paso 7: Dibujar el diseño de texto mediante el representador personalizado](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Paso 8: Limpieza](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Paso 1: Crear un diseño de texto

Para empezar, necesitará una aplicación con un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Si ya tiene una aplicación que muestra texto con un diseño de texto o usa el código de ejemplo DrawingEffect personalizado, vaya al paso 2.

Para agregar un diseño de texto, debe hacer lo siguiente:

1.  Declare un puntero a una [**interfaz IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase .
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Al final del método **CreateDeviceIndependentResources,** cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)
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

    

3.  Por último, recuerde liberar el diseño de texto en el destructor.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Paso 2: Implementar una clase de efecto de dibujo personalizada

Aparte de los métodos heredados de IUnknown, una interfaz de efecto de dibujo de cliente personalizada no tiene requisitos sobre lo que debe implementar. En este caso, la **clase ColorDrawingEffect** simplemente contiene un valor [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) y declara métodos para obtener y establecer este valor, así como un constructor que puede establecer el color inicialmente.

Después de aplicar un efecto de dibujo de cliente a un intervalo de texto en un objeto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) el efecto de dibujo se pasa al método [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de cualquier ejecución de glifo que se va a representar. A continuación, los métodos del efecto de dibujo están disponibles para el representador de texto.

Un efecto de dibujo de cliente puede ser tan complejo como desee, con más información que en este ejemplo, así como proporcionar métodos para modificar glifos, crear objetos que se usarán para dibujar, etc.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Paso 3: Implementar una clase de representador de texto personalizado

Para aprovechar las ventajas de un efecto de dibujo de cliente, debe implementar un representador de texto personalizado. Este representador de texto aplicará el efecto de dibujo pasado por el método [**IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) a la ejecución del glifo que se va a dibujar.

### <a name="the-constructor"></a>The Constructor

El constructor del representador de texto personalizado almacena el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se usará para crear objetos [Direct2D](../direct2d/direct2d-portal.md) y el destino de representación de Direct2D en el que se dibujará el texto.


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



### <a name="the-drawglyphrun-method"></a>Método DrawGlyphRun

Una ejecución de glifo es un conjunto de glifos que comparten el mismo formato, incluido el efecto de dibujo de cliente. El [**método DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) se encarga de la representación de texto para una ejecución de glifo especificada.

En primer lugar, cree un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)y, a continuación, recupere el esquema de ejecución del glifo mediante [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline). A continuación, transforme el origen de la geometría mediante el método [**Id2D1Factory::CreateTransformedGeometry de**](../direct2d/id2d1factory-createtransformedgeometry.md) [Direct2D,](../direct2d/direct2d-portal.md) como se muestra en el código siguiente.


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



A continuación, declare un objeto de pincel sólido de [Direct2D.](../direct2d/direct2d-portal.md)


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Si el *parámetro clientDrawingEffect* no es NULL, consulte el objeto para la **interfaz ColorDrawingEffect.** Esto funcionará porque establecerá esta clase como el efecto de dibujo de cliente en los intervalos de texto del objeto de diseño de texto.

Una vez que tenga un puntero a la interfaz **ColorDrawingEffect,** puede recuperar el valor [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) que almacena mediante el **método GetColor.** A continuación, use **D2D1 \_ COLOR \_ F** para crear un [**objeto ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) en ese color.

Si el *parámetro clientDrawingEffect* **es NULL,** solo tiene que crear un [**ID2D1SolidColorBrush negro.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)


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



Por último, dibuje la geometría del contorno y rellénela con el pincel de color sólido que acaba de crear.


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



### <a name="the-destructor"></a>The Destructor

No olvide liberar el generador [de Direct2D](../direct2d/direct2d-portal.md) y representar el destino en el destructor.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Paso 4: Crear el representador de texto

En los **recursos CreateDeviceDependent,** cree el objeto de representador de texto personalizado. Depende del dispositivo porque usa **ID2D1RenderTarget,** que es dependiente del propio dispositivo.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Paso 5: Crear instancias de los objetos de efecto de dibujo de color

Cree una instancia **de los objetos ColorDrawingEffect** en rojo, verde y azul.


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Paso 6: Establecer el efecto de dibujo para intervalos de texto específicos

Establezca el efecto de dibujo para intervalos específicos de texto mediante el método [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) y una estructura [**DWRITE \_ TEXT \_ RANGE.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range)


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Paso 7: Dibujar el diseño de texto mediante el representador personalizado

Debe llamar al método [**IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) en lugar de a los métodos [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) o [**ID2D1RenderTarget::D rawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Paso 8: Limpieza

En el destructor DemoApp, libere el representador de texto personalizado.


```C++
SafeRelease(&pTextRenderer_);
```



Después, agregue código para liberar las clases de efecto de dibujo de cliente.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 