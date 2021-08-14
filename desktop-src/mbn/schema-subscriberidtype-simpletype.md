---
description: Define un tipo para el elemento SubscriberID del perfil de banda ancha móvil.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: subscriberIdType Simple Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881369"
---
# <a name="subscriberidtype-simple-type"></a>subscriberIdType Simple Type

El **tipo simple subscriberIdType** define un tipo para el [**elemento SubscriberID**](schema-subscriberid-mbnprofile-element.md) del perfil de banda ancha móvil. Este tipo es una colección de uno o varios caracteres.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




