---
title: Elemento String (StringTableType)
description: Define una cadena traducida.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- elemento de cadena EventLog
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996579"
---
# <a name="string-stringtabletype-element"></a>Elemento String (StringTableType)

Define una cadena traducida.

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

El elemento de **cadena** se define mediante el tipo complejo de [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre       | Tipo   | Descripción                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | string | Identificador que identifica de forma única la cadena en la tabla de cadenas.<br/> |
| stringType | string | No se utiliza.<br/>                                                                  |
| value      | string | Cadena localizada.<br/>                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





