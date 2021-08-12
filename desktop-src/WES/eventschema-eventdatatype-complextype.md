---
title: Tipo complejo EventDataType
description: Define las estructuras y los elementos de datos de evento que contienen los datos del evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType de tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 424f7f5f6472859a06605467c427fc7b9f210a960f0920fb8593778bd757fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589028"
---
# <a name="eventdatatype-complex-type"></a>Tipo complejo EventDataType

Define las estructuras y los elementos de datos de evento que contienen los datos del evento.

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo                                                               | Descripción                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Binario**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Blob de datos binarios para los eventos que se escriben mediante [el registro de eventos](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Estructura que se define en la plantilla para el evento.<br/>                                |
| [**data**](eventschema-data-eventdatatype-element.md)               | [**Datatype**](eventschema-datafieldtype-complextype.md)          | Elemento de datos de nivel superior que se define en la plantilla para el evento.<br/>                      |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                       |
|------|--------|-------------------------------------------------------------------|
| Nombre | string | Nombre de la plantilla que contiene los elementos de datos.<br/> |



## <a name="remarks"></a>Comentarios

La [**función EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa matrices y estructuras como blobs binarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

