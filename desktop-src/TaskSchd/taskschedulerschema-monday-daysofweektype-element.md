---
title: Elemento Monday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el lunes.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Elemento Monday Programador de tareas
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 22bd1028a36efa6e2fe96a300b221073dbf87f14e77621d8b1591f85c7f6fd6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513945"
---
# <a name="monday-daysofweektype-element"></a>Elemento Monday (daysOfWeekType)

Especifica que la tarea se ejecuta el lunes.

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

El tipo complejo [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) define el elemento **Monday.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                  | Derivado de                                                             | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual del día de la semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.<br/>              |



## <a name="examples"></a>Ejemplos

El código XML siguiente define un calendario de día de la semana que inicia una tarea el lunes.


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





