---
title: Tipo complejo de TaskEventDefinitionType
description: Define un evento específico de la tarea que el proveedor puede registrar. | Tipo complejo de TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698139"
---
# <a name="taskeventdefinitiontype-complex-type"></a>Tipo complejo de TaskEventDefinitionType

\[A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, el tipo complejo de TaskEventDefinitionType ya no está disponible. En su lugar, use códigos de tiempo específicos de la tarea para proporcionar la misma funcionalidad.\]

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
| **event**                                                                    | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento específico de tarea publicado con una tarea.<br/> |
| [**Código**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | Un código de operación específico de la tarea que para un evento. <br/>   |



## <a name="attributes"></a>Atributos



| Nombre | Tipo      | Descripción                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nombre del código de operación específico de la tarea.<br/> |
| name | anyURI    | Nombre de la tarea.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





