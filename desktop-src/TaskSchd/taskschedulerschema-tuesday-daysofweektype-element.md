---
title: Elemento Tuesday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el martes.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Elemento Tuesday Programador de tareas
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524d5dbe6b0deb1636fd06281d81b641665609310ad10a8b407da2dc570876ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355618"
---
# <a name="tuesday-daysofweektype-element"></a>Elemento Tuesday (daysOfWeekType)

Especifica que la tarea se ejecuta el martes.

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

El **elemento Tuesday** se define mediante el tipo complejo [**daysOfWeekType.**](taskschedulerschema-daysofweektype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                  | Derivado de                                                             | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual del día de la semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.<br/>              |



## <a name="examples"></a>Ejemplos

El código XML siguiente define un calendario de día de la semana que inicia una tarea el martes.


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





