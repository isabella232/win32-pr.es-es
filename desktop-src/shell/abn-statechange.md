---
description: Notifica a una Appbar que el estado de ocultar automáticamente o siempre en la barra de tareas ha cambiado&\# 8212; es decir, el usuario ha seleccionado o desactivado el &\# 0034; Siempre visible&\# 0034 o &\# 0034; Ocultar automáticamente&\# 0034; en la hoja de propiedades de la barra de tareas.
title: Mensaje de ABN_STATECHANGE (ShellAPI. h)
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
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907733"
---
# <a name="abn_statechange-message"></a>Mensaje de ABN. \_

Notifica a una Appbar que el estado de ocultación automática o siempre visible de la barra de tareas ha cambiado es decir, el usuario ha activado o desactivado la casilla "siempre visible" o "ocultar automáticamente" en la hoja de propiedades de la barra de tareas.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un Appbar puede usar este mensaje de notificación para establecer su estado de conformidad con el de la barra de tareas, si lo desea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




