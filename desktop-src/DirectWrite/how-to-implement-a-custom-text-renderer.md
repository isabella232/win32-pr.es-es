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
# <a name="render-using-a-custom-text-renderer"></a>Representación mediante un representador de texto personalizado

Un representador de texto personalizado derivado de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)puede dibujar un  [**diseño de texto**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) de [DirectWrite](direct-write-portal.md). Se requiere un representador personalizado para aprovechar algunas características avanzadas de DirectWrite, como la representación en un mapa de bits o una superficie de GDI, objetos insertados y efectos de dibujo de cliente. En este tutorial se describen los métodos de **IDWriteTextRenderer** y se proporciona una implementación de ejemplo que usa [Direct2D](../direct2d/direct2d-portal.md) para representar texto con un relleno de mapa de bits.

Este tutorial contiene las siguientes partes:

-   [Constructor](#the-constructor)
-   [DrawGlyphRun ()](#drawglyphrun)
-   [DrawUnderline () y DrawStrikethrough ()](#drawunderline-and-drawstrikethrough)
-   [Ajuste de píxeles, píxeles por DIP y transformación](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled()](#ispixelsnappingdisabled)
    -   [GetCurrentTransform()](#getcurrenttransform)
    -   [GetPixelsPerDip()](#getpixelsperdip)
-   [DrawInlineObject()](#drawinlineobject)
-   [El destructor](#the-destructor)
-   [Usar el representador de texto personalizado](#using-the-custom-text-renderer)

El representador de texto personalizado debe implementar los métodos heredados de IUnknown además de los métodos enumerados en la página de referencia de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) y a continuación.

Para ver el código fuente completo del representador de texto personalizado, consulte los archivos CustomTextRenderer. cpp y CustomTextRenderer. h del [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Constructor

El representador de texto personalizado necesitará un constructor. En este ejemplo se usan pinceles sólidos y de mapa de bits [Direct2D](../direct2d/direct2d-portal.md) para representar el texto.

Por este motivo, el constructor toma los parámetros que se encuentran en la tabla siguiente con descripciones.



| Parámetro       | Descripción                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Un puntero a un objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se usará para crear los recursos de Direct2D necesarios.                                                                                                        |
| *pRT*           | Un puntero al objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) en el que se representará el texto. |
| *pOutlineBrush* | Un puntero a la [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) que se usará para dibujar el contorno del texto.                                                                                                                     |
| *pFillBrush*    | Un puntero a la [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que se usará para rellenar el texto.                                                                                                                                      |



 

Estos se almacenarán en el constructor tal y como se muestra en el código siguiente.


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



## <a name="drawglyphrun"></a>DrawGlyphRun ()

El método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) es el método de devolución de llamada principal del representador de texto. Se pasa una ejecución de glifos que se va a representar además de información como el origen de la línea base y el modo de medición. También pasa un objeto de efecto de dibujo de cliente que se va a aplicar a la ejecución del glifo. Para obtener más información, vea el tema [Cómo agregar efectos de dibujo de cliente a un diseño de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Esta implementación de representación de texto representa ejecuciones de glifos convirtiéndolos en geometrías de [Direct2D](rendering-by-using-direct2d.md) y, a continuación, dibujando y rellenando las geometrías. Este proceso consta de los pasos siguientes.

1.  Cree un objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y, a continuación, recupere el objeto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) mediante el método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .

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

    

2.  La [**\_ \_ ejecución del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que se pasa a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contiene un objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominado *fontFace*, que representa el tipo de fuente para toda la ejecución del glifo. Coloque el contorno de la ejecución del glifo en el receptor de geometría mediante el método [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , como se muestra en el código siguiente.

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

    

3.  Después de rellenar el receptor de geometría, ciérrelo.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  El origen de la ejecución del glifo se debe traducir para que se represente desde el origen de base de referencia correcto, tal y como se muestra en el código siguiente.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* y *baselineOriginY* se pasan como parámetros al método de devolución de llamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .

5.  Cree la geometría transformada mediante el método [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) y pase la geometría de trazado y la matriz de traslación.

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

    

6.  Por último, dibuje el contorno de la geometría transformada y rellénelo mediante los métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) y los pinceles de [Direct2D](../direct2d/direct2d-portal.md) almacenados como variables de miembro.

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

    

7.  Ahora que ha terminado de dibujar, no olvide limpiar los objetos que se crearon en este método.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline () y DrawStrikethrough ()

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) también tiene devoluciones de llamada para dibujar el subrayado y el tachado. En este ejemplo se dibuja un rectángulo sencillo para un subrayado o tachado, pero se pueden dibujar otras formas.

Dibujar un subrayado mediante [Direct2D](../direct2d/direct2d-portal.md) consta de los siguientes pasos.

1.  En primer lugar, cree una estructura [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) del tamaño y la forma del subrayado. La estructura de [**\_ subrayado DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) que se pasa al método de devolución de llamada [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) proporciona el desplazamiento, el ancho y el grosor del subrayado.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  A continuación, cree un objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) mediante el método [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) y la estructura [**D2D1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) inicializada.

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Al igual que con la ejecución del glifo, el origen de la geometría de subrayado se debe traducir, en función de los valores de origen de la línea base, mediante el método [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .

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

    

4.  Por último, dibuje el contorno de la geometría transformada y rellénelo mediante los métodos [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) y [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) y los pinceles de [Direct2D](../direct2d/direct2d-portal.md) almacenados como variables de miembro.

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

    

5.  Ahora que ha terminado de dibujar, no olvide limpiar los objetos que se crearon en este método.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

El proceso para dibujar un tachado es el mismo. Sin embargo, el tachado tendrá un desplazamiento diferente y probablemente un ancho y un grosor distintos.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Ajuste de píxeles, píxeles por DIP y transformación

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled()

Se llama a este método para determinar si está deshabilitado el ajuste de píxeles. El valor predeterminado recomendado es **false** y es el resultado de este ejemplo.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform()

Este ejemplo se representa en un destino de representación de Direct2D, por lo que reenvía la transformación del destino de representación mediante [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip()

Se llama a este método para obtener el número de píxeles por píxel independiente del dispositivo (DIP).


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject()

Un representador de texto personalizado también tiene una devolución de llamada para dibujar objetos insertados. En este ejemplo, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) devuelve E \_ NOTIMPL. Una explicación de cómo se dibujan los objetos insertados queda fuera del ámbito de este tutorial. Para obtener más información, vea el tema [Cómo agregar objetos insertados en un diseño de texto](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>El destructor

Es importante liberar los punteros usados por la clase de representador de texto personalizado.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Usar el representador de texto personalizado

Se representa con el representador personalizado mediante el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que toma una interfaz de devolución de llamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como argumento, tal y como se muestra en el código siguiente.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



El método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) llama a los métodos de la devolución de llamada del representador personalizado que se proporciona. Los métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritos anteriormente realizan las funciones de dibujo.

 

 