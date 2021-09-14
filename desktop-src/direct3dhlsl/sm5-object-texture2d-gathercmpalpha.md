---
title: Función Texture2D::GatherCmpAlpha(S,float,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación. | Función Texture2D::GatherCmpAlpha(S,float,float,int)
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
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
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063691"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Función Texture2D::GatherCmpAlpha(S,float,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente alfa con un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 GatherCmpAlpha(
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

## <a name="remarks"></a>Observaciones

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




