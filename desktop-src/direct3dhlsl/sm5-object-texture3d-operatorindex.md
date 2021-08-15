---
title: Función Texture3D::Operator
description: Devuelve una variable de recurso de solo lectura. | Función Texture3D::Operator
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: d701e5f9ba46d17c305fda0a936700e10a1348440e55c913537f2a2d00a5c57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985705"
---
# <a name="texture3doperator--function"></a>Función Texture3D::Operator

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint3**

Posición del índice. Contiene las coordenadas (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

Este método siempre tiene acceso al primer nivel de mip. Para especificar otros niveles de mip, use [**el operador \[ \] \[ \] mip.operator**](sm5-object-texture3d-mipsoperatorindex.md) en su lugar.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




