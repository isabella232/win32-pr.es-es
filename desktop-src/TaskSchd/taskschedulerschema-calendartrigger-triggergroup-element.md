---
title: Elemento CalendarTrigger (triggerGroup)
description: Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- desencadenador de calendario Programador de tareas elemento , XML
- Elemento CalendarTrigger Programador de tareas
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516975"
---
# <a name="calendartrigger-triggergroup-element"></a>Elemento CalendarTrigger (triggerGroup)

Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

El **elemento CalendarTrigger** se define mediante el [**tipo complejo calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                            | Tipo                                                                                                 | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Especifica la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Especifica la cantidad máxima de tiempo en la que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)                             | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Especifica una programación diaria.<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Especifica una programación mensual.<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo según una programación mensual del día de la semana.<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Especifica una programación semanal.<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Especifica la fecha y hora en que se activa el desencadenador. Este elemento es obligatorio.<br/>                                    |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                               |
|------|------|-------------------------------------------|
| Identificador   | ID   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Comentarios

El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores time y calendar [**(TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) **y CalendarTrigger).**

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

Para el desarrollo de scripts, los desencadenadores de calendario se especifican mediante uno de los objetos siguientes.

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

Para el desarrollo de C++, los desencadenadores de calendario se especifican mediante una de las interfaces siguientes.

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que especifica un desencadenador de calendario, vea Ejemplo de desencadenador diario [(XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





