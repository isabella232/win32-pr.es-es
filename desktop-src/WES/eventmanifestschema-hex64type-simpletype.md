---
title: Tipo simple HexInt64Type
description: Define un tipo hexadecimal de 8 bytes. | Tipo simple HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- Tipo simple HexInt64Type EventLog
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 22b0cacc482f5bde657c9cf5eb451acb273e79cda0cbf14a4d3536fe90af756c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652425"
---
# <a name="hexint64type-simple-type"></a>Tipo simple HexInt64Type

Define un tipo hexadecimal de 8 bytes.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple HexInt64Type** es una [cadena](/dotnet/api/system.string) restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,16}`

    El valor puede contener de uno a dieciséis caracteres hexadecimales (por ejemplo, 0xa o 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

