---
title: Tipo simple de HexInt64Type
description: Define un tipo hexadecimal de 8 bytes. | Tipo simple de HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- HexInt64Type de tipo simple de registro
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424208"
---
# <a name="hexint64type-simple-type"></a>Tipo simple de HexInt64Type

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

El tipo simple **HexInt64Type** es una [cadena](/dotnet/api/system.string) restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,16}`

    El valor puede contener de 1 a dieciséis caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

