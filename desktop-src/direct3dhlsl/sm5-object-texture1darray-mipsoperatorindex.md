---
title: Texture1DArray::mips. Función operator
description: Devuelve una variable de recurso de solo lectura. | Texture1DArray::mips. Función operator
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
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
ms.openlocfilehash: cbe2d1116839cede8dda69f1b0b8cf9a049595e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966543"
---
# <a name="texture1darraymipsoperator----function"></a>Texture1DArray::mips. Función operator

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
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

Tipo: **uint2**

Posición del índice. El primer componente contiene la coordenada X. El segundo componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

### <a name="usage-example"></a>Ejemplo de uso


```
Texture1DArray<float4> tex;
uint mip = 2;
uint2 pos_x_and_array = {1234, 3};
float4 f = tex.mips[mip][pos_x_and_array];        
        
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




