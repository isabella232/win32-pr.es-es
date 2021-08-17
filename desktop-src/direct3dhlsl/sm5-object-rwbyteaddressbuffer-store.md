---
title: RWByteAddressBuffer::Store (Función)
description: Establece un valor.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Almacenar la función HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be699a28eea213b8847f32a3b66f53739a7db86ee5964bd97559a6d534fff6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724947"
---
# <a name="store-function"></a>Función Store

Establece un valor.

## <a name="syntax"></a>Sintaxis

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*address* \[ En\]
</dt> <dd>

Tipo: **uint**

Dirección de entrada en bytes, que debe ser un múltiplo de 4.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **uint**

Un valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




