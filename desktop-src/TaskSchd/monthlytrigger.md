---
title: Objeto MonthlyTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación mensual.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Programador de tareas de desencadenador mensual, objeto
- Objeto MonthlyTrigger Programador de tareas
- Programador de tareas de objeto MonthlyTrigger, descrito
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802563"
---
# <a name="monthlytrigger-object"></a>Objeto MonthlyTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación mensual. Por ejemplo, la tarea se inicia en días específicos de meses específicos.

## <a name="members"></a>Miembros

El objeto **MonthlyTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **MonthlyTrigger** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece los días del mes durante los que se ejecuta la tarea.<br/>                                                                                                                   |
| [**habilitado**](trigger-enabled.md)<br/>                                | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                            | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que puede ejecutarse la tarea iniciada por el desencadenador.<br/>                           |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece los meses del año en los que se ejecuta la tarea.<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                          | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se ejecuta el último día del mes.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Observaciones

La hora del día en que se inicia la tarea se establece mediante la propiedad [**StartBoundary**](trigger-startboundary.md) .

Al leer o escribir su propio XML para una tarea, se especifica un desencadenador mensual mediante el elemento [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) del esquema de programador de tareas.

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

 

 





