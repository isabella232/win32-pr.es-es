---
description: Define los tipos de red inalámbrica.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: tipo simple networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161170"
---
# <a name="networktypetype-simple-type"></a>tipo simple networkTypeType

El tipo simple networkTypeType define los tipos de red inalámbrica. Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple networkTypeType** define los siguientes valores.



| Value | Descripción |
|-------|-------------|
| IBSS  |             |
| ESS   |             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




