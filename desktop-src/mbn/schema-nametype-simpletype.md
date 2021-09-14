---
description: Define un tipo de cadena para el perfil de banda ancha móvil.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: tipo simple nameType (banda ancha móvil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168133"
---
# <a name="nametype-simple-type-mobile-broadband"></a>tipo simple nameType (banda ancha móvil)

El **tipo simple nameType** define un tipo de cadena para el perfil de banda ancha móvil. Esta cadena tiene al menos un carácter de longitud y 255 caracteres como máximo.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




