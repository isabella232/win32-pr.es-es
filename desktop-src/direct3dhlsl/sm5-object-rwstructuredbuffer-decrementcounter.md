---
title: RWStructuredBuffer::D función ecrementCounter (Httpserv. h)
description: Disminuye el contador oculto del objeto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter de función HLSL
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987061"
---
# <a name="decrementcounter-function"></a>DecrementCounter función)

Disminuye el contador oculto del objeto.

## <a name="syntax"></a>Sintaxis

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Valor del contador posterior a la disminución.

## <a name="remarks"></a>Observaciones

La vista de acceso desordenado enlazada debe tener establecido el [**\_ contador D3D11 buffer \_ UAV \_ Flag \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) durante creationfor para que este método funcione.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Httpserv. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

