---
title: Tipo complejo RenderingInfoType
description: Define los mensajes representados para el evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- EventLog de tipo complejo RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361746"
---
# <a name="renderinginfotype-complex-type"></a>Tipo complejo RenderingInfoType

Define los mensajes representados para el evento.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                             | Tipo   | Descripción                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | string | Cadena de mensaje representado del canal especificado en el evento.<br/> |
| [**Palabra clave**](eventschema-keyword-keywords-element.md)             | string | Cadena de mensaje representado de una palabra clave especificada en el evento .<br/>   |
| [**Palabras clave**](eventschema-keywords-renderingtype-element.md)      |        | Lista de palabras clave representados.<br/>                                       |
| [**Nivel**](eventschema-level-renderingtype-element.md)            | string | Cadena de mensaje representado del nivel especificado en el evento.<br/>   |
| [**Message**](eventschema-message-renderingtype-element.md)        | string | Cadena de mensaje representado del evento.<br/>                          |
| [**Código de operación**](eventschema-opcode-renderingtype-element.md)          | string | Cadena de mensaje representado del código de operación especificado en el evento.<br/>  |
| [**Proveedor**](eventschema-publisher-renderinginfotype-element.md) | string | Cadena de mensaje representado para el proveedor.<br/>                      |
| [**Tarea**](eventschema-task-renderingtype-element.md)              | string | Cadena de mensaje representado de la tarea especificada en el evento .<br/>    |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo     | Descripción                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | language | Nombre de idioma (por ejemplo, en-US) que identifica la configuración regional utilizada para representar las cadenas de mensaje.<br/> |



## <a name="remarks"></a>Observaciones

Esta sección solo contendrá los eventos recopilados [mediante Windows recopilador](/windows/desktop/WEC/windows-event-collector) de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

