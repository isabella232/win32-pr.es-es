---
title: Efecto de contraste
description: Aumenta o disminuye el contraste de una imagen.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164178"
---
# <a name="contrast-effect"></a>Efecto de contraste

Aumenta o disminuye el contraste de una imagen.

El CLSID para este efecto es CLSID \_ D2D1Contrast.

La función de contraste modifica cada valor de canal de color mediante dos polinomios cuadráticos por partes que se encuentran con continuidad de pendiente en el punto (0,5, 0,5).

![polinomios cuadráticos por fragmentos que se encuentran con continuidad de pendiente en el punto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Imágenes de ejemplo](#example-images)
-   [Código de ejemplo](#sample-code)
-   [Propiedades de efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-images"></a>Imágenes de ejemplo

En este ejemplo se muestra la salida del efecto con el contraste máximo aplicado (Contraste = 1,0).

Antes

![imagen antes de aplicar el efecto](images/contrast-effect-before.png)

Después

![imagen después de aplicar el efecto](images/contrast-effect-after.png)

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de contraste se definen mediante la [**enumeración \_ CONTRAST PROP \_ de D2D1.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
