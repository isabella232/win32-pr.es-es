---
title: CalendarTriggerType Complex Type
description: Define los elementos secundarios y la información de secuenciación para los elementos de calendario.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Tipo complejo calendarTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62b6aa2c3c1aff0e6e9cb706ede58c1b21af79fb7a5bae812a992e68bbd28b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866655"
---
# <a name="calendartriggertype-complex-type"></a>CalendarTriggerType Complex Type

Define los elementos secundarios y la información de secuenciación para los elementos de calendario.

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                      | Tipo                                                                                                 | Descripción                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).<br/> |
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Especifica una programación diaria. Por ejemplo, la tarea se inicia todos los días, cada dos días, cada tercer día, y así sucesivamente.<br/>                                                                                                               |
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Especifica una programación mensual. Por ejemplo, la tarea se inicia a las 8:00 a. m. en días específicos del mes en meses específicos. <br/>                                                                                                       |
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Especifica un desencadenador que inicia un trabajo según una programación mensual del día de la semana. Por ejemplo, la tarea se inicia en días específicos de la semana, semanas del mes y meses del año. <br/>                                               |
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Especifica una programación semanal. Por ejemplo, la tarea se inicia a las 8:00 a. m. en un día específico de la semana cada semana o en un día específico de la semana cada dos semanas. <br/>                                                              |



## <a name="remarks"></a>Comentarios

Además del elemento secundario definido aquí, el elemento [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) también usa los elementos secundarios definidos por el tipo complejo [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





