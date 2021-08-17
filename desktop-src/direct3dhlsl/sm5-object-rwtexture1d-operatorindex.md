---
title: RWTexture1D::Operator (Función)
description: Devuelve una variable de recurso. | RWTexture1D::Operator (Función)
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: a6f338efd27573a86c661df36f9fc0e9906814bf15c1cc5d2d6c478a17f83a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724858"
---
# <a name="rwtexture1doperator--function"></a>RWTexture1D::Operator (Función)

Devuelve una variable de recurso.

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

Posición del índice. Contiene la coordenada x.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Una variable de recurso.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




