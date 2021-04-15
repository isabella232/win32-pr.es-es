---
title: Elemento WeeksInterval (weeklyScheduleType)
description: Especifica el intervalo entre las semanas de la programación.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Programador de tareas del elemento WeeksInterval
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422534"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>Elemento WeeksInterval (weeklyScheduleType)

Especifica el intervalo entre las semanas de la programación.

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el tipo complejo de [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                                     | Descripción                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Especifica una programación semanal.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el intervalo semanal se especifica mediante la propiedad [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

En el desarrollo de C++, el intervalo semanal se especifica mediante la propiedad [**IWeeklyTrigger:: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un desencadenador de calendario semanal que inicia una tarea de lunes a viernes (a las 8:00 A.M.) cada semana.


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

 

 





