---
title: Tipo simple de pathType
description: Define el número mínimo y máximo de caracteres de una cadena que define una ruta de acceso de archivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Programador de tareas de tipo simple pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686225"
---
# <a name="pathtype-simple-type"></a>Tipo simple de pathType

Define el número mínimo y máximo de caracteres de una cadena que define una ruta de acceso de archivo. La ruta de acceso no puede ser una cadena vacía y debe tener menos de 260 caracteres.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





