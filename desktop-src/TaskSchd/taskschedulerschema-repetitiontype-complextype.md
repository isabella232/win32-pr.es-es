---
title: tipo complejo repetitionType
description: Define los elementos secundarios y la información de secuencia para el elemento Repetition (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- tipo complejo de tipo repetitionType Programador de tareas
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d45f83be8ab8b37211224ec9f284a71cdde6bfc06032c5d05df9e5dee8bf4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772095"
---
# <a name="repetitiontype-complex-type"></a>tipo complejo repetitionType

Define los elementos secundarios y la información de secuencia [**para el elemento Repetition (triggerBaseType).**](taskschedulerschema-repetition-triggerbasetype-element.md)

``` syntax
<xs:complexType name="repetitionType">
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
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                   | Tipo    | Descripción                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   |         | Especifica cuánto tiempo se repite el patrón. Si no se especifica ningún valor, el patrón se repite indefinidamente.<br/> |
| [**Intervalo**](taskschedulerschema-interval-repetitiontype-element.md)                   |         | Especifica la cantidad de tiempo entre cada reinicio de la tarea.<br/>                                              |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean | Especifica que una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.<br/>     |



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

 

 





