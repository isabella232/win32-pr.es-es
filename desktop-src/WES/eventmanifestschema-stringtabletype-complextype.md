---
title: Tipo complejo de StringTableType
description: Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto. | Tipo complejo de StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- StringTableType tipo complejo EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698111"
---
# <a name="stringtabletype-complex-type"></a>Tipo complejo de StringTableType

Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo | Descripción                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**string**](eventmanifestschema-string-stringtabletype-element.md) |      | Define una cadena traducida.<br/> |



## <a name="attributes"></a>Atributos



| Nombre       | Tipo   | Descripción                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Identificador que identifica de forma única la cadena en la tabla de cadenas. Por ejemplo, "Printer. Connection".<br/> |
| stringType | string | No se utiliza.<br/>                                                                                                     |
| value      | string | Cadena localizada.<br/>                                                                                         |



## <a name="remarks"></a>Observaciones

Puede hacer referencia a las cadenas desde cualquier tipo de manifiesto que contenga el atributo Message. Para hacer referencia a una cadena con un valor de stringType de "String" y un identificador de "Printer. Connection", use $ (String. Printer. Connection) como valor del atributo Message.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





