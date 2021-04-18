---
title: Tipo complejo de restartType
description: Define los elementos secundarios y la información de secuencia para el elemento RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- tipo complejo de restartType Programador de tareas
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535494"
---
# <a name="restarttype-complex-type"></a>Tipo complejo de restartType

Define los elementos secundarios y la información de secuencia para el elemento [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo | Descripción                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Contabiliza**](taskschedulerschema-count-restarttype-element.md)       |      | Número de intentos de reinicio de la tarea.<br/> |
| [**Interval**](taskschedulerschema-interval-restarttype-element.md) |      | Cuánto tiempo se intentará iniciar la tarea.<br/>      |



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

 

 





