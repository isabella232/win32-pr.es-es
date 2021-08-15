---
title: RWTexture3D::Operator (Función)
description: Devuelve una variable de recurso de RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: 8db7073ef20976ecb6c39839d5639a1f0fcfe1fad765c2cf9b0ecdf086622b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509141"
---
# <a name="rwtexture3doperator--function"></a>RWTexture3D::Operator (Función)

Devuelve una variable de recurso de [**RWTexture3D.**](sm5-object-rwtexture3d.md)

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

Variable de recurso.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




