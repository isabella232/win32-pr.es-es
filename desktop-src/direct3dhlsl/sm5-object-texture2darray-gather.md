---
title: Función Texture2DArray::Gather(S,float,int)
description: Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2DArray::Gather(S,float,int)
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Recopilación de la función HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f684efa4cb597a640b78a2cdd08074d47fec3b4ec2f8a4a6fe6bcf993fd53ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119367805"
---
# <a name="texture2darraygathersfloatint-function"></a>Función Texture2DArray::Gather(S,float,int)

Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **sampler**

Índice de sampler de base cero.

</dd> <dt>

*ubicación* \[ En\]
</dt> <dd>

Tipo: **float3**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Recopilación de métodos](texture2darray-gather.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




