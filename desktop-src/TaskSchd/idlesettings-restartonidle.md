---
title: IdleSettings.RestartOnIdle, propiedad
description: Para el scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo pasa a una condición de inactividad más de una vez.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Propiedad RestartOnIdle Programador de tareas
- Propiedad RestartOnIdle Programador de tareas , objeto IdleSettings
- Objeto IdleSettings Programador de tareas , propiedad RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa405ce4090a080106ec030acbe0ca7211b1c6f94e5874729226ce6adfafa652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760092"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings.RestartOnIdle, propiedad

Para el scripting, obtiene o establece un valor booleano que indica si la tarea se reinicia cuando el equipo pasa a una condición de inactividad más de una vez.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Valor booleano que indica si la tarea debe reiniciarse cuando el equipo se convierte en una condición inactiva más de una vez. El valor predeterminado es False.

## <a name="remarks"></a>Comentarios

Esta propiedad solo se usa si la [**propiedad IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) está establecida en True.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





