---
title: Elemento CalendarTrigger (triggerGroup)
description: Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- desencadenador de calendario Programador de tareas, elemento XML
- Programador de tareas del elemento CalendarTrigger
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686080"
---
# <a name="calendartrigger-triggergroup-element"></a>Elemento CalendarTrigger (triggerGroup)

Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

El elemento **CalendarTrigger** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                            | Tipo                                                                                                 | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)                             | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Especifica una programación diaria.<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Especifica una programación mensual.<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo en una programación mensual de día de la semana.<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Especifica una programación semanal.<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Especifica la fecha y hora en que se activa el desencadenador. Este elemento es obligatorio.<br/>                                    |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                               |
|------|------|-------------------------------------------|
| Identificador   | id   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores de tiempo y calendario ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) y **CalendarTrigger**).

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

Para el desarrollo de scripts, los desencadenadores de calendario se especifican mediante uno de los siguientes objetos.

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

En el desarrollo de C++, los desencadenadores de calendario se especifican mediante una de las interfaces siguientes.

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de calendario, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





