---
title: Tipo complejo DebugDataType
description: Define los datos que se pueden registrar para Windows de preprocesador de seguimiento de software (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38d5ec0297fce91b28592dfb9a894a62d3558f516a01ff18c942d37cc9c93f2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124235"
---
# <a name="debugdatatype-complex-type"></a>Tipo complejo DebugDataType

Define los datos que se pueden registrar para Windows de preprocesador de seguimiento de software (WPP).

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
| [**Fileline**](eventschema-fileline-debugdatatype-element.md)             | string      | Nombre del archivo de origen y la línea dentro del archivo de origen que registró el mensaje de seguimiento.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | string      | Valor de marca pasado al proveedor cuando se ha habilitado.<br/>                                              |
| [**Function**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Nombre de la función que registró el mensaje de seguimiento.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | Valor de nivel pasado al proveedor cuando se ha habilitado.<br/>                                             |
| [**Message**](eventschema-message-debugdatatype-element.md)               | string      | Cadena del mensaje. El XML contiene este elemento si el evento WPP especificó el campo FormattedString.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Número de secuencia local o global del mensaje de seguimiento.<br/>                                               |
| [**Subcomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | Nombre del subcomponente que registró el mensaje de seguimiento.<br/>                                             |



## <a name="remarks"></a>Comentarios

Los elementos solo se incluyen si el proveedor establece la variable de entorno %TRACE \_ FORMAT \_ PREFIX% para incluirlos. Para obtener más información sobre estos elementos, vea Trace Message Prefix( Prefijo de mensaje de seguimiento).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





