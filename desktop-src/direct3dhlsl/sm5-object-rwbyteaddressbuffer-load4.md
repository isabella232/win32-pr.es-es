---
title: 'RWByteAddressBuffer:: Load4 (uint) (función)'
description: 'Obtiene cuatro valores. | RWByteAddressBuffer:: Load4 (uint) (función)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4 de función HLSL
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986724"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>RWByteAddressBuffer:: Load4 (uint) (función)

Obtiene cuatro valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección* \[ de de\]
</dt> <dd>

Tipo: **uint**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint4**

Cuatro valores.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




