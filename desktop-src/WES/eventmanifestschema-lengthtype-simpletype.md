---
title: Tipo simple LengthType
description: Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Tipo simple LengthType EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997865"
---
# <a name="lengthtype-simple-type"></a>Tipo simple LengthType

Define un tipo de longitud que se usa para especificar el número de bytes o caracteres de un elemento de datos de longitud variable, como datos binarios o una cadena ANSI o Unicode. El valor se puede especificar como un valor xs:unsignedShort o como una cadena que hace referencia al nombre del nodo de elemento de datos que contiene el valor corto sin signo.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





