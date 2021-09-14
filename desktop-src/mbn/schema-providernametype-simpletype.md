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
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252554"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




