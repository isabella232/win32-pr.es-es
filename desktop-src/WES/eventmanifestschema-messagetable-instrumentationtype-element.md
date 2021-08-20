---
title: elemento messageTable (EventsType)
description: Contiene una referencia a una cadena en la sección de localización del manifiesto. | elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- elemento EventLog de messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5a2bcf374e336047deaa1339ac749fde3fa7c4f27b38e046f6c9bc651c0e0ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120902"
---
# <a name="messagetable-eventstype-element"></a>elemento messageTable (EventsType)

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

El tipo complejo [**EventsType**](eventmanifestschema-eventstype-complextype.md) define el elemento **messageTable.**

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo | Descripción                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Mensaje**](eventmanifestschema-message-messagetable-element.md) |      | Especifica una referencia a una cadena en la sección de localización del manifiesto.<br/> |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Referencia a la cadena localizada en la tabla de cadenas.<br/>                                |
| mId     | string | No se usa.<br/>                                                                               |
| símbolo  | string | Nombre simbólico que desea que el compilador de mensajes cree para esta cadena de mensaje.<br/> |
| value   | string | Número que se va a usar como identificador de mensaje para este mensaje.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elementos primarios**
</dt> <dt>

[**elemento events (InstrumentationType)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





