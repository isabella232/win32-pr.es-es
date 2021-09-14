---
title: StructuredBuffer::Operator (Función)
description: Devuelve una variable de recurso de solo lectura de StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963532"
---
# <a name="structuredbufferoperator--function"></a>StructuredBuffer::Operator (Función)

Devuelve una variable de recurso de solo lectura de [**structuredBuffer.**](sm5-object-structuredbuffer.md)

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

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




