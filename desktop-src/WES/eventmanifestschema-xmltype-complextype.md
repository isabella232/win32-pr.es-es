---
title: Tipo complejo XmlType
description: Define un fragmento XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Tipo complejo XmlType EventLog
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9ac529ad3d965af76c144d0f02c1e6f8e5aef36fb25fd2fb052a5fdedc1e45f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589166"
---
# <a name="xmltype-complex-type"></a>Tipo complejo XmlType

Define un fragmento XML. Se permite cualquier instancia de esquema; El nodo de nivel superior del fragmento debe contener un atributo de espacio de nombres.

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





