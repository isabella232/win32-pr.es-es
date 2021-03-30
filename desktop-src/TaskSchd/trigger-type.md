---
title: Trigger. Type (propiedad)
description: En el caso de scripting, obtiene el tipo del desencadenador.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Propiedad Type Programador de tareas
- Propiedad de tipo Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad Type
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801742"
---
# <a name="triggertype-property"></a>Trigger. Type (propiedad)

En el caso de scripting, obtiene el tipo del desencadenador. El tipo de desencadenador se define cuando se crea el desencadenador y no se puede cambiar más adelante. Para obtener información sobre cómo crear un desencadenador, vea [**TriggerCollection. Create**](triggercollection-create.md).

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Valor de propiedad

Uno de los siguientes valores de enumeración [**\_ \_ tipo2 del desencadenador de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .



| Value                                                                                                                                                                                                                                                                                | Significado                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ evento**</dt> <dt>0</dt> </dl>                                                 | Inicia la tarea cuando se produce un evento específico.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tarea \_ de \_Hora del desencadenador**</dt> <dt>1</dt> </dl>                                                    | Inicia la tarea a una hora específica del día.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ diariamente**</dt> <dt>2</dt> </dl>                                                 | Inicia la tarea diariamente.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ semanalmente**</dt> <dt>3</dt> </dl>                                              | Inicia la tarea semanalmente.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ mensualmente**</dt> <dt>4</dt> </dl>                                           | Inicia la tarea mensualmente.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tarea \_ de DESENCADENAdor \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Inicia la tarea cada mes en un determinado día de la semana.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tarea \_ de DESENCADENAdor \_ inactivo**</dt> <dt>6</dt> </dl>                                                    | Inicia la tarea cuando el equipo entra en un estado de inactividad.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ registro**</dt> <dt>7</dt> </dl>                            | Inicia la tarea cuando se registra la tarea.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tarea \_ de DESENCADENAdor de \_ arranque**</dt> <dt>8</dt> </dl>                                                    | Inicia la tarea cuando se inicia el equipo.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ Inicio de sesión**</dt> <dt>9</dt> </dl>                                                 | Inicia la tarea cuando un usuario específico inicia sesión.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tarea \_ de \_Cambio de \_ estado \_ de sesión de desencadenador**</dt> <dt>11</dt> </dl> | Desencadena la tarea cuando cambia un estado de sesión específico.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> <dt>

[**\_Tipo2 de desencadenador de tarea \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





