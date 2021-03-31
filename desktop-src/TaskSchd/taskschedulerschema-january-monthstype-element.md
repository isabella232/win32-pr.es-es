---
title: Elemento de enero (monthsType)
description: Especifica que la tarea se ejecuta en enero.
ms.assetid: 3a0dde08-f2de-4ff4-9c5a-4368ff7a0e2c
keywords:
- Programador de tareas del elemento de enero
topic_type:
- apiref
api_name:
- January
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e72967f0fb6addb70af1792ffabf0457b1d20c29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801483"
---
# <a name="january-monthstype-element"></a>Elemento de enero (monthsType)

Especifica que la tarea se ejecuta en enero.

``` syntax
<xs:element name="January">
    <xs:complexType />
</xs:element>
```

El elemento de **enero** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                          | Derivado de                                                     | Descripción                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Meses (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.<br/> |
| [**Meses (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.<br/>             |



## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario de meses que ejecuta la tarea en enero.


```XML
<Months>
    <January/>
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

 

 





