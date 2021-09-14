---
description: Contiene el nombre o una descripción de un perfil de LAN inalámbrica.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: nameType Tipo simple (LAN_policy) (perfil)
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245445"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>nameType Tipo simple (LAN_policy) para profileschema

El tipo simple nameType puede contener el nombre o una descripción de un perfil de LAN inalámbrica. Este valor de cadena debe tener entre 1 y 255 caracteres.

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
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



 

 




