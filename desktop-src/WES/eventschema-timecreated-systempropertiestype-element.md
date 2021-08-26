---
title: Elemento TimeCreated (SystemPropertiesType)
description: Marca de tiempo que identifica cuándo se registró el evento.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- Elemento TimeCreated EventLog
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5026bed56e3e065a403c0e6076daa0ec478223c4d742db0a35109a41cc98d5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005305"
---
# <a name="timecreated-systempropertiestype-element"></a>Elemento TimeCreated (SystemPropertiesType)

Marca de tiempo que identifica cuándo se registró el evento.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

El tipo complejo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) define el elemento **TimeCreated.**

## <a name="attributes"></a>Atributos



| Nombre       | Tipo     | Descripción                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | La hora del sistema de cuando se registró el evento.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





