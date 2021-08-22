---
title: WeeklyTrigger, objeto
description: Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación semanal.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- desencadenador semanal Programador de tareas , objeto
- Objetos WeeklyTrigger Programador de tareas
- Objeto WeeklyTrigger Programador de tareas , descrito
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51eb48b03efb49bd5642909af4b99b99bfb1f7f139b97f8410e0d5f014843ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001823"
---
# <a name="weeklytrigger-object"></a>WeeklyTrigger, objeto

Objeto de scripting que representa un desencadenador que inicia una tarea basada en una programación semanal. Por ejemplo, la tarea comienza a las 8:00 a. m. en un día específico de la semana cada semana o cada dos semanas.

## <a name="members"></a>Miembros

El **objeto WeeklyTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto WeeklyTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece los días de la semana en los que se ejecuta la tarea.<br/>                                                                                                                        |
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la cantidad máxima de tiempo que la tarea iniciada por el desencadenador puede ejecutarse.<br/>                           |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece el identificador del desencadenador.<br/>                                                                               |
| [**RandomDelay**](weeklytrigger-randomdelay.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.<br/>                                                                                               |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Se hereda del [**objeto Trigger.**](trigger.md) Obtiene el tipo del desencadenador.<br/>                                                                                              |
| [**WeeksInterval**](weeklytrigger-weeksinterval.md)<br/>     | Lectura/escritura<br/> | Obtiene o establece el intervalo entre las semanas de la programación.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

La hora del día en que se inicia la tarea se establece mediante [**la propiedad StartBoundary.**](trigger-startboundary.md)

Al leer o escribir su propio XML para una tarea, se especifica un desencadenador semanal mediante el [**elemento ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) del esquema Programador de tareas trabajo.

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo de código para este objeto de scripting, vea Ejemplo de desencadenador [semanal (scripting).](weekly-trigger-example--scripting-.md)

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

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection.Create**](triggercollection-create.md)
</dt> </dl>

 

 





