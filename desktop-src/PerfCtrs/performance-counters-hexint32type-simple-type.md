---
description: Define un tipo hexadecimal de 4 bytes.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo simple de HexInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667282"
---
# <a name="hexint32type-simple-type-performance-counters"></a>Tipo simple de HexInt32Type (contadores de rendimiento)

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

El tipo simple **HexInt32Type** es **xs: String** , que está restringido por el patrón siguiente:

-   `0[xX][0-9A-Fa-f]{1,8}`

    El valor puede contener de uno a ocho caracteres hexadecimales (por ejemplo, 0xA o 0xac7bd361).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




