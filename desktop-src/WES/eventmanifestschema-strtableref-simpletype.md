---
title: Tipo simple de strTableRef
description: Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas del manifiesto o en un archivo de mensajes (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef de tipo simple de registro
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534384"
---
# <a name="strtableref-simple-type"></a>Tipo simple de strTableRef

Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas del manifiesto o en un archivo de mensajes (. MC).

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

El tipo simple **strTableRef** es **xs: String** , que está restringido por el patrón siguiente:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    La cadena debe tener el formato $string. *stringid* o $MC.*symbolid*. Si la cadena tiene el formato, $string. *stringid*, debe hacer referencia a una cadena en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. Si la cadena tiene el formato, $mc.*symbolid*, debe hacer referencia a un símbolo definido en el archivo de mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





