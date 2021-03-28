---
title: 'Texture1DArray:: MIPS. Operador (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture1DArray:: MIPS. Operador (función)'
ms.assetid: b8f2ef78-4b50-4051-a00f-5b81cd77d1e0
keywords:
- MIPS. Función de operador HLSL
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083656"
---
# <a name="texture1darraymipsoperator----function"></a>Texture1DArray:: MIPS. Operador (función)

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

*mipSlice* \[ de\]
</dt> <dd>

Tipo: **uint**

Índice del segmento MIP.

</dd> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint2**

Posición de índice. El primer componente contiene la coordenada x. El segundo componente indica el segmento de matriz deseado.

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



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




