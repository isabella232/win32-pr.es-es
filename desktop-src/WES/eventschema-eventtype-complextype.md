---
title: Tipo complejo de EventType
description: Define el nodo raíz del esquema de eventos.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventLog de tipo complejo de EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421987"
---
# <a name="eventtype-complex-type"></a>Tipo complejo de EventType

Define el nodo raíz del esquema de eventos.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
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



| Elemento                                                                          | Tipo                                                                               | Descripción                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Contiene los datos del evento como un BLOB binario. Los datos de evento se representan como un BLOB binario si la función de representación no encuentra los metadatos usados para descodificar el evento.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Contiene los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contiene los datos del evento. El orden de los elementos de datos de la plantilla determina el diseño de los datos de evento.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contiene detalles del error que se produjo al intentar representar el evento. Esto puede ocurrir si los datos del evento no coinciden con la definición de datos del evento en el manifiesto. Los datos de evento se incluyen como un BLOB binario.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contiene las cadenas de mensaje representadas para el evento (incluye la cadena de mensaje del evento y las cadenas de mensaje para cualquiera de las propiedades del evento como el nivel, la tarea y el código de operación). Solo los eventos recopilados mediante el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) contendrán esta sección.<br/> |
| [**System**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contiene los datos del evento. La sección de datos de usuario de la plantilla determina el diseño de los datos de evento.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Observaciones

Normalmente, esta sección contendrá la sección **EventData** o **UserData** . La sección **EventData** se usa si la plantilla no contiene una sección **UserData** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

