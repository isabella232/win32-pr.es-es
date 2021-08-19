---
title: AppendStructuredBuffer::Append (Función)
description: Anexa un valor al final del búfer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Función append HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725399"
---
# <a name="append-function"></a>Función Append

Anexa un valor al final del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno

## <a name="remarks"></a>Observaciones

T puede ser cualquier tipo de datos, incluidas las estructuras.

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

 

 




