---
title: ByteAddressBuffer::GetDimensions (Función)
description: Obtiene la longitud del búfer. | ByteAddressBuffer::GetDimensions (Función)
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573624"
---
# <a name="byteaddressbuffergetdimensions-function"></a>ByteAddressBuffer::GetDimensions (Función)

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

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[ByteAddressBuffer](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




