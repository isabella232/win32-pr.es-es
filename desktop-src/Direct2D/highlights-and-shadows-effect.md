---
title: Efecto de resaltado y sombras
description: Ajusta los resaltados y las sombras de la imagen.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335de3bc6b115221c1a2a343cac9c5c5154a6d868c9fa8f63b2cfa719e287c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569624"
---
# <a name="highlights-and-shadows-effect"></a>Efecto de resaltado y sombras

Ajusta los resaltados y las sombras de la imagen.

El CLSID para este efecto es CLSID \_ D2D1HighlightsShadows.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de salida de efecto](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de resaltado y sombra se definen mediante la enumeración [**D2D1 \_ HIGHLIGHTSANDSHADOWS \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop)

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
