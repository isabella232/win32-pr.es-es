---
title: Función Texture1DArray::Operator
description: Devuelve una variable de recurso de solo lectura. | Función Texture1DArray::Operator
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
keywords:
- Función de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed214b4c4ccc55dfe6500f70659f4f81b2188de68b8cea7b5ba69c495108d730
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788355"
---
# <a name="texture1darrayoperator--function"></a>Función Texture1DArray::Operator

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint2**

Posición del índice. El primer componente contiene la coordenada X. El segundo componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

Este método siempre tiene acceso al primer nivel de mip. Para especificar otros niveles de mip, use el [**método \[ \] \[ \] mip.operator**](sm5-object-texture1darray-mipsoperatorindex.md) en su lugar.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




