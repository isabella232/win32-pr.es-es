---
title: Tipo complejo de daysOfWeekType
description: Define los elementos secundarios y la información de secuenciación para los elementos DaysOfWeek (weeklyScheduleType) y DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- tipo complejo de daysOfWeekType Programador de tareas
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359865"
---
# <a name="daysofweektype-complex-type"></a>Tipo complejo de daysOfWeekType

Define los elementos secundarios y la información de secuenciación para los elementos [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) y [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Tipo | Descripción                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Día**](taskschedulerschema-friday-daysofweektype-element.md)       | N/D  | La tarea se ejecuta el viernes. <br/>    |
| [**Lunes**](taskschedulerschema-monday-daysofweektype-element.md)       | N/D  | La tarea se ejecuta el lunes.<br/>     |
| [**Sábado**](taskschedulerschema-saturday-daysofweektype-element.md)   | N/D  | La tarea se ejecuta el sábado. <br/>  |
| [**Domingo**](taskschedulerschema-sunday-daysofweektype-element.md)       | N/D  | La tarea se ejecuta el domingo. <br/>    |
| [**Martes**](taskschedulerschema-thursday-daysofweektype-element.md)   | N/D  | La tarea se ejecuta el jueves <br/>   |
| [**Jueves**](taskschedulerschema-tuesday-daysofweektype-element.md)     | N/D  | La tarea se ejecuta el martes. <br/>   |
| [**Lunes**](taskschedulerschema-wednesday-daysofweektype-element.md) | N/D  | La tarea se ejecuta el miércoles. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos complejos de esquema Programador de tareas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





