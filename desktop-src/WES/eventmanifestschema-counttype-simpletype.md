---
title: Tipo simple de CountType
description: Define un tipo de recuento que se utiliza para especificar el número de elementos de una matriz.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- CountType de tipo simple de registro
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804028"
---
# <a name="counttype-simple-type"></a>Tipo simple de CountType

Define un tipo de recuento que se utiliza para especificar el número de elementos de una matriz. El valor se puede especificar como un valor XS: unsignedShort o como una cadena que hace referencia al nombre del nodo elemento de datos que contiene el valor Short unsiged.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





