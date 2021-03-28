---
title: 'Texture2DArray:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2DArray:: Operator (función)'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083618"
---
# <a name="texture2darrayoperator--function"></a>Texture2DArray:: Operator (función)

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **UInt3**

Posición de índice. Los componentes primero y segundo contienen las coordenadas (x, y). El tercer componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

Este método siempre tiene acceso al primer nivel de MIP. Para especificar otros niveles de MIP, utilice en su lugar el método [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2darray-mipsoperatorindex.md) .

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




