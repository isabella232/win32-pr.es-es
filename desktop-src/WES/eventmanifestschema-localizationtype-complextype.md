---
title: Tipo complejo LocalizationType
description: Define un grupo de recursos localizados a los que se hace referencia en el manifiesto. | Tipo complejo LocalizationType
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- Registro de eventos de tipo complejo LocalizationType
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a596ff981944943c193fb158f14aa04eafb0b0b3d4df660d2034c5b5d281be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055954"
---
# <a name="localizationtype-complex-type"></a>Tipo complejo LocalizationType

Define un grupo de recursos localizados a los que se hace referencia en el manifiesto.

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
| [**Recursos**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.<br/> |
| [**stringTable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Define una lista de cadenas localizadas a las que puede hacer referencia en el manifiesto.<br/>                             |



## <a name="attributes"></a>Atributos



| Nombre            | Tipo   | Descripción                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| referencia cultural         | string | Nombre de idioma que identifica la referencia cultural de las cadenas localizadas en la tabla de cadenas. Por ejemplo, "en-US" para inglés (Estados Unidos).<br/> |
| fallbackCulture | string | No se usa.<br/>                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





