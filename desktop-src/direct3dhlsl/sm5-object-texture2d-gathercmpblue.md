---
title: Función Texture2D::GatherCmpBlue(S,float,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente azul con un valor de comparación. | Función Texture2D::GatherCmpBlue(S,float,float,int)
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
keywords:
- Función HLSL de GatherCmpBlue
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5344414ce35b1063fff938eb6ea0f6ed0813d407f99d1fc2202c2cb58b6a74b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671325"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a>Función Texture2D::GatherCmpBlue(S,float,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente azul con un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **SamplerComparisonState**

Índice de sampler de base cero.

</dd> <dt>

*ubicación* \[ En\]
</dt> <dd>

Tipo: **float2**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **float**

Valor que se compara con cada valor muestreado.

</dd> <dt>

*desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float4**

Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.

## <a name="remarks"></a>Comentarios

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de GatherCmpBlue](texture2d-gathercmpblue.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




