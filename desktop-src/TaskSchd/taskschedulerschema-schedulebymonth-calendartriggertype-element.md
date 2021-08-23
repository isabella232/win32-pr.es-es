---
title: Elemento ScheduleByMonth (calendarTriggerType)
description: Especifica una programación mensual.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Elemento ScheduleByMonth Programador de tareas
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a03fcc3b30e4fe684926baaba2815132c9f2f06bf4373b4e9fbbc181e187bf6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513815"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Elemento ScheduleByMonth (calendarTriggerType)

Especifica una programación mensual. Por ejemplo, la tarea se inicia a las 8:00 a. m. en días específicos del mes en meses específicos.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

El **elemento ScheduleByMonth** se define mediante el [**tipo complejo calendarTriggerType.**](taskschedulerschema-calendartriggertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                  | Tipo                                                                       | Descripción                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica los días del mes durante los que se ejecuta la tarea.<br/>  |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Especifica los meses del año durante los que se ejecuta la tarea.<br/> |



## <a name="remarks"></a>Comentarios

El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) establece la hora del día en que se inicia la tarea.

Para el desarrollo de scripts, se especifica un desencadenador mensual mediante el [**objeto MonthlyTrigger.**](monthlytrigger.md)

Para el desarrollo de C++, se especifica un desencadenador mensual mediante la [**interfaz IMonthlyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)

Los elementos secundarios enumerados a continuación se definen mediante los tipos de elementos complejos [**monthlyScheduleType.**](taskschedulerschema-monthlyscheduletype-complextype.md)

## <a name="examples"></a>Ejemplos

El siguiente XML define un desencadenador de calendario mensual que inicia una tarea (a las 8:00 a. m.) el día 1 y 15 de cada mes del año.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
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

 

 





