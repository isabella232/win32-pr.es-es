---
title: Tipo simple UInt64Type (esquema EventManifest)
description: Define un tipo Long sin signo.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- UInt64Type de tipo simple de registro
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079326"
---
# <a name="uint64type-simple-type"></a>Tipo simple de UInt64Type

Define un tipo Long sin signo. El valor se puede especificar como un entero de 8 bytes o como un valor hexadecimal en el intervalo comprendido entre 0 y 18446744073709551615.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





