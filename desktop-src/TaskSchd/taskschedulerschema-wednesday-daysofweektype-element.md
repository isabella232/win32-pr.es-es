---
title: Elemento Wednesday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el miércoles.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Miércoles, Programador de tareas
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80f26c921a10df8bd62714021345e7cd2bbbcd065940403f82bae3207445f0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002233"
---
# <a name="wednesday-daysofweektype-element"></a>Elemento Wednesday (daysOfWeekType)

Especifica que la tarea se ejecuta el miércoles.

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

El **elemento Wednesday** se define mediante el tipo complejo [**daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                  | Derivado de                                                             | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual del día de la semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.<br/>              |



## <a name="examples"></a>Ejemplos

El código XML siguiente define un calendario de día de la semana que inicia una tarea el miércoles.


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
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

 

 





