---
title: Tipo complejo StringTableType
description: Define una lista de cadenas localizadas a las que puede hacer referencia en el manifiesto. | Tipo complejo StringTableType
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Tipo complejo StringTableType EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d52f19ca01a926c82fcc1e13cc7191866722ba5e0e6eef81e916e244744783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342989"
---
# <a name="stringtabletype-complex-type"></a>Tipo complejo StringTableType

Define una lista de cadenas localizadas a las que puede hacer referencia en el manifiesto.

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
| [**Cadena**](eventmanifestschema-string-stringtabletype-element.md) |      | Define una cadena localizada.<br/> |



## <a name="attributes"></a>Atributos



| Nombre       | Tipo   | Descripción                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | string | Identificador que identifica de forma única la cadena dentro de la tabla de cadenas. Por ejemplo, "Printer.Connection".<br/> |
| stringType | string | No se usa.<br/>                                                                                                     |
| value      | string | Cadena localizada.<br/>                                                                                         |



## <a name="remarks"></a>Comentarios

Puede hacer referencia a las cadenas de cualquier tipo de manifiesto que contenga el atributo de mensaje. Para hacer referencia a una cadena con un stringType de "string" y un identificador de "Printer.Connection", use $(string. Printer.Connection) como el valor del atributo de mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





