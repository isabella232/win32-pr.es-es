---
title: Elemento xmlType (XmlTypeListType)
description: Define un tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- elemento xmlType EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695918"
---
# <a name="xmltype-xmltypelisttype-element"></a>Elemento xmlType (XmlTypeListType)

Define un tipo XML.

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

El elemento **xmlType** se define mediante el tipo complejo de [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre   | Tipo      | Descripción                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Nombre del tipo de salida.<br/>                                                                                                                                                                                                                    |
| símbolo | string    | Símbolo que se va a usar para hacer referencia al tipo de salida de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el tipo de salida en el archivo de encabezado que genera el compilador.<br/> |
| value  | string    | Valor entero que identifica de forma única el tipo de salida en la lista de tipos de salida que se define.<br/>                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**xmlTypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





