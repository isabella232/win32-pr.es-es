---
title: Tipo complejo de TypeListType
description: Define los tipos que se usan en el manifiesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- TypeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695993"
---
# <a name="typelisttype-complex-type"></a>Tipo complejo de TypeListType

Define los tipos que se usan en el manifiesto.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                                                           | Descripción                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Intypes**](eventmanifestschema-intypes-typelisttype-element.md)   | [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md) | Define una lista de tipos de datos de entrada.<br/>                                                              |
| [**xmlTypes**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)     | Define una lista de tipos de salida que el servicio usa para determinar cómo se representa un tipo de datos de entrada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





