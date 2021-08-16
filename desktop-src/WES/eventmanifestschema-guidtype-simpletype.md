---
title: Tipo simple GUIDType (esquema EventManifest)
description: Define un tipo de identificador único global, en formato registro. | Tipo simple GUIDType (esquema EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
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
ms.openlocfilehash: 0ff7d5b0b65e7c434b6281098531e4eae5e76cf1565b21f6b1a3ffbca46af37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343734"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Tipo simple GUIDType (esquema EventManifest)

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





