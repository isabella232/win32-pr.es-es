---
title: Elemento System (EventType)
description: Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- EventLog (elemento del sistema)
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695864"
---
# <a name="system-eventtype-element"></a>Elemento System (EventType)

Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

El elemento **System** se define mediante el tipo complejo de [**EventType**](eventschema-eventtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**evento**](eventschema-event-element.md)
</dt> </dl>

 

 





