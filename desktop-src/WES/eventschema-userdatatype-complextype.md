---
title: Tipo complejo UserDataType
description: Define un fragmento XML que especifica el diseño de los datos del evento.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Tipo complejo UserDataType EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747f2e30f6b2588cdfd6a9f0dd50187b73817996bd3725a571283a7929c91b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904195"
---
# <a name="userdatatype-complex-type"></a>Tipo complejo UserDataType

Define un fragmento XML que especifica el diseño de los datos del evento.

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





