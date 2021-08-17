---
title: Tipo simple nonEmptyStringType
description: Define los valores usados para una cadena de texto no vacía.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Tipo simple nonEmptyString Programador de tareas
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758421"
---
# <a name="nonemptystringtype-simple-type"></a>Tipo simple nonEmptyStringType

Define los valores usados para una cadena de texto no vacía.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple nonEmptyString** define el valor siguiente.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| 1     | La cadena contiene al menos un carácter.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





