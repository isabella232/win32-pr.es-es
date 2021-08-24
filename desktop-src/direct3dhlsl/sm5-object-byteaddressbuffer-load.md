---
title: Función ByteAddressBuffer::Load(int)
description: Obtiene un valor. | Función ByteAddressBuffer::Load(int)
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
ms.openlocfilehash: 7a9854f85ebd92b9f57e4b2339f374ad8f7816ea7b9ba31e37c9404b08c14864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671455"
---
# <a name="byteaddressbufferloadint-function"></a>Función ByteAddressBuffer::Load(int)

Obtiene un valor.

## <a name="syntax"></a>Sintaxis

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*address* \[ En\]
</dt> <dd>

Tipo: **int**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Un valor.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de carga](byteaddressbuffer-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




