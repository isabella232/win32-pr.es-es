---
description: Define una lista de estructuras que contienen valores de contador.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: structs Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250568"
---
# <a name="structs-complex-type"></a>structs Complex Type

Define una lista de estructuras que contienen valores de contador.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento    | Tipo                                                           | Descripción                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**man:struct**](performance-counters-struct-complex-type.md) | Nombre de una estructura que contiene valores de contador.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




