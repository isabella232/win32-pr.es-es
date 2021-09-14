---
title: Función RWByteAddressBuffer::Load4(uint)
description: Obtiene cuatro valores. | Función RWByteAddressBuffer::Load4(uint)
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Función Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884116"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>Función RWByteAddressBuffer::Load4(uint)

Obtiene cuatro valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint4 Load4(
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

Tipo: **uint4**

Cuatro valores.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




