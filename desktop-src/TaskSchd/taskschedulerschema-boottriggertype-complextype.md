---
title: Tipo complejo bootTriggerType
description: Define el elemento secundario y la información de secuenciación para el elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Tipo complejo bootTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0b04bfaf08ecee87d02a2b410fd1df2fbbe584d5649a5e9fe2ea2e5efacebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131864"
---
# <a name="boottriggertype-complex-type"></a>Tipo complejo bootTriggerType

Define el elemento secundario y la información de secuenciación para el [**elemento BootTrigger.**](taskschedulerschema-boottrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="bootTriggerType">
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



| Elemento                                                            | Tipo     | Descripción                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Cantidad de tiempo entre el momento en que se inicia el sistema y el momento en que se desencadena el desencadenador. <br/> |



## <a name="remarks"></a>Comentarios

Además del elemento secundario definido aquí, el [**elemento BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) también usa elementos secundarios definidos por el tipo complejo [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





