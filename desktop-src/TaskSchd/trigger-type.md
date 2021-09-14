---
title: Propiedad Trigger.Type
description: Para el scripting, obtiene el tipo del desencadenador.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Tipo de propiedad Programador de tareas
- Propiedad type Programador de tareas , Trigger object
- Desencadenador de objetos Programador de tareas , propiedad Type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891412"
---
# <a name="triggertype-property"></a>Propiedad Trigger.Type

Para el scripting, obtiene el tipo del desencadenador. El tipo de desencadenador se define cuando se crea el desencadenador y no se puede cambiar más adelante. Para obtener información sobre cómo crear un desencadenador, [**vea TriggerCollection.Create**](triggercollection-create.md).

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valor de propiedad

Uno de los siguientes valores [**de \_ enumeración TASK TRIGGER \_ TYPE2.**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)



| Value                                                                                                                                                                                                                                                                                | Significado                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**TASK \_ TRIGGER \_ EVENT**</dt> <dt>0</dt> </dl>                                                 | Inicia la tarea cuando se produce un evento específico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**TASK \_ TIEMPO \_ DE DESENCADENADOR**</dt> <dt>1</dt> </dl>                                                    | Inicia la tarea a una hora específica del día.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**TASK \_ DESENCADENADOR \_ DIARIO**</dt> <dt>2</dt> </dl>                                                 | Inicia la tarea diariamente.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**TASK \_ TRIGGER \_ WEEKLY**</dt> <dt>3</dt> </dl>                                              | Inicia la tarea semanalmente.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**TASK \_ DESENCADENADOR \_ MENSUAL**</dt> <dt>4</dt> </dl>                                           | Inicia la tarea mensualmente.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**TASK \_ TRIGGER \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Inicia la tarea cada mes en un día específico de la semana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**TASK \_ TRIGGER \_ IDLE**</dt> <dt>6</dt> </dl>                                                    | Inicia la tarea cuando el equipo entra en un estado inactivo.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**TASK \_ REGISTRO \_ DE DESENCADENADOR**</dt> <dt>7</dt> </dl>                            | Inicia la tarea cuando se registra la tarea.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**TASK \_ TRIGGER \_ BOOT**</dt> <dt>8</dt> </dl>                                                    | Inicia la tarea cuando se inicia el equipo.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**TASK \_ DESENCADENAR \_ INICIO DE SESIÓN**</dt> <dt>9</dt> </dl>                                                 | Inicia la tarea cuando un usuario específico inicia sesión.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**TASK \_ DESENCADENAR \_ CAMBIO DE ESTADO DE \_ \_ SESIÓN**</dt> <dt>11</dt> </dl> | Desencadena la tarea cuando cambia un estado de sesión específico.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> <dt>

[**TASK \_ TRIGGER \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





