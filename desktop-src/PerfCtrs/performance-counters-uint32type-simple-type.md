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
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114583"
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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




