---
title: Propiedad SessionStateChangeTrigger.StateChange
description: Para el scripting, obtiene o establece el tipo de cambio de sesión de Terminal Server que desencadenaría el inicio de una tarea.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Propiedad StateChange Programador de tareas
- Propiedad StateChange Programador de tareas , objeto SessionStateChangeTrigger
- Objeto SessionStateChangeTrigger Programador de tareas , propiedad StateChange
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
ms.openlocfilehash: cfbd2037f19ca2d9fe8ec5d0ba046e69894f431b81d623b61b9474515bcef3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100165"
---
# <a name="sessionstatechangetriggerstatechange-property"></a>Propiedad SessionStateChangeTrigger.StateChange

Para el scripting, obtiene o establece el tipo de cambio de sesión de Terminal Server que desencadenaría el inicio de una tarea.

## <a name="syntax"></a>Syntax


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a>Valor de propiedad

Tipo de cambio de sesión de Terminal Server que desencadena el inicio de una tarea.

Los valores posibles son de la [**enumeración TASK \_ SESSION STATE \_ CHANGE \_ \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type)



| Value                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <dt>**TASK \_ CONSOLE \_ CONNECT**</dt> <dt>1</dt> </dl>          | Cambio del estado de conexión de la consola de Terminal Server. Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo. <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <dt>**TASK \_ \_DESCONEXIÓN DE LA**</dt> CONSOLA <dt>2</dt> </dl> | Cambio de estado de desconexión de la consola de Terminal Server. Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.<br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <dt>**TASK \_ CONEXIÓN \_ REMOTA**</dt> <dt>3</dt> </dl>             | Cambio de estado de conexión remota de Terminal Server. Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa Conexión a Escritorio remoto desde un equipo remoto.<br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <dt>**TASK \_ REMOTE \_ DISCONNECT**</dt> <dt>4</dt> </dl>    | Cambio de estado de desconexión remota de Terminal Server. Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa Conexión a Escritorio remoto programa desde un equipo remoto.<br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <dt>**TASK \_ BLOQUEO \_ DE SESIÓN**</dt> <dt>7</dt> </dl>                   | Cambio de estado bloqueado de sesión de Terminal Server. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado. <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <dt>**TASK \_ DESBLOQUEO \_ DE SESIÓN**</dt> <dt>8</dt> </dl>             | Cambio de estado desbloqueado de sesión de Terminal Server. Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está desbloqueado.<br/>                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





