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
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510015"
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

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




