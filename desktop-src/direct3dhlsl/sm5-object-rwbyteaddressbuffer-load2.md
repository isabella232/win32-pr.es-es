---
title: 'RWByteAddressBuffer:: Load2 (uint) (función)'
description: 'Obtiene dos valores. | RWByteAddressBuffer:: Load2 (uint) (función)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2 de función HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986701"
---
# <a name="rwbyteaddressbufferload2uint-function"></a>RWByteAddressBuffer:: Load2 (uint) (función)

Obtiene dos valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint2 Load2(
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

Tipo: **uint2**

Dos valores.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load2](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




