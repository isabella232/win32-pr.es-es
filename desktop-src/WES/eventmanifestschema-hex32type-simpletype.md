---
title: Tipo simple HexInt32Type (esquema EventManifest)
description: Define un tipo hexadecimal de 4 bytes. | Tipo simple HexInt32Type (esquema EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- Tipo simple HexInt32Type EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248105"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>Tipo simple HexInt32Type (esquema EventManifest)

Define un tipo hexadecimal de 4 bytes.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple HexInt32Type** es una **cadena** restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,8}`

    El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xa o 0xac7bd361).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





