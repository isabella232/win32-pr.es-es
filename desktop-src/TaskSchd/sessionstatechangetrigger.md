---
title: Objeto SessionStateChangeTrigger
description: Objeto de scripting que desencadena tareas de conexión o desconexión de la consola, conexión remota o desconexión, o notificaciones de bloqueo o desbloqueo de la estación de trabajo.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Objeto SessionStateChangeTrigger Programador de tareas
- Programador de tareas de objeto SessionStateChangeTrigger, descrito
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676651"
---
# <a name="sessionstatechangetrigger-object"></a>Objeto SessionStateChangeTrigger

Objeto de scripting que desencadena tareas de conexión o desconexión de la consola, conexión remota o desconexión, o notificaciones de bloqueo o desbloqueo de la estación de trabajo.

## <a name="members"></a>Miembros

El objeto **SessionStateChangeTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **SessionStateChangeTrigger** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso           | Descripción                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](sessionstatechangetrigger-delay.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.<br/>                                         |
| [**habilitado**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                              |
| [**EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/>               |
| [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                                 |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                                             |
| [**Repetición**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor que indica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el tipo de cambio de sesión de Terminal Server que desencadenaría un inicio de tarea.<br/>                                                                                                      |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                                            |
| [**Deberían**](sessionstatechangetrigger-userid.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el usuario para la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.<br/>                                                               |



 

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, se especifica un desencadenador de cambio de estado de sesión mediante el elemento [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





