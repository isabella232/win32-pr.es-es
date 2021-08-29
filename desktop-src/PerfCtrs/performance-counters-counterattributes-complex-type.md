---
description: Define una lista que contiene hasta cinco atributos de contador.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: counterAttributes (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be740abacc9a10674b98e2c2088f647dfaa26c7cd99c7e55efbfe968731a9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775425"
---
# <a name="counterattributes-complex-type"></a>counterAttributes (tipo complejo)

Define una lista que contiene hasta cinco atributos de contador.

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento              | Tipo                                                                               | Descripción                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **counterAttribute** | [**man:counterAttribute**](performance-counters-counterattribute-complex-type.md) | Atributo de contador que especifica cómo se muestran los datos del contador en una aplicación consumidora.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




