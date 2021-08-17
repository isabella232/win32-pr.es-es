---
title: Función Texture2DArray::GatherCmpRed(S,float,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente rojo con un valor de comparación. | Función Texture2DArray::GatherCmpRed(S,float,float,int)
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- Función GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aea723bbcdc2822adb8084cbdb5feff155165158d3abaf872a96259a77accdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724616"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a>Función Texture2DArray::GatherCmpRed(S,float,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente rojo con un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 GatherCmpRed(
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

*offset* \[ En\]
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



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherCmpRed](texture2darray-gathercmpred.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




