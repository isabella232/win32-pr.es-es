---
title: Tipo simple de versionType
description: Define un patrón que especifica una versión de una tarea.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Programador de tareas de tipo simple versionType
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359695"
---
# <a name="versiontype-simple-type"></a>Tipo simple de versionType

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

El tipo simple **versionType** es una **cadena** restringida por el siguiente patrón:

-   `\d+(\.\d+){1,3}`

    Un valor de tipo Double seguido de uno, dos o tres valores double. Por ejemplo, 1,2 o 1.2.3.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





