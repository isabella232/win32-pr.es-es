---
title: Tipo simple UInt32Type (Windows de eventos)
description: 'UInt32Type Simple Type (Windows Event Log): define un tipo entero sin signo.'
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- UInt32Tipo de tipo simple EventLog
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1bd3ecb22b3b2bb65d3563a1a29ba4a1ff9550ff2c4de68dba1cf81789d7f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865875"
---
# <a name="uint32type-simple-type-windows-event-log"></a>Tipo simple UInt32Type (Windows de eventos)

Define un tipo entero sin signo. El valor se puede especificar como un entero de 4 bytes o un valor hexadecimal en el intervalo comprendido entre 0 y 4.294.967.295.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





