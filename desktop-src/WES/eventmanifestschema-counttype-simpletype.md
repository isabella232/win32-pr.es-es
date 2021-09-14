---
title: Tipo simple CountType
description: Define un tipo de recuento que se usa para especificar el número de elementos de una matriz.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Tipo simple CountType EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967920"
---
# <a name="counttype-simple-type"></a>Tipo simple CountType

Define un tipo de recuento que se usa para especificar el número de elementos de una matriz. El valor se puede especificar como un valor xs:unsignedShort o como una cadena que hace referencia al nombre del nodo de elemento de datos que contiene el valor corto no especificado.

``` syntax
<xs:simpleType name="CountType">
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



 

 





