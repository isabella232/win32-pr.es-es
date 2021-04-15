---
title: Elemento jueves (daysOfWeekType)
description: Especifica que la tarea se ejecuta el jueves.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Programador de tareas del elemento jueves
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676869"
---
# <a name="thursday-daysofweektype-element"></a>Elemento jueves (daysOfWeekType)

Especifica que la tarea se ejecuta el jueves.

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

El elemento **jueves** se define mediante el tipo complejo [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                  | Derivado de                                                             | Descripción                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación mensual de día de la semana.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Especifica los días de la semana en los que se ejecuta la tarea para una programación semanal.<br/>              |



## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario de día de la semana que inicia una tarea el jueves.


```XML
<DaysOfWeek>
    <Thursday/>
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

 

 





