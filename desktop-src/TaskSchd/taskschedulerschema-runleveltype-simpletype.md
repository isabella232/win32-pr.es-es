---
title: Tipo simple de runLevelType
description: Define los valores posibles para el elemento nivel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Programador de tareas de tipo simple runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676877"
---
# <a name="runleveltype-simple-type"></a>Tipo simple de runLevelType

Define los valores posibles para el elemento [**nivel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) .

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El tipo simple **runLevelType** define los siguientes valores.



| Value            | Descripción                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Las tareas se ejecutan con los privilegios mínimos (LUA).<br/> |
| HighestAvailable | Las tareas se ejecutan con los privilegios más altos.<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





