---
title: Objeto MonthlyDOWTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea según una programación mensual del día de la semana.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- desencadenador DOW mensual Programador de tareas , objeto
- Objeto MonthlyDOWTrigger Programador de tareas
- Objeto MonthlyDOWTrigger Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170677"
---
# <a name="monthlydowtrigger-object"></a>Objeto MonthlyDOWTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea según una programación mensual del día de la semana. Por ejemplo, la tarea se inicia cada primer jueves, de mayo a octubre.

## <a name="members"></a>Members

El **objeto MonthlyDOWTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto MonthlyDOWTrigger** tiene estas propiedades.



| Propiedad                                                                          | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](monthlydowtrigger-daysofweek.md)<br/>                     | Lectura y escritura<br/> | Obtiene o establece los días de la semana durante los que se ejecuta la tarea.<br/>                                                                                                                    |
| [**Enabled**](trigger-enabled.md)<br/>                                     | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                                 | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>               | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por este desencadenador puede ejecutarse.<br/>                          |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**MonthsOfYear**](monthlydowtrigger-monthsofyear.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece los meses del año durante los que se ejecuta la tarea.<br/>                                                                                                                  |
| [**RandomDelay**](monthlydowtrigger-randomdelay.md)<br/>                   | Lectura y escritura<br/> | Obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                               | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**RunOnLastWeekOfMonth**](monthlydowtrigger-runonlastweekofmonth.md)<br/> | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se ejecuta en la última semana del mes.<br/>                                                                                    |
| [**StartBoundary**](trigger-startboundary.md)<br/>                         | Lectura y escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                              |
| [**WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md)<br/>                 | Lectura y escritura<br/> | Obtiene o establece las semanas del mes durante las que se ejecuta la tarea.<br/>                                                                                                                  |



 

## <a name="remarks"></a>Observaciones

La hora del día en que se inicia la tarea se establece mediante [**la propiedad StartBoundary.**](trigger-startboundary.md)

Al leer o escribir XML para una tarea, se especifica un desencadenador del día de la semana mensual mediante el elemento [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) del esquema Programador de tareas semana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Detonante**](trigger.md)
</dt> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





