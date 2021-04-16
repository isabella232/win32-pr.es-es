---
description: Define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN inalámbrica.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo simple de nameType (LAN_policy)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678391"
---
# <a name="nametype-simple-type-lan_policy"></a>Tipo simple de nameType (LAN_policy)

El tipo simple nameType define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN inalámbrica. Los nombres y las descripciones son cadenas que tienen al menos un carácter de longitud y una longitud máxima de 255 caracteres.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




