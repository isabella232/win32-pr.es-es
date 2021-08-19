---
title: elemento resources (LocalizationType)
description: Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- elemento resources EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120582"
---
# <a name="resources-localizationtype-element"></a>elemento resources (LocalizationType)

Define un grupo de tablas de cadenas que contienen las cadenas localizadas a las que se hace referencia en el manifiesto.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El **elemento resources** se define mediante el tipo complejo [**LocalizationType.**](eventmanifestschema-localizationtype-complextype.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                                       | Descripción                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**stringTable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Define una lista de cadenas localizadas a las que puede hacer referencia en el manifiesto.<br/> |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo   | Descripción                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| referencia cultural | string | Nombre de idioma que identifica la referencia cultural de las cadenas localizadas en la tabla de cadenas. Por ejemplo, "en-US" para inglés (Estados Unidos).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**localización (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





