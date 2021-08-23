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
ms.openlocfilehash: 8302f31cd07b81f4f78abe6a0a1fbcb2e6a1028f6153da69e55e0fb34977b585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671395"
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

## <a name="remarks"></a>Comentarios

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

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

