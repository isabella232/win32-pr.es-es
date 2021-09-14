---
title: Tipo complejo logonTriggerType
description: Define los elementos secundarios y la información de secuenciación para el elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Tipo complejo logonTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259183"
---
# <a name="logontriggertype-complex-type"></a>Tipo complejo logonTriggerType

Define los elementos secundarios y la información de secuenciación para el [**elemento LogonTrigger.**](taskschedulerschema-logontrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                                    | Descripción                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea.<br/>         |
| [**Userid**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.<br/> |



## <a name="remarks"></a>Observaciones

Además de los elementos secundarios definidos aquí, el elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) también usa elementos secundarios definidos por el tipo [**complejo triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





