---
description: 'Tipo simple UInt32Type (contadores de rendimiento): define un tipo entero sin signo.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo simple UInt32Type (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92eafff1be2c1dc924a7041ad45cadfca994d03d776f61a3c866d6c3c2f6f380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033385"
---
# <a name="uint32type-simple-type-performance-counters"></a>Tipo simple UInt32Type (contadores de rendimiento)

Define un tipo entero sin signo.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Comentarios

Puede especificar el valor como un entero de 4 bytes o un valor hexadecimal en el intervalo comprendido entre 0 y 4.294.967.295.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




