---
title: Texture2DMS::sample. Función de operador
description: Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados. | Texture2DMS::sample. Función de operador
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- Muestra. Función de operador HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5d7082ee72c49d3aa4be131491151b1bab65502e6fe85884b2a03573c497b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508477"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS::sample. Función de operador

Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados.

## <a name="syntax"></a>Sintaxis

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*sampleSlice* \[ En\]
</dt> <dd>

Tipo: **uint**

Índice de segmento de ejemplo.

</dd> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint2**

Posición del índice. Los componentes contienen las coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




