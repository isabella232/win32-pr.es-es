---
title: dailyScheduleType Complex Type
description: Define los elementos secundarios y la información de secuenciación para el elemento ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- tipo complejo dailyScheduleType Programador de tareas
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 881442d4aa6d6b22fb443a2670aac379b39bfed064089b95dd1bd07ba80a1f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357186"
---
# <a name="dailyscheduletype-complex-type"></a>dailyScheduleType Complex Type

Define los elementos secundarios y la información de secuenciación para [**el elemento ScheduleByDay.**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





