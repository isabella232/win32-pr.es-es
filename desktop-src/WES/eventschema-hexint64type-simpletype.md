---
title: HexInt64Type (tipo simple) (esquema de eventos)
description: Define un tipo hexadecimal de 8 bytes. | HexInt64Type (tipo simple) (esquema de eventos)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
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
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698138"
---
# <a name="hexint64type-simple-type-event-schema"></a>HexInt64Type (tipo simple) (esquema de eventos)

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

El tipo simple **HexInt64Type** es una **cadena** restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,16}`

    El valor puede contener de 1 a dieciséis caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361004fe190).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





