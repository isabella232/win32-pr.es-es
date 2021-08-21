---
title: elemento xmlType (XmlTypeListType)
description: Define un tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- Elemento xmlType EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 119ebe7f09f86aa46d9e80380670309fe8734fa818b48049d5dffc29e6a2ebb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863285"
---
# <a name="xmltype-xmltypelisttype-element"></a>elemento xmlType (XmlTypeListType)

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

El tipo complejo XmlTypeListType define el [**elemento xmlType.**](eventmanifestschema-xmltypelisttype-complextype.md) 

## <a name="attributes"></a>Atributos



| Nombre   | Tipo      | Descripción                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Nombre del tipo de salida.<br/>                                                                                                                                                                                                                    |
| símbolo | string    | Símbolo que se usará para hacer referencia al tipo de salida de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el tipo de salida en el archivo de encabezado que genera el compilador.<br/> |
| value  | string    | Valor entero que identifica de forma única el tipo de salida en la lista de tipos de salida que defina.<br/>                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**xmlTypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





