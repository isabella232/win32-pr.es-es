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
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800115"
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



| Valor | Descripción |
|-------|-------------|
| IBSS  |             |
| Ess   |             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




