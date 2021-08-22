---
description: Define un tipo de cadena para el elemento ProviderName del perfil de banda ancha móvil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: ProviderNameType Tipo simple
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744407"
---
# <a name="providernametype-simple-type"></a>ProviderNameType Tipo simple

El **tipo simple providerNameType** define un tipo de cadena para el [**elemento ProviderName**](schema-providername-providertype-element.md) en el perfil de banda ancha móvil. Esta cadena tiene al menos un carácter de longitud y 20 caracteres como máximo.

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




