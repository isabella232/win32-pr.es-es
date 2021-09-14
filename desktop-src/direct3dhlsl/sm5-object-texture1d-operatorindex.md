---
title: Función Texture1D::Operator
description: Devuelve una variable de recurso de solo lectura para texture1D.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966547"
---
# <a name="texture1doperator--function"></a>Función Texture1D::Operator

Devuelve una variable de recurso de solo lectura para [**texture1D.**](sm5-object-texture1d.md)

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint**

Posición del índice. Contiene la coordenada X.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Una variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

Este método siempre tiene acceso al primer nivel de mip. Para especificar otros niveles de mip, use en su lugar [**\[ \] \[ \] mip.operator.**](sm5-object-texture1d-mipsoperatorindex.md)

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




