---
title: Función Texture2D::GatherCmpAlpha(S,float,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente alfa con un valor de comparación. | Función Texture2D::GatherCmpAlpha(S,float,float,int)
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Función HLSL de GatherCmpAlpha
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6e350ed14482646562121d910a8bd35f30403acf8dbde7df249ee1bc6ca800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789608"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Función Texture2D::GatherCmpAlpha(S,float,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente alfa con un valor de comparación.

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

## <a name="remarks"></a>Comentarios

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




