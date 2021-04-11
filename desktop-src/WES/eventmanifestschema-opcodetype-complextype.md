---
title: Tipo complejo de OpcodeType
description: Define una operación dentro de un componente de la aplicación.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType tipo complejo EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151067"
---
# <a name="opcodetype-complex-type"></a>Tipo complejo de OpcodeType

Define una operación dentro de un componente de la aplicación. Se usa junto con una tarea para identificar la sección de la aplicación que está registrando el evento.

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
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nombre para mostrar localizado del código de operación. La cadena de mensaje hace referencia a una cadena localizada en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Reservado para uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Nombre del código de operación. Este nombre debe ser único dentro del ámbito de este proveedor. <br/>                                                                                                                                                                                                                      |
| símbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Símbolo que se va a usar para hacer referencia al código de operación en la aplicación. El [**compilador de mensajes (MC.exe)**](message-compiler--mc-exe-.md) utiliza el símbolo para crear una constante para el código de operación en el archivo de encabezado generado por el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valor de código de operación. Puede especificar valores en el rango 10 y 239. Para obtener una lista de valores de código de operación predefinidos, vea la sección Comentarios.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Observaciones

A continuación se muestran los valores de código de operación predefinidos que puede usar. Estos valores se definen en el archivo Winmeta.xml que se incluye en el Windows SDK.



| Nombre          | Value | Símbolo                      | Descripción                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| Win: info      | 0     | información de código de operación de WINEVENT \_ \_      | Evento de información.                                                                                |
| Win: Inicio     | 1     | \_Inicio del código de operación WINEVENT \_     | Un evento que representa el inicio de una actividad.                                                         |
| Win: detener      | 2     | \_detención del código de operación WINEVENT \_      | Un evento que representa la detención de una actividad. El evento corresponde al último evento de inicio no emparejado. |
| Win: Inicio de DC \_ | 3     | Inicio de WINEVENT \_ OPCODE de \_ DC \_ | Evento que representa el inicio de la recolección de datos. Estos son los tipos de evento de detención.                      |
| Win: detención de DC \_  | 4     | detención de DC del código de \_ operación WINEVENT \_ \_  | Evento que representa la detención de la recopilación de datos. Estos son los tipos de evento de detención.                      |
| Win: extensión | 5     | WINEVENT ( \_ extensión de código de operación) \_ | Evento de extensión.                                                                                    |
| Win: responder     | 6     | \_respuesta de código de operación WINEVENT \_     | Un evento de respuesta.                                                                                         |
| Win: currículum    | 7     | \_reanudación del código de operación WINEVENT \_    | Un evento que representa una actividad que se reanuda después de suspenderse.                                   |
| Win: suspender   | 8     | \_suspender código de operación WINEVENT \_   | Evento que representa la actividad que se va a suspender pendiente de la finalización de otra actividad.           |
| Win: enviar      | 9     | WINEVENT \_ envío de código de operación \_      | Evento que representa la transferencia de la actividad a otro componente.                                   |
| Win: Receive   | 240   | WINEVENT de \_ código de operación \_ recibida   | Evento que representa la recepción de una transferencia de actividad desde otro componente.                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





