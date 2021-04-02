---
description: Define un tipo para el elemento SubscriberID del perfil de banda ancha móvil.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Tipo simple de subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082097"
---
# <a name="subscriberidtype-simple-type"></a>Tipo simple de subscriberIdType

El tipo simple **subscriberIdType** define un tipo para el elemento [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) del perfil de banda ancha móvil. Este tipo es una colección de uno o más caracteres.

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




