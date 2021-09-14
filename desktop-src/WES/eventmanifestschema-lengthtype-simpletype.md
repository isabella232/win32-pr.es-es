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
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241088"
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



 

 





