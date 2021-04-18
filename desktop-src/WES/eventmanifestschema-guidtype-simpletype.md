---
title: Tipo simple GUIDType (esquema EventManifest)
description: Define un tipo de identificador único global, en formato de registro. | Tipo simple GUIDType (esquema EventManifest)
ms.assetid: c35fa54b-5a2e-46de-a1c7-fc408b00ee68
keywords:
- GUIDType de tipo simple de registro
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474715cf4e9c11536ca227ecdb5609b13be7e222
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698172"
---
# <a name="guidtype-simple-type-eventmanifest-schema"></a>Tipo simple GUIDType (esquema EventManifest)

Define un tipo de identificador único global, en formato de registro.

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

El tipo simple **GUIDType** es una cadena restringida por el siguiente patrón:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    El valor debe ser un tipo de identificador único global en el formato del registro. Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Utilice GUIDGen.exe o UUIDGen.exe para crear un GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





