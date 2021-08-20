---
description: Notifica&una barra de aplicaciones que el estado de la barra de tareas ha cambiado&8212; es decir, el usuario ha seleccionado o borrado el &\# \# 0034; Siempre en la parte superior&\# 0034; o &\# 0034; Ocultar automáticamente&\# 0034; casilla en la hoja de propiedades de la barra de tareas.
title: ABN_STATECHANGE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0017930bd3cf4c8cba356206cfa2207df04ea9c203018703a5f3064d0abb11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861587"
---
# <a name="abn_statechange-message"></a>Mensaje ABN \_ STATECHANGE

Notifica a una barra de aplicaciones que el estado de mostrar automáticamente o siempre en la parte superior de la barra de tareas ha cambiado, es decir, el usuario ha seleccionado o desactivado la casilla "Siempre en la parte superior" u "Ocultar automáticamente" en la hoja de propiedades de la barra de tareas.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una barra de aplicaciones puede usar este mensaje de notificación para establecer su estado para que se ajuste al de la barra de tareas, si lo desea.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




