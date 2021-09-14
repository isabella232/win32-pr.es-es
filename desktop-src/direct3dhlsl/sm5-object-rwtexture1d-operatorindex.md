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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974670"
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

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




