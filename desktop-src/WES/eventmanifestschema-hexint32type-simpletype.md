---
title: Tipo simple UInt32Type (Windows de eventos)
description: 'Tipo simple UInt32Type (Windows de eventos): define un tipo entero sin signo.'
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
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073309"
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



 

 





