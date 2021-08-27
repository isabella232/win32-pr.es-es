---
title: Tipo simple runLevelType
description: Define los valores posibles para el elemento RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Tipo simple runLevelType Programador de tareas
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991075"
---
# <a name="runleveltype-simple-type"></a>Tipo simple runLevelType

Define los valores posibles para [**el elemento RunLevel (principalType).**](taskschedulerschema-runlevel-principaltype-element.md)

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

El **tipo simple runLevelType** define los siguientes valores.



| Value            | Descripción                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Las tareas se ejecutan con los privilegios mínimos (LUA).<br/> |
| HighestAvailable | Las tareas se ejecutan con los privilegios más altos.<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





