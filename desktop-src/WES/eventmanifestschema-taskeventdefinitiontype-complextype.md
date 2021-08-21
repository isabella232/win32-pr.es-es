---
title: Tipo complejo TaskEventDefinitionType
description: Define un evento específico de la tarea que el proveedor puede registrar. | Tipo complejo TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44a4fc7ca8784b3472fea3b0d4f4e657ce615fae05a8cc7372aa3cca0fedb431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055843"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complejo TaskEventDefinitionType

\[A partir del compilador de mensajes que se incluye con la versión Windows 7 del SDK de Windows, el tipo complejo TaskEventDefinitionType ya no está disponible. En su lugar, use códigos de operación específicos de la tarea para proporcionar la misma funcionalidad.\]

Define un evento específico de la tarea que el proveedor puede registrar.

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="event"
                        type="EventDefinitionType"
                        maxOccurs="unbounded"
                     />
                </xs:sequence>
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
            </xs:complexType>
        </xs:element>
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                      | Tipo                                                                               | Descripción                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento específico de la tarea publicado con una tarea.<br/> |
| [**Opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Un código de operación específico de la tarea que para un evento. <br/>   |



## <a name="attributes"></a>Atributos



| Nombre | Tipo      | Descripción                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nombre del código de operación específico de la tarea.<br/> |
| name | anyURI    | Nombre de la tarea.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





