---
description: Contenga el nombre o una descripción de un perfil de LAN inalámbrica.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Tipo simple de nameType (LAN_policy) (perfil)
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
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187834"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>nameType tipo simple (LAN_policy) para profileschema

El tipo simple nameType puede contener el nombre o una descripción de un perfil de LAN inalámbrica. Este valor de cadena debe tener entre 1 y 255 caracteres de longitud.

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
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



 

 




