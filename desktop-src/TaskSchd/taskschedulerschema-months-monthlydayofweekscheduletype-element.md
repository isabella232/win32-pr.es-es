---
title: Elemento Months (monthlyDayOfWeekScheduleType)
description: Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual del día de la semana.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Elementos Months Programador de tareas
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259111"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Elemento Months (monthlyDayOfWeekScheduleType)

Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual del día de la semana.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

El **elemento Months** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                            | Derivado de                                                                                         | Descripción                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo para una programación mensual del día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo | Descripción                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**April**](taskschedulerschema-april-monthstype-element.md)         |      | Especifica que la tarea se ejecuta en abril.<br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       |      | Especifica que la tarea se ejecuta en agosto.<br/>    |
| [**Diciembre**](taskschedulerschema-december-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en diciembre.<br/>  |
| [**February**](taskschedulerschema-february-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en febrero.<br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     |      | Especifica que la tarea se ejecuta en enero.<br/>   |
| [**Julio**](taskschedulerschema-july-monthstype-element.md)           |      | Especifica que la tarea se ejecuta en julio.<br/>      |
| [**Junio**](taskschedulerschema-june-monthstype-element.md)           |      | Especifica que la tarea se ejecuta en junio.<br/>      |
| [**Marzo**](taskschedulerschema-march-monthstype-element.md)         |      | Especifica que la tarea se ejecuta en marzo.<br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             |      | Especifica que la tarea se ejecuta en mayo.<br/>       |
| [**Noviembre**](taskschedulerschema-november-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en noviembre.<br/>  |
| [**Octubre**](taskschedulerschema-october-monthstype-element.md)     |      | Especifica que la tarea se ejecuta en octubre.<br/>   |
| [**Septiembre**](taskschedulerschema-september-monthstype-element.md) |      | Especifica que la tarea se ejecuta en septiembre.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, los meses de un año para una programación mensual del día de la semana se especifican mediante la [**propiedad MonthlyDOWTrigger.MonthsOfYear.**](monthlydowtrigger-monthsofyear.md)

Para el desarrollo de C++, los meses de un año para una programación mensual del día de la semana se especifican mediante la propiedad [**IMonthlyDOWTrigger::MonthsOfYear.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear)

Los elementos secundarios anteriores se definen mediante el [**tipo complejo monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="examples"></a>Ejemplos

El xml siguiente define un calendario mensual del día de la semana que inicia la tarea el lunes de la primera semana para cada mes del año.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





