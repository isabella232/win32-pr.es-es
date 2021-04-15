---
title: 'Texture2D:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2D:: Operator (función)'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986511"
---
# <a name="texture2doperator--function"></a>Texture2D:: Operator (función)

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint2**

Posición de índice. Contiene las coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

Este método siempre tiene acceso al primer nivel de MIP. Para especificar otros niveles de MIP, utilice en su lugar el método [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) .

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




