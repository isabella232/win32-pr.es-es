---
title: Función RWByteAddressBuffer::Store3
description: Establece tres valores.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Función HlSL de Store3
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a752ada16db4800e6160ad7b1c2c0b480deee75ff760d0c7f270dac36d1cff51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790067"
---
# <a name="store3-function"></a>Función Store3

Establece tres valores.

## <a name="syntax"></a>Sintaxis

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*address* \[ En\]
</dt> <dd>

Tipo: **uint**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> <dt>

*valores* \[ En\]
</dt> <dd>

Tipo: **uint3**

Tres valores de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




