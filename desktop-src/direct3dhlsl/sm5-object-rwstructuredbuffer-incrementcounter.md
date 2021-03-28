---
title: 'RWStructuredBuffer:: IncrementCounter (función) (Httpserv. h)'
description: Incrementa el contador oculto del objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter de función HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362698"
---
# <a name="incrementcounter-function"></a>IncrementCounter función)

Incrementa el contador oculto del objeto.

## <a name="syntax"></a>Sintaxis

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Valor del contador previamente incrementado.

## <a name="remarks"></a>Observaciones

La vista de acceso desordenado enlazada debe tener establecido el [**contador D3D11 de \_ búfer \_ UAV \_ \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) en el conjunto de búferes de la creación para que este método funcione.

Un recurso estructurado se puede indexar más en función de los nombres de componente de las estructuras.

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

 

