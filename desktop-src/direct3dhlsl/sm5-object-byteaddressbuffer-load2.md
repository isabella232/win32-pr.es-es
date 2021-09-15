---
title: Función ByteAddressBuffer::Load2(uint)
description: Obtiene dos valores. | Función ByteAddressBuffer::Load2(uint)
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Función Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566588"
---
# <a name="byteaddressbufferload2uint-function"></a>Función ByteAddressBuffer::Load2(uint)

Obtiene dos valores.

## <a name="syntax"></a>Sintaxis

``` syntax
uint2 Load2(
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

Tipo: **uint2**

Dos valores.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




