---
title: tipo complejo monthsType
description: Define los elementos secundarios y la información de secuenciación para los elementos Months (monthlyDayOfWeekScheduleType) y Months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- monthsType tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0873f07cc76af9fab827c3df98a8f08ef300de93d4ae6b316809ba32aac87ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758751"
---
# <a name="monthstype-complex-type"></a>tipo complejo monthsType

Define los elementos secundarios y la información de secuenciación para los elementos [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) y [**Months (monthlyScheduleType).**](taskschedulerschema-months-monthlyscheduletype-element.md)

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo | Descripción                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**April**](taskschedulerschema-april-monthstype-element.md)         | N/D  | Especifica que la tarea se ejecuta en abril. <br/>     |
| [**Agosto**](taskschedulerschema-august-monthstype-element.md)       | N/D  | Especifica que la tarea se ejecuta en agosto. <br/>    |
| [**Diciembre**](taskschedulerschema-december-monthstype-element.md)   | N/D  | Especifica que la tarea se ejecuta en diciembre. <br/>  |
| [**February**](taskschedulerschema-february-monthstype-element.md)   | N/D  | Especifica que la tarea se ejecuta en febrero. <br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     | N/D  | Especifica que la tarea se ejecuta en enero. <br/>   |
| [**Julio**](taskschedulerschema-july-monthstype-element.md)           | N/D  | Especifica que la tarea se ejecuta en julio. <br/>      |
| [**Junio**](taskschedulerschema-june-monthstype-element.md)           | N/D  | Especifica que la tarea se ejecuta en junio. <br/>      |
| [**Marzo**](taskschedulerschema-march-monthstype-element.md)         | N/D  | Especifica que la tarea se ejecuta en marzo. <br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             | N/D  | Especifica que la tarea se ejecuta en mayo. <br/>       |
| [**Noviembre**](taskschedulerschema-november-monthstype-element.md)   | N/D  | Especifica que la tarea se ejecuta en noviembre. <br/>  |
| [**Octubre**](taskschedulerschema-october-monthstype-element.md)     | N/D  | Especifica que la tarea se ejecuta en octubre. <br/>   |
| [**Septiembre**](taskschedulerschema-september-monthstype-element.md) | N/D  | Especifica que la tarea se ejecuta en septiembre. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





