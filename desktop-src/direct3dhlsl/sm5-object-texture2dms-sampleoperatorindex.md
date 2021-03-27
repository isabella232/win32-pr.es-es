---
title: 'Texture2DMS:: sample. Operador (función)'
description: 'Recupera un valor del recurso en la ubicación y el índice de ejemplo proporcionados. | Texture2DMS:: sample. Operador (función)'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- AdventureWorks. Función de operador HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280187"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS:: sample. Operador (función)

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

*sampleSlice* \[ de\]
</dt> <dd>

Tipo: **uint**

Índice del segmento de ejemplo.

</dd> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint2**

Posición de índice. Los componentes contienen las coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




