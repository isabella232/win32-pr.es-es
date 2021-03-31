---
title: Información general de destinos de representación A8 compatibles
description: Describe los aspectos básicos de los destinos de representación A8 compatibles y proporciona ejemplos que muestran cómo utilizarlos.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "103995795"
---
# <a name="compatible-a8-render-targets-overview"></a>Información general de destinos de representación A8 compatibles

En este tema se describen los aspectos básicos de un destino de representación de A8 compatible y se proporcionan ejemplos de cómo utilizarlos.

Un destino de representación de A8 compatible es un destino de representación compatible ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) que usa un formato de píxel A8 (formato de DXGI \_ \_ a8 \_ UNORM). Puede usar un destino de representación A8 compatible para mejorar el rendimiento de la aplicación y proporcionar transiciones más suaves durante la animación del texto. Un destino de representación A8 compatible es especialmente útil cuando se intenta mejorar lo siguiente:

-   Velocidad de fotogramas de la aplicación que representa el texto o geometría suavizada que incluye solo animaciones simples, como cambios de traslación, rotación, escala o color.

-   La continuidad visual de la aplicación que amplía y diminshes el texto durante una animación.

Para crear un destino de representación de A8 compatible, use el método [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) junto con el formato de DXGI de la \_ \_ a8 \_ UNORM píxeles y especifique un destino de representación compatible. Para obtener más información sobre los formatos de píxeles, vea [formatos de píxeles compatibles y modos alfa](./supported-pixel-formats-and-alpha-modes.md).

Por ejemplo, para animar de forma eficaz el texto que se muestra en la siguiente captura de pantalla, use un destino de representación A8 compatible para almacenar en caché el texto como una máscara de opacidad. A continuación, aplique transformaciones a la máscara de opacidad para conseguir resultados de representación rápidos.

![captura de pantalla del texto que se va a animar](images/a8rendertarget.png)

El código siguiente muestra cómo hacerlo. Crea un destino de representación de A8 compatible, recupera el mapa de bits de él y, a continuación, representa el mapa de bits mediante [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a>Temas relacionados

[Referencia de Direct2D](reference.md)