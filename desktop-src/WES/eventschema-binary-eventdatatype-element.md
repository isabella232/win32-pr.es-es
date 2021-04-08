---
title: Elemento binario (EventDataType)
description: Un BLOB de datos binarios para los eventos que se escriben mediante el registro de eventos.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- EventLog del elemento binario
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078882"
---
# <a name="binary-eventdatatype-element"></a>Elemento binario (EventDataType)

Un BLOB de datos binarios para los eventos que se escriben mediante el [registro de eventos](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

El elemento **binario** se define mediante el tipo complejo [**EventDataType**](eventschema-eventdatatype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

