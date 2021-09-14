---
title: Elemento Binary (EventDataType)
description: Blob de datos binarios para los eventos que se escriben mediante el registro de eventos.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Elemento binario EventLog
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242666"
---
# <a name="binary-eventdatatype-element"></a>Elemento Binary (EventDataType)

Blob de datos binarios para eventos que se escriben mediante [el registro de eventos](/windows/desktop/EventLog/event-logging).

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

El tipo complejo [**EventDataType**](eventschema-eventdatatype-complextype.md) define el elemento **Binary.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

