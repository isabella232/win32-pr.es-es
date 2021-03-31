---
title: Tipo complejo de EventDataType
description: Define los elementos de datos de evento y las estructuras que contienen los datos de evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType tipo complejo EventLog
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801430"
---
# <a name="eventdatatype-complex-type"></a>Tipo complejo de EventDataType

Define los elementos de datos de evento y las estructuras que contienen los datos de evento.

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
| [**Binary**](eventschema-binary-eventdatatype-element.md)           | hexBinary                                                          | Un BLOB de datos binarios para los eventos que se escriben mediante el [registro de eventos](/windows/desktop/EventLog/event-logging).<br/> |
| [**ComplexData**](eventschema-complexdata-eventdatatype-element.md) | [**ComplexDataType**](eventschema-complexdatatype-complextype.md) | Estructura que se define en la plantilla para el evento.<br/>                                |
| [**Data**](eventschema-data-eventdatatype-element.md)               | [**DataType**](eventschema-datafieldtype-complextype.md)          | Un elemento de datos de nivel superior que se define en la plantilla para el evento.<br/>                      |



## <a name="attributes"></a>Atributos



| Nombre | Tipo   | Descripción                                                       |
|------|--------|-------------------------------------------------------------------|
| Nombre | string | Nombre de la plantilla que contiene los elementos de datos.<br/> |



## <a name="remarks"></a>Observaciones

La función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa matrices y estructuras como blobs binarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

