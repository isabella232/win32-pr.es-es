---
title: Tipo simple GUIDType (esquema de eventos)
description: Define un tipo de identificador único global, en formato registro. | Tipo simple GUIDType (esquema de eventos)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Tipo simple EventLog de GUIDType
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750627"
---
# <a name="guidtype-simple-type-event-schema"></a>Tipo simple GUIDType (esquema de eventos)

Define un tipo de identificador único global, en formato registro.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **GUIDType** es una cadena que está restringida por el siguiente patrón:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    El valor debe ser un tipo de identificador único global en formato registro. Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Use GUIDGen.exe o UUIDGen.exe para crear un GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





