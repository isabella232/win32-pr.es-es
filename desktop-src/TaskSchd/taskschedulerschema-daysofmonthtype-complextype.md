---
title: tipo complejo daysOfMonthType
description: Define el elemento secundario y la información de secuenciación para el elemento DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- Tipo complejo daysOfMonthType Programador de tareas
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a32f2d0b3084e5146e53370d1771018a5d27a025f5ea419a61d8c39804d5611a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010855"
---
# <a name="daysofmonthtype-complex-type"></a>tipo complejo daysOfMonthType

Define el elemento secundario y la información de secuenciación para [**el elemento DaysOfMonth (monthlyScheduleType).**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md)

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                        | Tipo                                                                    | Descripción                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Día**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Especifica un día del mes durante el que se ejecuta la tarea. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





