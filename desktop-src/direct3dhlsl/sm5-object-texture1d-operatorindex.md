---
title: 'Texture1D:: Operator (función)'
description: Devuelve una variable de recurso de solo lectura para un Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149811"
---
# <a name="texture1doperator--function"></a>Texture1D:: Operator (función)

Devuelve una variable de recurso de solo lectura para un [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint**

Posición de índice. Contiene la coordenada x.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

Este método siempre tiene acceso al primer nivel de MIP. Para especificar otros niveles de MIP, utilice en su lugar el [**\[ \] \[ \] operador MIP.**](sm5-object-texture1d-mipsoperatorindex.md)

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




