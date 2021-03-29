---
title: 'Texture2DMSArray:: sample. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2DMSArray:: sample. Operador (función)'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986677"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray:: sample. Operador (función)

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
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

Tipo: **UInt3**

Posición de índice. Los componentes primero y segundo contienen las coordenadas (x, y). El tercer componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2DMSArray<float4, 4> alpha;

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




