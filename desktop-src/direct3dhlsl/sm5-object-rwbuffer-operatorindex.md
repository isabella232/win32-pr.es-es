---
title: RWBuffer::Operator (Función)
description: Devuelve una variable de recurso. | RWBuffer::Operator (Función)
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963580"
---
# <a name="rwbufferoperator--function"></a>RWBuffer::Operator (Función)

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

Posición del índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




