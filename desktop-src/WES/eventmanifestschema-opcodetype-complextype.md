---
title: Tipo complejo OpcodeType
description: Define una operación dentro de un componente de la aplicación.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Tipo complejo OpcodeType EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b18fa8a7591a54877251e10448842c3cd9d2394099028bf3a2cb680aee979bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136218"
---
# <a name="opcodetype-complex-type"></a>Tipo complejo OpcodeType

Define una operación dentro de un componente de la aplicación. Se usa junto con una tarea para identificar la sección de la aplicación que registra el evento.

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre     | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado del código de operación. La cadena de mensaje hace referencia a una cadena localizada en la [**sección stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Reservado para uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Nombre del código de operación. Este nombre debe ser único dentro del ámbito de este proveedor. <br/>                                                                                                                                                                                                                      |
| símbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se usará para hacer referencia al código de operación de la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) usa el símbolo para crear una constante para el código de operación en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valor del código de operación. Puede especificar valores en el intervalo 10 y 239. Para obtener una lista de valores de código de operación predefinidos, vea Comentarios.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Comentarios

Estos son los valores predefinidos de código de operación que puede usar. Estos valores se definen en el Winmeta.xml que se incluye en Windows SDK.



| Nombre          | Value | Símbolo                      | Descripción                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| win:Info      | 0     | INFORMACIÓN DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT      | Evento de información.                                                                                |
| win:Start     | 1     | INICIO DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT     | Evento que representa el inicio de una actividad.                                                         |
| win:Stop      | 2     | WINEVENT \_ OPCODE \_ STOP      | Evento que representa la detención de una actividad. El evento corresponde al último evento de inicio no apareado. |
| win:DC \_ Start | 3     | WINEVENT \_ OPCODE \_ DC \_ START | Evento que representa el inicio de la recopilación de datos. Se trata de tipos de eventos de resumen.                      |
| win:DC \_ Stop  | 4     | WINEVENT \_ OPCODE \_ DC \_ STOP  | Evento que representa la detención de la recopilación de datos. Se trata de tipos de eventos de resumen.                      |
| win:Extension | 5     | EXTENSIÓN DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT | Evento de extensión.                                                                                    |
| win:Reply     | 6     | RESPUESTA DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT     | Evento de respuesta.                                                                                         |
| win:Resume    | 7     | REANUDACIÓN DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT    | Evento que representa una actividad que se reanuda después de ser suspendida.                                   |
| win:Suspend   | 8     | SUSPENSIÓN DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT   | Evento que representa la actividad que se suspende pendiente de la finalización de otra actividad.           |
| win:Send      | 9     | ENVÍO DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT      | Evento que representa la transferencia de actividad a otro componente.                                   |
| win:Receive   | 240   | RECEPCIÓN DE \_ CÓDIGO DE OPERACIÓN DE \_ WINEVENT   | Evento que representa la recepción de una transferencia de actividad desde otro componente.                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





