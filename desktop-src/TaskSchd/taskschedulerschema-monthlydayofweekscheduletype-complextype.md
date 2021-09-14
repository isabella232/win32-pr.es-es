---
title: monthlyDayOfWeekScheduleType Complex Type
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- Tipo complejo monthlyDayOfWeekScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259143"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a>monthlyDayOfWeekScheduleType Complex Type

Define los elementos secundarios y la información de secuenciación para [**el elemento ScheduleByMonthDayOfWeek.**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md)

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                   | Tipo                                                                     | Descripción                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana durante los que se ejecuta la tarea.<br/>   |
| [**Meses**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Especifica los meses del año durante los que se ejecuta la tarea.<br/> |
| [**Semanas**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [**weeksType**](taskschedulerschema-weekstype-complextype.md)           | Especifica las semanas del mes durante las que se ejecuta la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





