---
title: registrationTriggerType Complex Type
description: Define elementos secundarios e información de secuenciación para el elemento RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- tipo complejo registrationTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dab91ecc0eed065a4ce3eea9d64bebae2e10560a43ab57308ea68e82dc17dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772285"
---
# <a name="registrationtriggertype-complex-type"></a>registrationTriggerType Complex Type

Define elementos secundarios e información de secuenciación para [**el elemento RegistrationTrigger.**](taskschedulerschema-registrationtrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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



| Elemento                                                                    | Tipo     | Descripción                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Además de los elementos secundarios definidos aquí, el [**elemento RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) también usa elementos secundarios definidos por el tipo complejo [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





