---
title: Elemento ScheduleByWeek (calendarTriggerType)
description: Especifica una programación semanal.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- desencadenador semanal Programador de tareas elemento , XML
- Elemento ScheduleByWeek Programador de tareas
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968676"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Elemento ScheduleByWeek (calendarTriggerType)

Especifica una programación semanal. Por ejemplo, la tarea se inicia a las 8:00 a. m. en un día específico de la semana cada semana o en un día específico de la semana cada dos semanas.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

El tipo complejo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) define el elemento **ScheduleByWeek.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                               | Tipo                                                                     | Descripción                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Especifica el intervalo entre las semanas de la programación.<br/> |



## <a name="remarks"></a>Observaciones

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**weeklyScheduleType.**](taskschedulerschema-weeklyscheduletype-complextype.md)

El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) establece la hora del día en que se inicia la tarea.

Para el desarrollo de scripting, se especifica un desencadenador semanal mediante el [**objeto WeeklyTrigger.**](weeklytrigger.md)

Para el desarrollo de C++, se especifica un desencadenador semanal mediante la [**interfaz IWeeklyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="examples"></a>Ejemplos

El código XML siguiente define un desencadenador de calendario semanal que inicia una tarea de lunes a viernes (a las 8:00 a. m.) cada semana.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





