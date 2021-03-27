---
title: 'RWByteAddressBuffer:: Load3 (uint) (función)'
description: 'Obtiene tres valores. | RWByteAddressBuffer:: Load3 (uint) (función)'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Load3 de función HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986731"
---
# <a name="rwbyteaddressbufferload3uint-function"></a>RWByteAddressBuffer:: Load3 (uint) (función)

Obtiene tres valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint3 Load3(
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

Tipo: **UInt3**

Tres valores.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load3](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




