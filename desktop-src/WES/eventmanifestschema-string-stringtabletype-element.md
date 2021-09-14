---
title: elemento string (StringTableType)
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
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068525"
---
# <a name="string-stringtabletype-element"></a>elemento string (StringTableType)

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

El **tipo** complejo [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) define el elemento string.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





