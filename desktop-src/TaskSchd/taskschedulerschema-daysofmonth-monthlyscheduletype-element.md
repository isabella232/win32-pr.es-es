---
title: Elemento DaysOfMonth (monthlyScheduleType)
description: Especifica los días del mes durante los que se ejecuta la tarea.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Programador de tareas del elemento DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686234"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>Elemento DaysOfMonth (monthlyScheduleType)

Especifica los días del mes durante los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

El elemento **DaysOfMonth** se define mediante el tipo complejo de [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                    | Derivado de                                                                                         | Descripción                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo para una programación mensual de día de la semana.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                    | Descripción                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Diariamente**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Especifica un día del mes durante el que se ejecuta la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, los días del mes para la programación se especifican mediante la propiedad [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .

En el desarrollo de C++, los días del mes para la programación se especifican mediante la propiedad [**IMonthlyTrigger::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .

El elemento secundario se debe repetir para cada día del mes en el que se va a ejecutar la tarea.

## <a name="examples"></a>Ejemplos

El siguiente código XML define un desencadenador de calendario mensual que inicia una tarea (a las 8:30 A.M.) el día 1 de cada mes.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





