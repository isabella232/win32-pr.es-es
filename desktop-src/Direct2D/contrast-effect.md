---
title: Efecto de contraste
description: Aumenta o disminuye el contraste de una imagen.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079480"
---
# <a name="contrast-effect"></a>Efecto de contraste

Aumenta o disminuye el contraste de una imagen.

El CLSID para este efecto es CLSID \_ D2D1Contrast.

La función Contrast modifica cada valor del canal de color mediante dos polinómicas cuadráticas a trozos que se cumplen con la continuidad de la pendiente en el punto (0,5, 0,5).

![a trozos polinómicos cuadráticas que se cumplen con la continuidad de la pendiente en el punto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Imágenes de ejemplo](#example-images)
-   [Código de ejemplo](#sample-code)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-images"></a>Imágenes de ejemplo

En este ejemplo se muestra el resultado del efecto con el contraste máximo aplicado (Contrast = 1,0).

Antes

![imagen antes de aplicar el efecto](images/contrast-effect-before.png)

Después

![se aplica la imagen después del efecto](images/contrast-effect-after.png)

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

## <a name="effect-properties"></a>Propiedades del efecto

Las propiedades del efecto de contraste se definen mediante la enumeración de la propiedad [**\_ \_ contraste D2D1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
