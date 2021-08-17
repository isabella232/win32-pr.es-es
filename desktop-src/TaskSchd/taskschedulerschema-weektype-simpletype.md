---
title: Tipo simple weekType
description: Define los valores que se pueden usar en el elemento Week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- tipo simple weekType Programador de tareas
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 923d5a5d672407f9d15fed62bd554853f23ce5b31debd6a7c331e4b1217f15fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757938"
---
# <a name="weektype-simple-type"></a>Tipo simple weekType

Define los valores que se pueden usar en el [**elemento Week.**](taskschedulerschema-week-weekstype-element.md)

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **weekType** es una **cadena** restringida por el siguiente patrón:

-   `[1-4]|Last`

    Especifica la primera a la cuarta semana del mes (1-4) o siempre la última semana del mes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas simples de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





