---
title: Tipo complejo EventDataType
description: Define las estructuras y elementos de datos de evento que contienen los datos del evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374358"
---
# <a name="eventdatatype-complex-type"></a>Tipo complejo EventDataType

Define las estructuras y elementos de datos de evento que contienen los datos del evento.

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
| [**Binario**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Blob de datos binarios para eventos que se escriben mediante [el registro de eventos](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Estructura que se define en la plantilla para el evento.<br/>                                |
| [**Data**](eventschema-data-eventdatatype-element.md)               | [**DataType**](eventschema-datafieldtype-complextype.md)          | Elemento de datos de nivel superior que se define en la plantilla para el evento.<br/>                      |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                       |
|------|--------|-------------------------------------------------------------------|
| Nombre | string | Nombre de la plantilla que contiene los elementos de datos.<br/> |



## <a name="remarks"></a>Observaciones

La [**función EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa matrices y estructuras como blobs binarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

