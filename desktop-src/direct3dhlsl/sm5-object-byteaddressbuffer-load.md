---
title: 'ByteAddressBuffer:: Load (int) (función)'
description: 'Obtiene un valor. | ByteAddressBuffer:: Load (int) (función)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998060"
---
# <a name="byteaddressbufferloadint-function"></a>ByteAddressBuffer:: Load (int) (función)

Obtiene un valor.

## <a name="syntax"></a>Sintaxis

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección* \[ de de\]
</dt> <dd>

Tipo: **int**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Un valor.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cargar métodos](byteaddressbuffer-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




