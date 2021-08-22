---
title: Texture2DMSArray::sample. Función operator
description: Devuelve una variable de recurso de solo lectura. | Texture2DMSArray::sample. Función de operador
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: 09ac18e7830dfe6b18718deed56e8495ba476dcedcb8290eab4e16aa0d7f24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508330"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray::sample. Función operator

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

*sampleSlice* \[ En\]
</dt> <dd>

Tipo: **uint**

Índice de segmento de ejemplo.

</dd> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint3**

Posición del índice. El primer y segundo componente contienen las coordenadas (x, y). El tercer componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2DMSArray<float4, 4> alpha;

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




