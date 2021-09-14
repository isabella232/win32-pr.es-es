---
title: Función RWStructuredBuffer::IncrementCounter (Httpserv.h)
description: Incrementa el contador oculto del objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Función IncrementCounter HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174709"
---
# <a name="incrementcounter-function"></a>Función IncrementCounter

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

La vista de acceso no ordenado enlazada debe tener [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) establecido durante la creación para que este método funcione.

Un recurso estructurado se puede indexar aún más en función de los nombres de componente de las estructuras.

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

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

