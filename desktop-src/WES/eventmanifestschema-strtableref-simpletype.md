---
title: strTableRef Simple Type
description: Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas en el manifiesto o en un archivo de mensaje (.mc).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef de tipo simple EventLog
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97280b342015338be1cea089f8cb14121e2e51466506e89818501302c3fa891a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750921"
---
# <a name="strtableref-simple-type"></a>strTableRef Simple Type

Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas en el manifiesto o en un archivo de mensaje (.mc).

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple strTableRef** es **un xs:string** restringido por el siguiente patrón:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    La cadena debe tener el formato $string. *stringid* o $mc.*symbolid*. Si la cadena tiene el formato , $string. *stringid*, debe hacer referencia a una cadena en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. Si la cadena tiene el formato , $mc.*symbolid*, debe hacer referencia a un símbolo definido en el archivo de mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





