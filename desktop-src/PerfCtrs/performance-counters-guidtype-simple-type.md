---
description: Define un tipo de identificador único global, en formato de registro.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo simple de GUIDType (contadores de rendimiento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909717"
---
# <a name="guidtype-simple-type-performance-counters"></a>Tipo simple de GUIDType (contadores de rendimiento)

Define un tipo de identificador único global, en formato de registro.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Patrones

El tipo simple **GUIDType** es **xs: String** , que está restringido por el patrón siguiente:

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    El valor debe ser un tipo de identificador único global en el formato del registro. Por ejemplo, {5b2fc63a-8af4-44cb-960c-aefdced908d6}. Utilice GUIDGen.exe o UUIDGen.exe para crear un GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




