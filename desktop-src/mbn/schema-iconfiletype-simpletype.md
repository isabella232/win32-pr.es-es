---
description: Define un tipo de cadena para el elemento ICONFilePath en el perfil de banda ancha móvil.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo simple de iconFileType
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154194"
---
# <a name="iconfiletype-simple-type"></a>Tipo simple de iconFileType

El tipo simple **iconFileType** define un tipo de cadena para el elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) en el perfil de banda ancha móvil. Esta cadena tiene al menos un carácter de longitud y una longitud máxima de 1024 caracteres.

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
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




