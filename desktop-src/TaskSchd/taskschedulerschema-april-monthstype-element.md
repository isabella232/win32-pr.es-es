---
title: Elemento April (monthsType)
description: Especifica que la tarea se ejecuta en abril.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- April (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151021"
---
# <a name="april-monthstype-element"></a>Elemento April (monthsType)

Especifica que la tarea se ejecuta en abril.

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

El elemento **April** se define mediante el tipo complejo [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                          | Derivado de                                                     | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.<br/>             |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.<br/> |



## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario de meses que ejecuta la tarea en abril.


```XML
<Months>
    <April/>
</Months>
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

 

 





