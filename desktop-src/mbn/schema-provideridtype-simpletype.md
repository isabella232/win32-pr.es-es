---
description: Define un tipo para el elemento ProviderID del perfil de banda ancha móvil.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Tipo simple de providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154191"
---
# <a name="provideridtype-simple-type"></a>Tipo simple de providerIdType

El tipo simple **providerIdType** define un tipo para el elemento [**ProviderID**](schema-providerid-providertype-element.md) del perfil de banda ancha móvil. Este tipo es una colección de dígitos de al menos un dígito de longitud y de 6 dígitos como máximo.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **providerIdType** es un token que está restringido por el siguiente patrón:

-   `\d{1,6}`

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




