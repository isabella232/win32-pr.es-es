---
title: FUNCIÓN RWByteAddressBuffer::GetDimensions
description: Obtiene la longitud del búfer. | FUNCIÓN RWByteAddressBuffer::GetDimensions
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
keywords:
- Función GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2271f563251cfdb9c6f2a2174c91dc8c271c7354a2b10b9b2e7e55cb4af09d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725150"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>FUNCIÓN RWByteAddressBuffer::GetDimensions

Obtiene la longitud del búfer.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

Tipo: **uint**

Longitud, en bytes, del búfer.

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

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




