---
title: tipo simple pathType
description: Define el número mínimo y máximo de caracteres para una cadena que define una ruta de acceso de archivo.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Tipo simple pathType Programador de tareas
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758384"
---
# <a name="pathtype-simple-type"></a>tipo simple pathType

Define el número mínimo y máximo de caracteres para una cadena que define una ruta de acceso de archivo. La ruta de acceso no puede ser una cadena vacía y debe tener menos de 260 caracteres.

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





