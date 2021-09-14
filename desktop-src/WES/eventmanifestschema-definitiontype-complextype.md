---
title: Tipo complejo DefinitionType
description: Define una lista de eventos que el proveedor puede registrar.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Tipo complejo DefinitionType EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967903"
---
# <a name="definitiontype-complex-type"></a>Tipo complejo DefinitionType

Define una lista de eventos que el proveedor puede registrar.

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                           | Tipo                                                                                       | Descripción                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Evento**](eventmanifestschema-event-definitiontype-element.md) | [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)         | Define un evento que el proveedor puede registrar.<br/>                                                                                                                                                                                                                                 |
| [**Tarea**](eventmanifestschema-task-definitiontype-element.md)   | [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) | No compatible.<br/> **Windows Server 2008 y Windows Vista:** Define un evento específico de la tarea que el proveedor puede registrar. (A partir del compilador de mensajes que se incluye con la versión Windows 7 del SDK de Windows, ya no se admiten eventos específicos de tareas).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





