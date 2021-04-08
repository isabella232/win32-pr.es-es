---
title: Tipo complejo de DebugDataType
description: Define los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078797"
---
# <a name="debugdatatype-complex-type"></a>Tipo complejo de DebugDataType

Define los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
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



| Elemento                                                                    | Tipo        | Descripción                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Componente**](eventschema-component-debugdatatype-element.md)           | string      | Nombre del componente que registró el mensaje de seguimiento.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | string      | Nombre del archivo de código fuente y la línea del archivo de código fuente que registró el mensaje de seguimiento.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | string      | El valor de marca que se pasa al proveedor cuando se habilitó.<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | El nombre de la función que registró el mensaje de seguimiento.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | Valor de nivel que se pasa al proveedor cuando se habilitó.<br/>                                             |
| [**Message**](eventschema-message-debugdatatype-element.md)               | string      | Cadena del mensaje. El XML contiene este elemento si el evento WPP especificó el campo FormattedString.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | El número de secuencia local o global del mensaje de seguimiento.<br/>                                               |
| [**Subcomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | Nombre del subcomponente que registró el mensaje de seguimiento.<br/>                                             |



## <a name="remarks"></a>Observaciones

Los elementos se incluyen solo si el proveedor ha establecido la variable de entorno% TRACE \_ format \_ prefix% para incluirlos. Para obtener más información sobre estos elementos, consulte prefijo de mensaje de seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





