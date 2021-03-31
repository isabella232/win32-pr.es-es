---
title: Propiedad SessionStateChangeTrigger. StateChange
description: Para scripting, obtiene o establece el tipo de Terminal Server cambio de sesión que desencadenaría un inicio de tarea.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Propiedad StateChange Programador de tareas
- Propiedad StateChange Programador de tareas, objeto SessionStateChangeTrigger
- Programador de tareas de objeto SessionStateChangeTrigger, propiedad StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801610"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Propiedad SessionStateChangeTrigger. StateChange

Para scripting, obtiene o establece el tipo de Terminal Server cambio de sesión que desencadenaría un inicio de tarea.

## <a name="syntax"></a>Sintaxis


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valor de propiedad

El tipo de Terminal Server cambio de sesión que desencadena la ejecución de una tarea.

Los valores posibles proceden de la enumeración de [**tipo de cambio de estado de sesión de tarea \_ \_ \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .



| Value                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**Tarea \_ de \_Conexión**</dt> de la consola <dt>1</dt> </dl>          | Terminal Server cambio del estado de conexión de la consola. Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**Tarea \_ de \_Desconexión**</dt> de la consola <dt>2</dt> </dl> | Terminal Server cambio de estado de desconexión de la consola. Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**Tarea \_ de \_Conexión remota**</dt> <dt>3</dt> </dl>             | Terminal Server cambio de estado de la conexión remota. Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa de Conexión a Escritorio remoto desde un equipo remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**Tarea \_ de \_Desconexión remota**</dt> <dt>4</dt> </dl>    | Terminal Server cambio de estado de desconexión remota. Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa el programa Conexión a Escritorio remoto desde un equipo remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**Tarea \_ de \_Bloqueo de sesión**</dt> <dt>7</dt> </dl>                   | Terminal Server cambio de estado de la sesión bloqueada. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**Tarea \_ de \_Desbloqueo de sesión**</dt> <dt>8</dt> </dl>             | Terminal Server cambio de estado desbloqueado de la sesión. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando se desbloquea el equipo.<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





