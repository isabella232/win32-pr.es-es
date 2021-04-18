---
title: DaysOfWeek (weeklyScheduleType), elemento
description: Especifica los días de la semana en los que se ejecuta la tarea. | DaysOfWeek (weeklyScheduleType), elemento
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- Elemento DaysOfWeek Programador de tareas
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689830"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>DaysOfWeek (weeklyScheduleType), elemento

Especifica los días de la semana en los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

El elemento **DaysOfWeek** se define mediante el tipo complejo de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                                     | Descripción                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Especifica una programación semanal.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo | Descripción                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Día**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el viernes.<br/>    |
| [**Lunes**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el lunes.<br/>    |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Especifica que la tarea se ejecuta el sábado.<br/>  |
| [**Domingo**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el domingo.<br/>    |
| [**Martes**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Especifica que la tarea se ejecuta el jueves.<br/>  |
| [**Jueves**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Especifica que la tarea se ejecuta el martes.<br/>   |
| [**Lunes**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Especifica que la tarea se ejecuta el miércoles.<br/> |



## <a name="remarks"></a>Observaciones

Los elementos secundarios anteriores se definen mediante el tipo complejo de [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

Para el desarrollo de scripting, el intervalo semanal se especifica mediante la propiedad [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

En el desarrollo de C++, el intervalo semanal se especifica mediante la propiedad [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un desencadenador de calendario diario que inicia una tarea de lunes a viernes (a las 8:00 A.M.) cada semana.


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



Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador semanal, consulte el [ejemplo de desencadenador semanal (XML)](weekly-trigger-example--xml-.md).

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

 

 





