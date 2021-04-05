---
description: Define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN cableada.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: tipo simple de nameType (LAN_policy)
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002359"
---
# <a name="nametype-simple-type-lan_policy"></a>tipo simple de nameType (LAN_policy)

El tipo simple nameType define un tipo de cadena para el nombre o la descripción de un perfil de directiva de LAN cableada. Los nombres y las descripciones son cadenas que tienen al menos un carácter de longitud y una longitud máxima de 255 caracteres.

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



 

 




