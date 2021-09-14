---
title: Introducción a los destinos de representación A8 compatibles
description: Describe los conceptos básicos de los destinos de representación A8 compatibles y proporciona ejemplos que muestran cómo usarlos.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164186"
---
# <a name="compatible-a8-render-targets-overview"></a>Introducción a los destinos de representación A8 compatibles

En este tema se describen los conceptos básicos de un destino de representación A8 compatible y se proporcionan ejemplos de cómo usarlo.

Un destino de representación A8 compatible es un destino de representación compatible [**(ID2D1BitmapRenderTarget)**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)que usa un formato de píxeles A8 (DXGI \_ FORMAT \_ A8 \_ UNORM). Puede usar un destino de representación A8 compatible para mejorar el rendimiento de la aplicación y proporcionar transiciones más fluidas durante la animación de texto. Un destino de representación A8 compatible es especialmente útil cuando se intenta mejorar lo siguiente:

-   Velocidad de fotogramas de la aplicación que representa texto o geometría con suavizado de alias que incluye solo animaciones simples, como la traducción, la rotación, la escala o los cambios de color.

-   Continuidad visual de la aplicación que extiende y diminuta el texto durante una animación.

Para crear un destino de representación A8 compatible, use el método [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) junto con el formato de píxelES UNORM DXGI FORMAT A8 y especifique un destino de representación \_ \_ compatible \_ devuelto. Para obtener más información sobre los formatos de píxel, vea [Formatos de píxeles admitidos y modos alfa.](./supported-pixel-formats-and-alpha-modes.md)

Por ejemplo, para animar eficazmente el texto que se muestra en la siguiente captura de pantalla, use un destino de representación A8 compatible para almacenar en caché el texto como una máscara de opacidad. A continuación, aplique transformaciones a la máscara de opacidad para lograr resultados de representación rápidos.

![captura de pantalla de texto para animar](images/a8rendertarget.png)

El código siguiente muestra cómo hacerlo. Crea un destino de representación A8 compatible, recupera el mapa de bits de él y, a continuación, representa el mapa de bits mediante [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).

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