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
ms.openlocfilehash: 0dfa7f72ee537d857f19301aa4df906d94b0bf7ba9e3f7a76bdb6ab82c84dfd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314425"
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



 

 




