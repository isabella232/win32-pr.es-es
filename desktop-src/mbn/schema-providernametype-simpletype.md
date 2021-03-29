---
description: Define un tipo de cadena para el elemento ProviderName en el perfil de banda ancha móvil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo simple de providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541387"
---
# <a name="providernametype-simple-type"></a>Tipo simple de providerNameType

El tipo simple **providerNameType** define un tipo de cadena para el elemento [**providerName**](schema-providername-providertype-element.md) en el perfil de banda ancha móvil. Esta cadena tiene al menos un carácter de longitud y 20 caracteres como máximo.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




