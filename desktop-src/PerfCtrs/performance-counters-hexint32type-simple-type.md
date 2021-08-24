---
description: Define un tipo hexadecimal de 4 bytes.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo simple HexInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08b9ea7e483f6580e3f896a6a3f54a65e9117597538564889df8a5afb2fe795f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033485"
---
# <a name="hexint32type-simple-type-performance-counters"></a>Tipo simple HexInt32Type (contadores de rendimiento)

Define un tipo hexadecimal de 4 bytes.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple HexInt32Type** es **un xs:string** restringido por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,8}`

    El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xa o 0xac7bd361).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




