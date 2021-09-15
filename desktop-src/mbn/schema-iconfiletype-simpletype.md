---
description: Define un tipo de cadena para el elemento ICONFilePath en el perfil de banda ancha móvil.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: iconFileType Tipo simple
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568676"
---
# <a name="iconfiletype-simple-type"></a>iconFileType Tipo simple

El **tipo simple iconFileType** define un tipo de cadena para el [**elemento ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) en el perfil de banda ancha móvil. Esta cadena tiene al menos un carácter de longitud y 1024 caracteres como máximo.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




