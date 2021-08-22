---
description: Define un tipo de identificador único global, en formato registro.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo simple GUIDType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624925"
---
# <a name="guidtype-simple-type-performance-counters"></a>Tipo simple GUIDType (contadores de rendimiento)

Define un tipo de identificador único global, en formato registro.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **GUIDType** es **una cadena xs:string** que está restringida por el siguiente patrón:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    El valor debe ser un tipo de identificador único global en formato registro. Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Use GUIDGen.exe o UUIDGen.exe para crear un GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




