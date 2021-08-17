---
title: Elemento Weeks (monthlyDayOfWeekScheduleType)
description: Especifica las semanas del mes en que se ejecuta la tarea.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento Weeks Programador de tareas
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757982"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Elemento Weeks (monthlyDayOfWeekScheduleType)

Especifica las semanas del mes en que se ejecuta la tarea.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

El **elemento Weeks** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType.**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                      | Derivado de                                                                                         | Descripción                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo según una programación mensual del día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                    | Tipo                                                        | Descripción                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Semana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Especifica una semana específica del mes.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, las semanas del mes se especifican mediante la [**propiedad MonthlyDOWTrigger.WeeksOfMonth.**](monthlydowtrigger-weeksofmonth.md)

Para el desarrollo de C++, las semanas del mes se especifican mediante la propiedad [**IMonthlyDOWTrigger::WeeksOfMonth.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth)

Al especificar las semanas del mes, use 1-4 para especificar las cuatro primeras semanas del mes o use la cadena "Last" para indicar la última semana independientemente de la semana que sea.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





