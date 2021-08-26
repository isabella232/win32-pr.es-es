---
title: Elemento October (monthsType)
description: Especifica que la tarea se ejecuta en octubre.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Elemento October Programador de tareas
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65f14f0ccaa2831bc4aae24ce45a520f746a57b2e9d03d70b64714bafa69e25b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125735"
---
# <a name="october-monthstype-element"></a>Elemento October (monthsType)

Especifica que la tarea se ejecuta en octubre.

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

El **elemento October** se define mediante el tipo complejo [**monthsType.**](taskschedulerschema-monthstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                          | Derivado de                                                     | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual del día de la semana.<br/> |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual.<br/>             |



## <a name="examples"></a>Ejemplos

El siguiente XML define un calendario de meses que ejecuta la tarea en octubre.


```XML
<Months>
    <October/>
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

 

 





