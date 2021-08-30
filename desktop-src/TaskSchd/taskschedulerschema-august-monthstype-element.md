---
title: Elemento August (monthsType)
description: Especifica que la tarea se ejecuta en agosto.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Elemento August Programador de tareas
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c5a8d4adb6e0bdb855499abef9fbfda1ebe7de2cdcaba21ebde9647352ff57a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991455"
---
# <a name="august-monthstype-element"></a>Elemento August (monthsType)

Especifica que la tarea se ejecuta en agosto.

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

El **elemento August** se define mediante el tipo complejo [**monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                          | Derivado de                                                     | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual del día de la semana.<br/> |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual.<br/>             |



## <a name="examples"></a>Ejemplos

El xml siguiente define un calendario de meses que ejecuta la tarea en agosto.


```XML
<Months>
    <August/>
</Months>
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

 

 





