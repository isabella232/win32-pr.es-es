---
title: Tipo complejo EventType
description: Define el nodo raíz del esquema de eventos.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType de tipo complejo EventLog
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374346"
---
# <a name="eventtype-complex-type"></a>Tipo complejo EventType

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
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Contiene los datos del evento como un blob binario. Los datos del evento se representan como un blob binario si la función de representación no encuentra los metadatos usados para descodificar el evento.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Contiene los datos que se pueden registrar para Windows de preprocesador de seguimiento de software (WPP).<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contiene los datos del evento. El orden de los elementos de datos de la plantilla determina el diseño de los datos del evento.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contiene detalles del error que se produjo al intentar representar el evento. Esto puede ocurrir si los datos del evento no coinciden con la definición de datos del evento en el manifiesto. Los datos del evento se incluyen como un blob binario.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contiene las cadenas de mensaje representados para el evento (incluye la cadena de mensaje del evento y las cadenas de mensaje para cualquiera de las propiedades del evento, como level, task y opcode). Esta sección solo contendrá los eventos que se hayan recopilado [Windows servicio recopilador](/windows/desktop/WEC/windows-event-collector) de eventos.<br/> |
| [**Sistema**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contiene información que identifica el proveedor y cómo se ha habilitado, el evento, el canal en el que se escribió el evento y la información del sistema, como los identidades de proceso y subproceso.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contiene los datos del evento. La sección de datos de usuario de la plantilla determina el diseño de los datos del evento.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Observaciones

Normalmente, esta sección contendrá la **sección EventData** **o UserData.** La **sección EventData** se usa si la plantilla no contiene una **sección UserData.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

