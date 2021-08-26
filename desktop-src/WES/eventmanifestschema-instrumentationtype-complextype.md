---
title: Tipo complejo InstrumentationType
description: Define el contenido de la sección de instrumentación del manifiesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Registro de eventos de tipo complejo InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21462782ad14dfd977c87ab0898b7b9d2211e730bae42ed6281207fc557a4101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905005"
---
# <a name="instrumentationtype-complex-type"></a>Tipo complejo InstrumentationType

Define el contenido de la sección de instrumentación del manifiesto.

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                             | Descripción                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**events**](eventmanifestschema-events-instrumentationtype-element.md) | [**EventsType**](eventmanifestschema-eventstype-complextype.md) | Contiene una lista de proveedores que define el manifiesto.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





