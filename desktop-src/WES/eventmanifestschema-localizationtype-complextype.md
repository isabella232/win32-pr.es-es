---
title: Tipo complejo de LocalizationType
description: Define un grupo de recursos localizados al que se hace referencia en el manifiesto. | Tipo complejo de LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType tipo complejo EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698058"
---
# <a name="localizationtype-complex-type"></a>Tipo complejo de LocalizationType

Define un grupo de recursos localizados al que se hace referencia en el manifiesto.

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                                       | Descripción                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**recursos**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.<br/> |
| [**stringTable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Define una lista de cadenas traducidas a las que se puede hacer referencia en el manifiesto.<br/>                             |



## <a name="attributes"></a>Atributos



| Nombre            | Tipo   | Descripción                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture         | string | Un nombre de idioma que identifica la referencia cultural de las cadenas localizadas en la tabla de cadenas. Por ejemplo, "en-US" para inglés (Estados Unidos).<br/> |
| fallbackCulture | string | No se utiliza.<br/>                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





