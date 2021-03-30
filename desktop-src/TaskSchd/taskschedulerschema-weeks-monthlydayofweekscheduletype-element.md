---
title: Weeks (monthlyDayOfWeekScheduleType), elemento
description: Especifica las semanas del mes en que se ejecuta la tarea.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Elemento weeks Programador de tareas
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803632"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Weeks (monthlyDayOfWeekScheduleType), elemento

Especifica las semanas del mes en que se ejecuta la tarea.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

El elemento **weeks** se define mediante el tipo complejo [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                      | Derivado de                                                                                         | Descripción                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo en una programación mensual de día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                    | Tipo                                                        | Descripción                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Semana**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Especifica una semana específica del mes.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, las semanas del mes se especifican mediante la propiedad [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .

En el desarrollo de C++, las semanas del mes se especifican mediante la propiedad [**IMonthlyDOWTrigger:: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .

Al especificar las semanas del mes, use 1-4 para especificar las cuatro primeras semanas del mes o use la cadena "Last" para indicar la última semana, independientemente de la semana en la que se encuentra.

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

 

 





