---
title: Elemento TimeCreated (SystemPropertiesType)
description: Marca de tiempo que identifica Cuándo se registró el evento.
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
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996578"
---
# <a name="timecreated-systempropertiestype-element"></a>Elemento TimeCreated (SystemPropertiesType)

Marca de tiempo que identifica Cuándo se registró el evento.

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

El elemento **TimeCreated** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre       | Tipo     | Descripción                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | Hora del sistema en la que se registró el evento.<br/> |



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

 

 





