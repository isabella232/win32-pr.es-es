---
description: Define un tipo de cadena para los identificadores de conjunto de servicios (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: tipo simple networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f653c84f36730ed9f6f078b3713dde414fbf63469bd4ea43f632842d33d7e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064755"
---
# <a name="networknametype-simple-type"></a>tipo simple networkNameType

El tipo simple networkNameType define un tipo de cadena para los identificadores de conjunto de servicios (SSID). Un SSID es una cadena que tiene al menos un carácter de longitud y, como máximo, 32 caracteres.

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




