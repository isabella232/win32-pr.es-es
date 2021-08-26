---
title: Provider (SystemPropertiesType) (Elemento)
description: Identifica el proveedor que registró el evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Elemento Provider EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904534"
---
# <a name="provider-systempropertiestype-element"></a>Provider (SystemPropertiesType) (Elemento)

Identifica el proveedor que registró el evento.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El tipo complejo **SystemPropertiesType** define el [**elemento Provider.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Atributos



| Nombre            | Tipo                                                | Descripción                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | string                                              | Nombre del origen del evento que publicó el evento (si el origen del evento es de la API de registro de eventos [heredada).](/windows/desktop/EventLog/event-logging)<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica de forma única el proveedor.<br/>                                                                   |
| Nombre            | anyURI                                              | Nombre del proveedor de eventos que registró el evento.<br/>                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

