---
title: Efecto de relieve
description: Crea una versión de escala de grises de la imagen que aparece como si se hubiera estampado en papel.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802300"
---
# <a name="emboss-effect"></a>Efecto de relieve

Crea una versión de escala de grises de la imagen que aparece como si se hubiera estampado en papel.

El CLSID para este efecto es CLSID \_ D2D1Emboss.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de resultado de efecto](images/emboss-effect.png)

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades del efecto

Las propiedades del efecto de relieve se definen mediante la enumeración de [**D2D1 \_ relieve \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
