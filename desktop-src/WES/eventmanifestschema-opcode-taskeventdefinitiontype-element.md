---
title: opcode (TaskEventDefinitionType) (Elemento)
description: Contiene un código de operación específico de la tarea para un evento. Se supone que todas las definiciones de código de operación son específicas de la tarea que contiene las definiciones de eventos.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- elemento opcode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f3923e0a42375ac7d926d418943af81cc0264e111e6bdc4be56919780dfacf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652155"
---
# <a name="opcode-taskeventdefinitiontype-element"></a>opcode (TaskEventDefinitionType) (Elemento)

\[A partir del compilador de mensajes que se incluye Windows versión 7 del SDK de Windows, este elemento ya no está disponible.\]

Contiene un código de operación específico de la tarea para un evento. Se supone que todas las definiciones de código de operación son específicas de la tarea que contiene las definiciones de eventos.

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

El tipo complejo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) define el elemento **opcode.**

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Tipo                                                                               | Descripción                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Evento**](eventmanifestschema-event-opcode-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md) | Evento que se publica con una tarea.<br/> |



## <a name="attributes"></a>Atributos



| Nombre | Tipo      | Descripción                                      |
|------|-----------|--------------------------------------------------|
| name | **QName** | Nombre del código de operación específico de la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**task (DefinitionType)**](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





