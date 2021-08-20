---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Especifica los días del mes durante los que se ejecuta la tarea.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Elemento DaysOfMonth Programador de tareas
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa490ab690d244bffe9b45801473df82a72d85fe564a3bf24940b44429620363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942840"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>Elemento DaysOfMonth (monthlyScheduleType)

Especifica los días del mes durante los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

El **elemento DaysOfMonth** se define mediante el [**tipo complejo monthlyScheduleType.**](taskschedulerschema-monthlyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                    | Derivado de                                                                                         | Descripción                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo para una programación mensual del día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                    | Descripción                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Día**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Especifica un día del mes durante el que se ejecuta la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripts, los días del mes de la programación se especifican mediante la [**propiedad MonthlyTrigger.DaysOfMonth.**](monthlytrigger-daysofmonth.md)

Para el desarrollo de C++, los días del mes de la programación se especifican mediante la propiedad [**IMonthlyTrigger::D aysOfMonth.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth)

El elemento secundario debe repetirse para cada día del mes que se va a ejecutar la tarea.

## <a name="examples"></a>Ejemplos

El código XML siguiente define un desencadenador de calendario mensual que inicia una tarea (a las 8:30 a. m.) el primer día de cada mes.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





