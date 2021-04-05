---
title: Objeto MonthlyDOWTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea en una programación mensual de día de la semana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- Programador de tareas de desencadenador de DOW mensual, objeto
- Objeto MonthlyDOWTrigger Programador de tareas
- Programador de tareas de objeto MonthlyDOWTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079162"
---
# <a name="monthlydowtrigger-object"></a>Objeto MonthlyDOWTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea en una programación mensual de día de la semana. Por ejemplo, la tarea se inicia el primer jueves, de mayo a octubre.

## <a name="members"></a>Miembros

El objeto **MonthlyDOWTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **MonthlyDOWTrigger** tiene estas propiedades.



| Propiedad                                                                          | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece los días de la semana en los que se ejecuta la tarea.<br/>                                                                                                                    |
| [**habilitado**](trigger-enabled.md)<br/>                                     | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                                 | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que se permite la ejecución de la tarea iniciada por este desencadenador.<br/>                          |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece los meses del año en los que se ejecuta la tarea.<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                               | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se ejecuta en la última semana del mes.<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece las semanas del mes en las que se ejecuta la tarea.<br/>                                                                                                                  |



 

## <a name="remarks"></a>Observaciones

La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .

Al leer o escribir XML para una tarea, se especifica un desencadenador de día de la semana mensual mediante el elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Activado**](trigger.md)
</dt> <dt>

[Objetos Programador de tareas](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





