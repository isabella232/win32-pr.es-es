---
title: OpCode (TaskEventDefinitionType) (elemento)
description: Contiene un código de operación específico de la tarea para un evento. Se supone que todas las definiciones de código de operación son específicas de la tarea para la tarea que contiene las definiciones de evento.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- elemento OpCode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696028"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>OpCode (TaskEventDefinitionType) (elemento)

\[A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, este elemento ya no está disponible.\]

Contiene un código de operación específico de la tarea para un evento. Se supone que todas las definiciones de código de operación son específicas de la tarea para la tarea que contiene las definiciones de evento.

``` syntax
<xs:element name="opcode">
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
```

El elemento **OpCode** se define mediante el tipo complejo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Tipo                                                                               | Descripción                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ceso**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento que se publica con una tarea.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo      | Descripción                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nombre del código de operación específico de la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**tarea (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





