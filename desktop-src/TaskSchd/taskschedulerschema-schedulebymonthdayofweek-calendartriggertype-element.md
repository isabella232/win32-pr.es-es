---
title: Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Especifica una programación mensual de día de la semana.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Programador de tareas del elemento ScheduleByMonthDayOfWeek
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803319"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Elemento ScheduleByMonthDayOfWeek (calendarTriggerType)

Especifica una programación mensual de día de la semana. Por ejemplo, la tarea se inicia en determinados días de la semana, semanas del mes y meses del año.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

El elemento **ScheduleByMonthDayOfWeek** se define mediante el tipo complejo de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                   | Tipo                                                                     | Descripción                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea.<br/>       |
| [**Partir**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Especifica los meses del año en los que se ejecuta la tarea.<br/> |
| [**Semanas**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Especifica el intervalo entre las semanas de la programación.<br/>    |



## <a name="remarks"></a>Observaciones

La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Para el desarrollo de scripting, se especifica un desencadenador de día de la semana mensual mediante el objeto [**MonthlyDOWTrigger**](monthlydowtrigger.md) .

En el desarrollo de C++, se especifica un desencadenador de día de la semana mensual mediante la interfaz [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un desencadenador de calendario mensual de un día de la semana que inicia una tarea (a las 8:00 A.M.) el lunes de la primera semana para cada mes del año.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





