---
title: Tipo complejo eventTriggerType
description: Define los elementos secundarios y la información de secuenciación para el elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Tipo complejo eventTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0acd4bafa6033e461b69180862a8302e76f363b581d7f06b0812824f2031780b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612058"
---
# <a name="eventtriggertype-complex-type"></a>Tipo complejo eventTriggerType

Define los elementos secundarios y la información de secuenciación para el [**elemento EventTrigger.**](taskschedulerschema-eventtrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Suscripción**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica la consulta XPath que identifica el evento que activa el desencadenador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Especifica una secuencia de elementos que contienen un nombre y un valor de consulta XPath. Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el [**elemento**](taskschedulerschema-subscription-eventtriggertype-element.md) Subscription. El nombre del valor de consulta XPath se puede usar como variable en el [**elemento Body**](taskschedulerschema-body-showmessagetype-element.md) de la sección de acción [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) de una tarea. <br/> |



## <a name="remarks"></a>Observaciones

Además del elemento secundario definido aquí, el [**elemento EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) también usa elementos secundarios definidos por el tipo [**complejo triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

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

 

 





