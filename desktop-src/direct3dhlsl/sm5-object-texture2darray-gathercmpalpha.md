---
title: 'Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación. | Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)'
ms.assetid: d5fc78eb-2378-4e63-a712-c6f4ef9fc729
keywords:
- GatherCmpAlpha de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42f11131ebf377ddc64be5309c3edf77214ddd4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362351"
---
# <a name="texture2darraygathercmpalphasfloatfloatint-function"></a>Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)

En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **SamplerComparisonState**

Índice de muestra de base cero.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float3**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **float**

Valor que se va a comparar cada uno con cada valor muestreado.

</dd> <dt>

*desplazamiento* \[ de\]
</dt> <dd>

Tipo: **INT2**

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **FLOAT4**

Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherCmpAlpha](texture2darray-gathercmpalpha.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




