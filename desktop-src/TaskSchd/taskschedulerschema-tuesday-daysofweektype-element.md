---
title: Elemento Tuesday (daysOfWeekType)
description: Especifica que la tarea se ejecuta el martes.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Tuesday (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676991"
---
# <a name="tuesday-daysofweektype-element"></a>Elemento Tuesday (daysOfWeekType)

Especifica que la tarea se ejecuta el martes.

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

El elemento **Tuesday** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                  | Derivado de                                                             | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.<br/>              |



## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario de día de la semana que inicia una tarea el martes.


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
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

 

 





