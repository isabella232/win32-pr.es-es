---
title: string (StringTableType) (Elemento)
description: Define una cadena localizada.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- elemento string EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136178"
---
# <a name="string-stringtabletype-element"></a>string (StringTableType) (Elemento)

Define una cadena localizada.

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

El **tipo complejo StringTableType** define el elemento [**string.**](eventmanifestschema-stringtabletype-complextype.md)

## <a name="attributes"></a>Atributos



| Nombre       | Tipo   | Descripción                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Identificador que identifica de forma única la cadena dentro de la tabla de cadenas.<br/> |
| stringType | string | No se usa.<br/>                                                                  |
| value      | string | Cadena localizada.<br/>                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





