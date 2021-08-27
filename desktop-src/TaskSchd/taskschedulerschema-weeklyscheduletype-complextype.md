---
title: weeklyScheduleType Complex Type
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- tipo complejo weeklyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f886b2901a5cf1ff1c9db0c8ec761a796b8e68a0f3bdc746afa13a9d8e32ee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099785"
---
# <a name="weeklyscheduletype-complex-type"></a>weeklyScheduleType Complex Type

Define los elementos secundarios y la información de secuenciación para [**el elemento ScheduleByWeek.**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
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
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                               | Tipo                                                                     | Descripción                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | Especifica el intervalo entre las semanas de la programación.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





