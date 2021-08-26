---
title: Tipo simple HexInt32Type (esquema de eventos)
description: Define un tipo hexadecimal de 4 bytes. | Tipo simple HexInt32Type (esquema de eventos)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
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
ms.openlocfilehash: 25c977bca3ecf7b883b87a535b40b44024ded2a54025bdcb1ac107254ce932fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904755"
---
# <a name="hexint32type-simple-type-event-schema"></a>Tipo simple HexInt32Type (esquema de eventos)

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



 

 





