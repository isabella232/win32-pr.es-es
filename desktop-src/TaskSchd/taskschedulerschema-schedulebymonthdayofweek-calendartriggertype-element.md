---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Especifica una programación mensual del día de la semana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Elemento ScheduleByMonthDayOfWeek Programador de tareas
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 185608ea5a8805511de8430c82e6eecabd9cc5b9622fed85d71e26dd39f20cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099885"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)

Especifica una programación mensual del día de la semana. Por ejemplo, la tarea se inicia en días específicos de la semana, semanas del mes y meses del año.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

El **elemento ScheduleByMonthDayOfWeek** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                   | Tipo                                                                     | Descripción                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea.<br/>       |
| [**Meses**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Especifica los meses del año durante los que se ejecuta la tarea.<br/> |
| [**Semanas**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Especifica el intervalo entre las semanas de la programación.<br/>    |



## <a name="remarks"></a>Comentarios

El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) establece la hora del día en que se inicia la tarea.

Para el desarrollo de scripting, se especifica un desencadenador mensual del día de la semana mediante el [**objeto MonthlyDOWTrigger.**](monthlydowtrigger.md)

Para el desarrollo de C++, se especifica un desencadenador del día de la semana mensual mediante la [**interfaz IMonthlyDOWTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="examples"></a>Ejemplos

El xml siguiente define un desencadenador de calendario del día de la semana mensual que inicia una tarea ( a las 8:00 a. m.) el lunes de la primera semana para cada mes del año.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





