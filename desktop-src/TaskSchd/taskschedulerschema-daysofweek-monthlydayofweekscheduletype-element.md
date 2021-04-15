---
title: DaysOfWeek (monthlyDayOfWeekScheduleType), elemento
description: Especifica los días de la semana en los que se ejecuta la tarea. | DaysOfWeek (monthlyDayOfWeekScheduleType), elemento
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689831"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek (monthlyDayOfWeekScheduleType), elemento

Especifica los días de la semana en los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

El elemento **DaysOfWeek** se define mediante el tipo complejo de [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                      | Derivado de                                                                                         | Descripción                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo para una programación mensual de día de la semana.<br/> |



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

Para el desarrollo de scripting, los días de la semana de un calendario mensual de día de la semana se especifican mediante la propiedad [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .

En el desarrollo de C++, los días de la semana de un calendario mensual de día de la semana se especifican mediante la propiedad [**IMonthlyDOWTrigger::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .

Los elementos secundarios anteriores se definen mediante el tipo complejo de [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario mensual de día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.


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

 

 





