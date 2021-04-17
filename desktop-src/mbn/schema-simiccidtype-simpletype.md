---
description: Define un tipo para el elemento SimIccID del perfil de banda ancha móvil.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Tipo simple de simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666503"
---
# <a name="simiccidtype-simple-type"></a>Tipo simple de simIccIDType

El tipo simple **simIccIDType** define un tipo para el elemento [**SimIccID**](schema-simiccid-mbnprofile-element.md) del perfil de banda ancha móvil. Este tipo es una colección de dígitos y/o letras mayúsculas y minúsculas, al menos un carácter de longitud y 20 caracteres como máximo.

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

El tipo simple **simIccIDType** es un token que está restringido por el siguiente patrón:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




