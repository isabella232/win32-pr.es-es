---
description: Define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN inalámbrica.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: tipo simple nameType (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161187"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo simple nameType (LAN_policy)

El tipo simple nameType define un tipo de cadena para el nombre o la descripción de un perfil de directiva LAN inalámbrica. Los nombres y descripciones son cadenas que tienen al menos un carácter de longitud y, como máximo, 255 caracteres.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
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
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




