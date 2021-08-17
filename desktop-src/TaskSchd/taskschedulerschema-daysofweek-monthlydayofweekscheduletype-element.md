---
title: Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
description: Especifica los días de la semana en los que se ejecuta la tarea. | Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: c7ed2a597c1b92245a34dae510c079a5b5aa7a4e7893a78dbb70d7bc5988d580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357160"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>Elemento DaysOfWeek (monthlyDayOfWeekScheduleType)

Especifica los días de la semana en los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

El **elemento DaysOfWeek** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                      | Derivado de                                                                                         | Descripción                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo para una programación mensual del día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo | Descripción                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Viernes**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el viernes.<br/>    |
| [**Lunes**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el lunes.<br/>    |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Especifica que la tarea se ejecuta el sábado.<br/>  |
| [**Domingo**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Especifica que la tarea se ejecuta el domingo.<br/>    |
| [**Jueves**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Especifica que la tarea se ejecuta el jueves.<br/>  |
| [**Martes**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Especifica que la tarea se ejecuta el martes.<br/>   |
| [**Miércoles**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Especifica que la tarea se ejecuta el miércoles.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, los días de la semana de un calendario mensual del día de la semana se especifican mediante la [**propiedad MonthlyDOWTrigger.DaysOfWeek.**](monthlydowtrigger-daysofweek.md)

Para el desarrollo de C++, los días de la semana de un calendario mensual del día de la semana se especifican mediante la propiedad [**IMonthlyDOWTrigger::D aysOfWeek.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek)

Los elementos secundarios anteriores se definen mediante el [**tipo complejo daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="examples"></a>Ejemplos

El código XML siguiente define un calendario mensual del día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.


```XML
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
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





