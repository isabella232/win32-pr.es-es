---
title: Elemento DaysOfWeek (weeklyScheduleType)
description: Especifica los días de la semana en los que se ejecuta la tarea. | Elemento DaysOfWeek (weeklyScheduleType)
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
ms.openlocfilehash: 650dcaf33d85db3e9f0b4172ec7ca63fe6d35819459006f1bdd596e7c9483622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857800"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>Elemento DaysOfWeek (weeklyScheduleType)

Especifica los días de la semana en los que se ejecuta la tarea.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

El tipo complejo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) define el elemento **DaysOfWeek.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                                     | Descripción                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Especifica una programación semanal.<br/> |



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

El tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) define los elementos secundarios anteriores.

Para el desarrollo de scripting, el intervalo semanal se especifica mediante la [**propiedad WeeklyTrigger.WeeksInterval.**](weeklytrigger-weeksinterval.md)

Para el desarrollo de C++, el intervalo semanal se especifica mediante la [**propiedad IWeeklyTrigger::WeeksInterval.**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval)

## <a name="examples"></a>Ejemplos

El siguiente XML define un desencadenador de calendario diario que inicia una tarea de lunes a viernes (a las 8:00 a. m.) cada semana.


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



Para obtener un ejemplo completo del XML de una tarea que usa un desencadenador semanal, vea Ejemplo de desencadenador semanal [(XML).](weekly-trigger-example--xml-.md)

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

 

 





