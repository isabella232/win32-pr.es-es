---
description: Contenga el nombre o una descripción de un perfil de LAN inalámbrica.
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
ms.openlocfilehash: 9179efbb52a07983f8d40c271ffc5c0b4ab3eea0c7ddd3a73e1ba790f867143f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684005"
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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



 

 




