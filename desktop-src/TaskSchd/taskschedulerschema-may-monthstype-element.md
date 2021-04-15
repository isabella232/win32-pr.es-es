---
title: Elemento May (monthsType)
description: Especifica que la tarea se ejecuta en mayo.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Elemento puede Programador de tareas
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676871"
---
# <a name="may-monthstype-element"></a>Elemento May (monthsType)

Especifica que la tarea se ejecuta en mayo.

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

El elemento **puede estar** definido por el tipo complejo [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                          | Derivado de                                                     | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.<br/>             |



## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un calendario de meses que ejecuta la tarea en mayo.


```XML
<Months>
    <May/>
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

 

 





