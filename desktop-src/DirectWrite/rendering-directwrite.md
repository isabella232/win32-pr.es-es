---
title: Representación DirectWrite
description: Representación DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069977"
---
# <a name="rendering-directwrite"></a>Representación DirectWrite

## <a name="rendering-options"></a>Opciones de representación

El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D;](../direct2d/direct2d-portal.md)sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

La cadena descrita por un [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.

## <a name="1-render-using-direct2d"></a>1. Representación mediante Direct2D

Para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante Direct2D, use el método [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) como se muestra en el código siguiente.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Para obtener una vista más detallada del dibujo de un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante [Direct2D,](../direct2d/direct2d-portal.md)vea Tareas iniciales [con DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. Representar mediante un representador de texto personalizado.

Se representa con un representador personalizado mediante el método [**IDWriteTextLayout::D raw,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) que toma una interfaz de devolución de llamada derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) como argumento, como se muestra en el código siguiente.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



El [**método IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) llama a los métodos de la devolución de llamada del representador personalizado que proporcione. Los [**métodos DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) realizan las funciones de dibujo.

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declara métodos para dibujar una ejecución de glifo, subrayado, tachado y objetos en línea. La aplicación debe implementar estos métodos. La creación de un representador de texto personalizado permite a la aplicación aplicar efectos adicionales al representar texto, como un relleno o un contorno personalizados. Se incluye un representador de texto personalizado de ejemplo en el [DirectWrite Hola mundo ejemplo](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. Representar ClearType en una superficie GDI.

La representación en una superficie GDI es realmente un ejemplo del uso de un representador de texto personalizado. Sin embargo, parte del trabajo se realiza en forma de la [**interfaz IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)

Para crear esta interfaz, use el [**método IDWriteGdiInterop::CreateBitmapRenderTarget.**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)

El [**método DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) del representador de texto personalizado llama al método [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar los glifos. La representación de los objetos subrayado, tachado y en línea debe realizarla el representador personalizado.

La [**interfaz IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) se representa en un contexto de dispositivo (DC) en memoria. Para obtener un identificador para este controlador de dominio, use el [**método IDWriteBitmapRenderTarget::GetMemoryDC.**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc)


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Una vez realizado el dibujo, el controlador de dominio de memoria del objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) debe copiarse en la superficie GDI de destino.

> [!Note]  
> También tiene la opción de transferir el mapa de bits a otro tipo de superficie, como una GDI+ mapa de bits.

 


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
> La aplicación tiene la responsabilidad de representarlo todo en la ventana al final. Esto incluye texto y gráficos. Esto tiene una penalización de rendimiento. Además, la representación en un controlador de dominio de memoria no está acelerada por hardware GDI.

 

Para obtener información general más detallada sobre cómo interoperar con GDI, [consulte Interoperación con GDI.](interoperating-with-gdi.md)

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. Representar texto de escala de grises de forma transparente en una superficie GDI. (Windows 8 y versiones posteriores)

A partir Windows 8, puede representar texto de escala de grises de forma transparente en una superficie GDI para mejorar el rendimiento. Para ello, debe:

1.  Borre el controlador de dominio de memoria para que sea transparente.
2.  Represente texto en hdc de memoria mediante suavizado de contorno de escala de grises (DWRITE \_ TEXT \_ ANTIALIAS \_ MODE \_ GRAYSCALE).
3.  Use la [**función AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) para representar la memoria HDC de forma transparente sobre el HDC de destino final.
4.  Repita tantas veces como sea necesario (por ejemplo, una vez por cada ejecución de glifo) y, entre otros gráficos, se puede representar directamente en el HDC de destino final sin que la función [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) la sobrescriba.


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

[Representación mediante Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Representación mediante un representador de texto personalizado](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Representación en una superficie GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperación con GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 