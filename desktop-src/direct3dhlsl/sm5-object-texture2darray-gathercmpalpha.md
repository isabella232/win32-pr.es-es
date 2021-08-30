---
title: Función Texture2DArray::GatherCmpAlpha(S,float,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación. | Función Texture2DArray::GatherCmpAlpha(S,float,float,int)
ms.assetid: d5fc78eb-2378-4e63-a712-c6f4ef9fc729
keywords:
- Función GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa91a1e86cbcb8d9a931b6b761c544833dd027f7d8592e0827da060fea501bdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067595"
---
# <a name="texture2darraygathercmpalphasfloatfloatint-function"></a>Función Texture2DArray::GatherCmpAlpha(S,float,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación.

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

Índice de sampler de base cero.

</dd> <dt>

*ubicación* \[ En\]
</dt> <dd>

Tipo: **float3**

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

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherCmpAlpha](texture2darray-gathercmpalpha.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




