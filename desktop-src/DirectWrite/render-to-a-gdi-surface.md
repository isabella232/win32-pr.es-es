---
title: Representar en una superficie de GDI
description: Representar en una superficie de GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421329"
---
# <a name="render-to-a-gdi-surface"></a>Representar en una superficie de GDI

En algunos casos, puede que desee poder mostrar texto de [DirectWrite](direct-write-portal.md) en una superficie de GDI. La interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula un mapa de bits y un contexto de dispositivo para representar texto en. Puede crear un **IDWriteBitmapRenderTarget** mediante el método [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , como se muestra en el código siguiente.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Para representar con un [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), debe implementar una interfaz de devolución de llamada de representador de texto personalizada derivada de la interfaz [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Debe implementar métodos para dibujar una ejecución de glifos, subrayado, tachado, objetos insertados, etc. Para obtener una lista completa de los métodos, vea la página de referencia de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . No todos los métodos deben implementarse, solo pueden devolver **E \_ NOTIMPL** y el dibujo continuará.

Después, puede dibujar el texto mediante el método [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) y pasar la interfaz de devolución de llamada que ha implementado como parámetro. El método **IDWriteTextLayout::D RAW** llama a los métodos de la devolución de llamada del representador personalizado que se proporciona. Los métodos [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)y [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) realizan las funciones de dibujo.

En la implementación de [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), llame al método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para dibujar los glifos. El representador personalizado debe realizar la representación del subrayado, el tachado y los objetos insertados.

[**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tiene un parámetro Rect out opcional que contiene los límites del área donde se dibujó el texto. Puede usar esta información para establecer el rectángulo delimitador del contexto del dispositivo con la función [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) proporcionada por GDI. El código siguiente es una implementación de ejemplo del método [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de un representador personalizado.


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



La interfaz [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) se representa en un contexto de dispositivo (DC) en memoria. Obtiene un identificador de este controlador de dominio mediante el método [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) . En cuanto se realiza el dibujo, el controlador de dominio de memoria del objeto **IDWriteBitmapRenderTarget** debe copiarse en la superficie GDI de destino.

Puede recuperar el rectángulo delimitador mediante la función [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) y, a continuación, usar el rectángulo delimitador con la función [**bitblt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar el texto de [DirectWrite](direct-write-portal.md) representado del DC de memoria en la superficie de GDI, tal y como se muestra en el código siguiente.


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



 

 