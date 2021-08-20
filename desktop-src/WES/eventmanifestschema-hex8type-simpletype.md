---
title: Tipo simple HexInt8Type
description: Define un tipo hexadecimal de 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Tipo simple HexInt8Type EventLog
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d2d70b7258317f16ac4e134f011a85218fa1b63aa768136f68b1d21c901856e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121011"
---
# <a name="hexint8type-simple-type"></a>Tipo simple HexInt8Type

Define un tipo hexadecimal de 1 byte.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple HexInt8Type** es una [cadena](/dotnet/api/system.string) restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,2}`

    El valor puede contener de uno a dos caracteres hexadecimales (por ejemplo, 0xa o 0xac).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

