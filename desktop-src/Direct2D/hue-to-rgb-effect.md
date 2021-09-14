---
title: Efecto de matiz a RGB
description: Convierte una imagen HSL (matiz, saturación, lumez) o HSV (matiz, saturación, valor) en el espacio de colores RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163117"
---
# <a name="hue-to-rgb-effect"></a>Efecto de matiz a RGB

Convierte una imagen HSL (matiz, saturación, lumez) o HSV (matiz, saturación, valor) en el espacio de colores RGB.

HSL y HSV son dos modelos diferentes para representar un color RGB en un espacio de colores cilíndrica. Son útiles porque permiten razonar sobre un color mediante conceptos más intuitivos, como matiz e intensidad, frente a la combinación de valores rojo, verde y azul.

Este efecto pasa a través de cualquier valor alfa de entrada.

El CLSID para este efecto es CLSID \_ D2D1HueToRgb.

Para invertir el comportamiento de este efecto, use el [efecto RGB a Hue](rgb-to-hue-effect.md).

-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de contraste se definen mediante la [**enumeración D2D1 \_ HUETORGB \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |



## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
