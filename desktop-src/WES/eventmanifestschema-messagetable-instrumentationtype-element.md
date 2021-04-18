---
title: Elemento messageTable (EventsType)
description: Contiene una referencia a una cadena en la sección de localización del manifiesto. | Elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- elemento messageTable EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698054"
---
# <a name="messagetable-eventstype-element"></a>Elemento messageTable (EventsType)

Contiene una referencia a una cadena en la sección de localización del manifiesto.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **messageTable** se define mediante el tipo complejo de [**EventsType**](eventmanifestschema-eventstype-complextype.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo | Descripción                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensaje**](eventmanifestschema-message-messagetable-element.md) |      | Especifica una referencia a una cadena en la sección de localización del manifiesto.<br/> |



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

[**Elemento Events (InstrumentationType)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





