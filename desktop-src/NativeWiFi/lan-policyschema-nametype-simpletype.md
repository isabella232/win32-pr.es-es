---
description: Define un tipo de cadena para el nombre o la descripción de un perfil de directiva LAN cableada.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
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
ms.openlocfilehash: 3b3d558717777c9b2bead2fd7e141dee38b22491af4142d4948c7f1f76aadfd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065115"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo simple nameType (LAN_policy)

El tipo simple nameType define un tipo de cadena para el nombre o la descripción de un perfil de directiva LAN cableada. Los nombres y descripciones son cadenas que tienen al menos un carácter de longitud y, como máximo, 255 caracteres.

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




