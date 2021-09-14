---
title: Temperatura y efecto de tono
description: Temperatura y efecto de tono
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162554"
---
# <a name="temperature-and-tint-effect"></a>Temperatura y efecto de tono

El CLSID para este efecto es CLSID \_ D2D1TemperatureTint.

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades de efecto

Las propiedades del efecto de temperatura y tono se definen mediante la [**enumeración D2D1 \_ TEMPERATUREANDTINT \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Servidor mínimo compatible | \[Windows 10 aplicaciones de escritorio \| Windows store\] |
| Encabezado                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |



 

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
