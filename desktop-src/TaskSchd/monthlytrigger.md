---
title: Objeto MonthlyTrigger
description: Objeto de scripting que representa un desencadenador que inicia una tarea según una programación mensual.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- desencadenador mensual Programador de tareas , objeto
- Objetos MonthlyTrigger Programador de tareas
- Objeto MonthlyTrigger Programador de tareas , descrito
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
ms.openlocfilehash: 078ecf023bd66fb0ad92b87f6dcc16978166fd7c6b3bbfce6d9b971f19b87be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760072"
---
# <a name="monthlytrigger-object"></a>Objeto MonthlyTrigger

Objeto de scripting que representa un desencadenador que inicia una tarea según una programación mensual. Por ejemplo, la tarea se inicia en días específicos de meses específicos.

## <a name="members"></a>Miembros

El **objeto MonthlyTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto MonthlyTrigger** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece los días del mes durante los que se ejecuta la tarea.<br/>                                                                                                                   |
| [**habilitado**](trigger-enabled.md)<br/>                                | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [EndBoundary](trigger-endboundary.md)<br/>                            | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/>          | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**MonthsOfYear**](monthlytrigger-monthsofyear.md)<br/>               | Lectura/escritura<br/> | Obtiene o establece los meses del año durante los que se ejecuta la tarea.<br/>                                                                                                                  |
| [**RandomDelay**](monthlytrigger-randomdelay.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                          | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**RunOnLastDayOfMonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se ejecuta el último día del mes.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                              |



 

## <a name="remarks"></a>Comentarios

La hora del día en que se inicia la tarea se establece mediante [**la propiedad StartBoundary.**](trigger-startboundary.md)

Al leer o escribir su propio XML para una tarea, se especifica un desencadenador mensual mediante el [**elemento ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) del esquema Programador de tareas datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**detonante**](trigger.md)
</dt> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





