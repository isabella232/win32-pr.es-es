---
description: Define una lista de estructuras que contienen valores de contador.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Structs (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667269"
---
# <a name="structs-complex-type"></a>Structs (tipo complejo)

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
| **struct** | [**Man: struct**](performance-counters-struct-complex-type.md) | Nombre de una estructura que contiene los valores del contador.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




