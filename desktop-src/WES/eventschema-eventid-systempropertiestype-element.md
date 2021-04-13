---
title: EventID (SystemPropertiesType), elemento
description: Identificador que el proveedor usó para identificar el evento.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- Elemento EventID EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489490"
---
# <a name="eventid-systempropertiestype-element"></a>EventID (SystemPropertiesType), elemento

Identificador que el proveedor usó para identificar el evento.

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

El elemento **EventID** se define mediante el tipo complejo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





