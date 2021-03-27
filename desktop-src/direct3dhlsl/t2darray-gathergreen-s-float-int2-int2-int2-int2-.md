---
title: 'Texture2DArray:: GatherGreen (S, Float, INT2, INT2, INT2, INT2) (función)'
description: 'Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherGreen (S, Float, INT2, INT2, INT2, INT2) (función)'
ms.assetid: 7E79442E-286F-4BDB-8D7A-2C20A0933585
keywords:
- GatherGreen de función HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12e8649882c7e3c8fd4d9f88cd37d1a27952eb2b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003703"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2-function"></a>Texture2DArray:: GatherGreen (S, Float, INT2, INT2, INT2, INT2) (función)

Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de muestra de base cero.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*Offset1* \[ de\]
</dt> <dd>

Tipo: **INT2**

Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset2* \[ de\]
</dt> <dd>

Tipo: **INT2**

Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset3* \[ de\]
</dt> <dd>

Tipo: **INT2**

Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset4* \[ de\]
</dt> <dd>

Tipo: **INT2**

Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherGreen](texture2darray-gathergreen.md)
</dt> </dl>

 

 




