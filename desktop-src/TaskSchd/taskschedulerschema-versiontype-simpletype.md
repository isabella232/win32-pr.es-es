---
title: tipo simple versionType
description: Define un patrón que especifica una versión de una tarea.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- tipo simple versionType Programador de tareas
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168829"
---
# <a name="versiontype-simple-type"></a>tipo simple versionType

Define un patrón que especifica una versión de una tarea.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **versionType** es **una cadena** restringida por el siguiente patrón:

-   `\d+(\.\d+){1,3}`

    Un doble seguido de uno, dos o tres dobles. Por ejemplo, 1.2 o 1.2.3.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





