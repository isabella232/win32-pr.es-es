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
# <a name="rendering-directwrite"></a>Representación de DirectWrite

## <a name="rendering-options"></a>Opciones de representación

El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D](../direct2d/direct2d-portal.md); sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

La cadena descrita por un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.

## <a name="1-render-using-direct2d"></a>1. representar mediante Direct2D

Para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante Direct2D, use el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , como se muestra en el código siguiente.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Para obtener más información detallada sobre cómo dibujar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante [Direct2D](../direct2d/direct2d-portal.md), consulte [Introducción con DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. representar mediante un representador de texto personalizado.

Se representa con un representador personalizado mediante el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , que toma una interfaz de devolución de llamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como argumento, tal y como se muestra en el código siguiente.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



El método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) llama a los métodos de la devolución de llamada del representador personalizado que se proporciona. Los métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) realizan las funciones de dibujo.

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declara métodos para dibujar una ejecución de glifos, subrayado, tachado y objetos insertados. Depende de la aplicación implementar estos métodos. La creación de un representador de texto personalizado permite a la aplicación aplicar efectos adicionales al representar texto, como un relleno o un contorno personalizados. En el [ejemplo de Hola mundo de DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)se incluye un representador de texto personalizado de ejemplo.

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. representar ClearType en una superficie de GDI.

La representación en una superficie de GDI es, en realidad, un ejemplo del uso de un representador de texto personalizado. Sin embargo, parte del trabajo se realiza en forma de la interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .

Para crear esta interfaz, use el método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .

El método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) del representador de texto personalizado llama al método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar los glifos. El representador personalizado debe realizar la representación de los objetos de subrayado, tachado e insertado.

La interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) se representa en un contexto de dispositivo (DC) en memoria. Obtiene un identificador de este controlador de dominio mediante el método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Una vez realizado el dibujo, el controlador de dominio de memoria del objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) debe copiarse en la superficie GDI de destino.

> [!Note]  
> También tiene la opción de transferir el mapa de bits a otro tipo de superficie, como una superficie de GDI+.

 


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
> La aplicación tiene la responsabilidad de representar todo en la ventana al final. Esto incluye texto y gráficos. Esto tiene una penalización del rendimiento. Además, la representación en un controlador de dominio de memoria no es una aceleración del hardware de GDI.

 

Para obtener información general más detallada sobre la interoperabilidad con GDI, vea [interoperar con GDI](interoperating-with-gdi.md).

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. representar el texto de escala de grises de forma transparente en una superficie de GDI. (Windows 8 y versiones posteriores)

A partir de Windows 8, puede representar texto de escala de grises de forma transparente en una superficie de GDI para mejorar el rendimiento. Para ello, debe hacer lo siguiente:

1.  Borre el DC de memoria para que sea transparente.
2.  Representar texto en la memoria HDC usando antialiasing de escala de grises (modo de SUAVIZAdo de contorno de \_ texto DWRITE \_ \_ \_ ).
3.  Use la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) para representar la memoria HDC de forma transparente sobre la HDC de destino final.
4.  Repita tantas veces como sea necesario (por ejemplo, una vez por ejecución del glifo) y entre otros gráficos se puede representar directamente en el destino HDC de destino sin sobrescribirlo con la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar mediante Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Representación mediante un representador de texto personalizado](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Representar en una superficie de GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperar con GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 