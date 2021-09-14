---
title: Función RWStructuredBuffer::D ecrementCounter (Httpserv.h)
description: Disminuye el contador oculto del objeto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- Función HLSL de DecrementCounter
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174713"
---
# <a name="decrementcounter-function"></a>Función DecrementCounter

Disminuye el contador oculto del objeto.

## <a name="syntax"></a>Sintaxis

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Valor del contador posterior al decrementado.

## <a name="remarks"></a>Observaciones

La vista de acceso no ordenado enlazada debe tener [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) establecido durante la creación para que este método funcione.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

