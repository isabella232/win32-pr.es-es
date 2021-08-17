---
title: Texture2DArray::mips. Función de operador
description: Devuelve una variable de recurso de solo lectura. | Texture2DArray::mips. Función de operador
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- Mips. Función de operador HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5dff48f721e45ef7853c125b1d7d0d32d5cb311a3dbc3b31d4100f3038a8fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724596"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray::mips. Función de operador

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*mipSlice* \[ En\]
</dt> <dd>

Tipo: **uint**

Índice del segmento mip.

</dd> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint3**

Posición del índice. El primer y segundo componentes contienen las coordenadas (x, y). El tercer componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




