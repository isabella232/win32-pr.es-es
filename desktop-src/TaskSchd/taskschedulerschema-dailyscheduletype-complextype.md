---
title: Tipo complejo de dailyScheduleType
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- tipo complejo de dailyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686101"
---
# <a name="dailyscheduletype-complex-type"></a>Tipo complejo de dailyScheduleType

Define los elementos secundarios y la información de secuenciación para el elemento [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo | Descripción                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | Especifica el intervalo entre los días de la programación. <br/> |



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

 

 





