---
title: Tipo simple HexInt16Type
description: Define un tipo hexadecimal de 2 bytes.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Tipo simple HexInt16Type EventLog
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5f441071daa84f162a1dacbd16513fe2550b99d34d24ed90205ff4d8d184493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055964"
---
# <a name="hexint16type-simple-type"></a>Tipo simple HexInt16Type

Define un tipo hexadecimal de 2 bytes.

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple HexInt16Type** es una **cadena** restringida por el siguiente patrón:

-   `0[xX][0-9A-Fa-f]{1,4}`

    El valor puede contener de uno a cuatro caracteres hexadecimales (por ejemplo, 0xa o 0xac7b).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





