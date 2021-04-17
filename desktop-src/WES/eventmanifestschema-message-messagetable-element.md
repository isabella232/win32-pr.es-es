---
title: Elemento message (messageTable)
description: Contiene una referencia a una cadena en la sección de localización del manifiesto. | Elemento message (messageTable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog del elemento de mensaje
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698055"
---
# <a name="message-messagetable-element"></a>Elemento message (messageTable)

Contiene una referencia a una cadena en la sección de localización del manifiesto.

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

El elemento de **mensaje** se define mediante el elemento [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .

## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Referencia a la cadena localizada en la tabla de cadenas.<br/>                                |
| mId     | string | No se utiliza.<br/>                                                                               |
| símbolo  | string | Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.<br/> |
| value   | string | Número que se va a usar como identificador de mensaje para este mensaje.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elementos primarios**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (MetadataType)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





