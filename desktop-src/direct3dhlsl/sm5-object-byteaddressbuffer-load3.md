---
title: Función ByteAddressBuffer::Load3(uint)
description: Obtiene tres valores. | Función ByteAddressBuffer::Load3(uint)
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Función Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063696"
---
# <a name="byteaddressbufferload3uint-function"></a>Función ByteAddressBuffer::Load3(uint)

Obtiene tres valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*address* \[ En\]
</dt> <dd>

Tipo: **uint**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint3**

Tres valores.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




