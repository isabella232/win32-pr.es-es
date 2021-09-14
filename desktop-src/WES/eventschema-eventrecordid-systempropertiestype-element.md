---
title: Elemento EventRecordID (SystemPropertiesType)
description: Número de registro asignado al evento cuando se registró.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- Elemento EventRecordID EventLog
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374354"
---
# <a name="eventrecordid-systempropertiestype-element"></a>Elemento EventRecordID (SystemPropertiesType)

Número de registro asignado al evento cuando se registró.

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

El tipo complejo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) define el elemento **EventRecordID.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





