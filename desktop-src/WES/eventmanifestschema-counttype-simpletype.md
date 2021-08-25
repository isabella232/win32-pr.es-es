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
ms.openlocfilehash: 63476d70a9bb5b336449a65707664c05c56a20b4c2c9fa4888c0c3125f129d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863625"
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



 

 





