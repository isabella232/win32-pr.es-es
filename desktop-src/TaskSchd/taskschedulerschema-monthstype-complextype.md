---
title: tipo complejo monthsType
description: Define los elementos secundarios y la información de secuenciación para los elementos Months (monthlyDayOfWeekScheduleType) y Months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- monthsType complex type Programador de tareas
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259100"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





