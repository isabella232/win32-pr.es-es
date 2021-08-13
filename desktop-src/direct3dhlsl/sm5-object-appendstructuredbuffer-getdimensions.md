---
title: Función AppendStructuredBuffer::GetDimensions
description: Obtiene las dimensiones de recursos. | Función AppendStructuredBuffer::GetDimensions
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Función GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790656"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>Función AppendStructuredBuffer::GetDimensions

Obtiene las dimensiones de recursos.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*numStructs* \[ out\]
</dt> <dd>

Tipo: **uint**

Número de estructuras.

</dd> <dt>

*stride* \[ out\]
</dt> <dd>

Tipo: **uint**

Número de bytes de cada elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




