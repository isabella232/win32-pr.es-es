---
title: Efecto RGB a matiz
description: Convierte una imagen RGB en los espacios de color HSL (Matiz, Saturación, Lightness) o HSV (Matiz, Saturación, Valor).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162606"
---
# <a name="rgb-to-hue-effect"></a>Efecto RGB a matiz

Convierte una imagen RGB en los espacios de color HSL (Matiz, Saturación, Lightness) o HSV (Matiz, Saturación, Valor).

HSL y HSV son dos modelos diferentes para representar un color RGB en un espacio de colores cilíndrica. Son útiles porque permiten razonar sobre un color mediante conceptos más intuitivos, como el matiz y la intensidad, frente a la combinación de valores rojo, verde y azul.

Este efecto normaliza los datos de salida (matiz, valor de saturación para HSV o matiz, saturación, lightness para HSL) al intervalo \[ 0, 1 \] .

El CLSID para este efecto es CLSID \_ D2D1RgbToHue.

Para invertir el comportamiento de este efecto, use [el efecto Hue a RGB](hue-to-rgb-effect.md).

-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="sample-code"></a>Código de ejemplo


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de contraste se definen mediante la [**enumeración D2D1 \_ RGBTOHUE \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
