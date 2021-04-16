---
title: Tipo complejo de eventTriggerType
description: Define los elementos secundarios y la información de secuenciación para el elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- tipo complejo de eventTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686100"
---
# <a name="eventtriggertype-complex-type"></a>Tipo complejo de eventTriggerType

Define los elementos secundarios y la información de secuenciación para el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .

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
| [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica la consulta XPath que identifica el evento que activa el desencadenador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Especifica una secuencia de elementos que contienen un nombre y un valor de consulta XPath. Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el elemento [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . El nombre del valor de consulta XPath se puede usar como una variable en el elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) de la sección de acción [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) de una tarea. <br/> |



## <a name="remarks"></a>Observaciones

Además del elemento secundario que se define aquí, el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) también utiliza elementos secundarios definidos por el tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





