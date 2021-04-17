---
title: TriggerCollection. Create (método)
description: En el caso de scripting, crea un nuevo desencadenador para la tarea.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- desencadenadores Programador de tareas, crear
- Crear método Programador de tareas
- Create Method Programador de tareas, TriggerCollection Object
- Programador de tareas de objeto TriggerCollection, Create (método)
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676677"
---
# <a name="triggercollectioncreate-method"></a>TriggerCollection. Create (método)

En el caso de scripting, crea un nuevo desencadenador para la tarea.

## <a name="syntax"></a>Sintaxis


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Este parámetro se establece en una de las constantes de enumeración [**\_ \_ tipo2 de desencadenador de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) siguiente.



| Value                                                                                                                                                                                                                                                                                | Significado                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ evento**</dt> <dt>0</dt> </dl>                                                 | Desencadena la tarea cuando se produce un evento específico.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Tarea \_ de \_Hora del desencadenador**</dt> <dt>1</dt> </dl>                                                    | Desencadena la tarea a una hora específica del día.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ diariamente**</dt> <dt>2</dt> </dl>                                                 | Desencadena la tarea según una programación diaria. Por ejemplo, la tarea se inicia a una hora específica cada día, cada día, cada tres días, etc.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ semanalmente**</dt> <dt>3</dt> </dl>                                              | Desencadena la tarea según una programación semanal. Por ejemplo, la tarea comienza a las 8:00 A.M. de un día específico cada semana u otra semana.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ mensualmente**</dt> <dt>4</dt> </dl>                                           | Desencadena la tarea según una programación mensual. Por ejemplo, la tarea se inicia en días específicos de meses específicos.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Tarea \_ de DESENCADENAdor \_ MONTHLYDOW**</dt> <dt>5</dt> </dl>                                  | Desencadena la tarea en una programación mensual de día de la semana. Por ejemplo, la tarea se inicia en un determinado día de la semana, las semanas del mes y los meses del año.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Tarea \_ de DESENCADENAdor \_ inactivo**</dt> <dt>6</dt> </dl>                                                    | Desencadena la tarea cuando el equipo entra en un estado de inactividad.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ registro**</dt> <dt>7</dt> </dl>                            | Desencadena la tarea cuando se registra la tarea.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Tarea \_ de DESENCADENAdor de \_ arranque**</dt> <dt>8</dt> </dl>                                                    | Desencadena la tarea cuando se inicia el equipo.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Tarea \_ de DESENCADENAr \_ Inicio de sesión**</dt> <dt>9</dt> </dl>                                                 | Desencadena la tarea cuando un usuario específico inicia sesión.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Tarea \_ de \_Cambio de \_ estado \_ de sesión de desencadenador**</dt> <dt>11</dt> </dl> | Desencadena la tarea cuando cambia un estado de sesión específico.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**desencadenador**](trigger.md) que representa el nuevo desencadenador.

## <a name="remarks"></a>Observaciones

Para obtener información acerca de cada tipo de desencadenador, consulte [tipos de desencadenador](trigger-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**Activado**](trigger.md)
</dt> </dl>

 

 





