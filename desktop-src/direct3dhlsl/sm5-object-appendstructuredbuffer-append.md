---
title: 'AppendStructuredBuffer:: Append (función)'
description: Anexa un valor al final del búfer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Anexar la función HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103994791"
---
# <a name="append-function"></a>Append (función)

Anexa un valor al final del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ninguno

## <a name="remarks"></a>Observaciones

T puede ser cualquier tipo de datos, incluidas las estructuras.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




