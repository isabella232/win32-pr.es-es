---
title: message (messageTable) (Elemento)
description: Contiene una referencia a una cadena en la sección localización del manifiesto. | message (messageTable) (Elemento)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- elemento message EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865675"
---
# <a name="message-messagetable-element"></a>message (messageTable) (Elemento)

Contiene una referencia a una cadena en la sección localización del manifiesto.

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El **elemento messagetable** define el [**elemento messageTable.**](eventmanifestschema-messagetable-instrumentationtype-element.md)

## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Referencia a la cadena localizada en la tabla de cadenas.<br/>                                |
| mId     | string | No se usa.<br/>                                                                               |
| símbolo  | string | Nombre simbólico que desea que el compilador de mensajes cree para esta cadena de mensaje.<br/> |
| value   | string | Número que se va a usar como identificador de mensaje para este mensaje.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elementos primarios**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





