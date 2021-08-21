---
description: Define un tipo para el elemento SimIccID del perfil de banda ancha móvil.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simple simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035763"
---
# <a name="simiccidtype-simple-type"></a>Tipo simple simIccIDType

El **tipo simple simIccIDType** define un tipo para el [**elemento SimIccID**](schema-simiccid-mbnprofile-element.md) del perfil de banda ancha móvil. Este tipo es una colección de dígitos o letras mayúsculas y minúsculas, al menos un carácter largo y 20 caracteres como máximo.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El **tipo simple simIccIDType** es un token restringido por el siguiente patrón:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




