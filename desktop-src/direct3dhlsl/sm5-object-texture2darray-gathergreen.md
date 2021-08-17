---
title: Función Texture2DArray::GatherGreen(S,float,int)
description: Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2DArray::GatherGreen(S,float,int)
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
keywords:
- Función GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fab908d7c8b0ed97a99aa04b8557e1008235cb91597ab00bdc90912e83e9627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724586"
---
# <a name="texture2darraygathergreensfloatint-function"></a>Función Texture2DArray::GatherGreen(S,float,int)

Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType GatherGreen(
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

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherGreen](texture2darray-gathergreen.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




