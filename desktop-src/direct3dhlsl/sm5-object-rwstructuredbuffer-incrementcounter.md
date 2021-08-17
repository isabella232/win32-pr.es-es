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
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095175"
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

## <a name="remarks"></a>Comentarios

La vista de acceso sin ordenar enlazada debe tener [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) establecido durante la creación para que este método funcione.

Un recurso estructurado se puede indexar aún más en función de los nombres de componente de las estructuras.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

