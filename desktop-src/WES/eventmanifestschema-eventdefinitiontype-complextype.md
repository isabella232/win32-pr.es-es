---
title: Tipo complejo EventDefinitionType
description: Define un evento que el proveedor puede escribir.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType, tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42959edd4c7f7f49c3ced305b5b9bd1072f721a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482991"
---
# <a name="eventdefinitiontype-complex-type"></a>Tipo complejo EventDefinitionType

Define un evento que el proveedor puede escribir.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos




| Nombre | Tipo | Descripción | 
|------|------|-------------|
| canal | token | Identificador que identifica el canal en el que se escribe el evento. Especifique un identificador de canal de uno de los canales que definió o importó. Si el canal no especifica un identificador de canal, use el nombre del canal. Para más información sobre cómo definir o importar un canal, consulte el tipo complejo <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType.</strong></a><br /> Si no especifica un canal, el evento no se escribe en un canal. Normalmente, la única razón para no especificar un canal es si escribe eventos solo en una sesión ETW. Para obtener más información, consulte Creación de una sesión ETW, vea <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlar sesiones de seguimiento de eventos.</a><br /> | 
| keywords | <a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a> | Lista separada por espacios de nombres de palabra clave que identifican la categoría de eventos a la que pertenece este evento. Especifique un nombre de palabra clave de la lista de palabras clave que defina. Para más información sobre cómo definir palabras clave, consulte el <a href="eventmanifestschema-keywordtype-complextype.md"><strong>tipo complejo KeywordType.</strong></a><br /> Si no especifica palabras clave, el descriptor de eventos contendrá un cero para las palabras clave.<br /> | 
| Nivel | <strong>QName</strong> | Nivel de detalle que se usará al escribir el evento. Especifique el nombre de un nivel definido en el manifiesto o uno de los niveles definidos en el archivo \Include\Winmeta.xml que se incluye en el SDK de Windows. Para más información sobre cómo definir un nivel, consulte el <a href="eventmanifestschema-leveltype-complextype.md"><strong>tipo complejo LevelType.</strong></a><br /> Si no especifica un nivel, el descriptor de eventos contendrá un cero para level.<br /> Debe especificar un nivel si el tipo de canal en el que se escribe el evento es Admin; el nivel debe ser uno de los siguientes niveles definidos en Winmeata.xml:<ul><li>win:Critical</li><li>win:Error</li><li>win:Warning</li><li>win:Informational</li></ul><br /> | 
| message | <a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a> | Mensaje localizado para el evento. La cadena de mensaje hace referencia a una cadena localizada en la <a href="eventmanifestschema-stringtable-resources-element.md"><strong>sección stringTable</strong></a> del manifiesto.<br /> Debe especificar un mensaje si el tipo de canal en el que se escribe el evento es Admin.<br /> | 
| notLogged | boolean | Determina si el proveedor registra este evento. Especifique true si el proveedor registra este evento; de lo contrario, false. Use este atributo para indicar que el proveedor ya no registra este evento en lugar de quitar el evento del manifiesto. Conservar el evento en el manifiesto permitirá a los consumidores descodificar archivos etl anteriores que incluyan el evento.<br /><strong>Windows Server 2008 y Windows Vista:</strong> Este atributo no se admite en las versiones del compilador de mensajes que se incluyeron antes de la versión Windows 7 del SDK de Windows.<br /> | 
| Opcode | <strong>QName</strong> | Nombre de un código de operación que identifica una operación dentro de la tarea. Especifique el nombre de un código de operación definido en el manifiesto o uno de los códigos de operación definidos en Winmeta.xml. Para más información sobre cómo definir un código de operación, consulte el <a href="eventmanifestschema-opcodetype-complextype.md"><strong>tipo complejo OpcodeType.</strong></a><br /> Si la tarea a la que hace referencia contiene códigos de operación específicos de la tarea (local), puede especificar uno de sus códigos de operación específicos de la tarea o un código de operación definido en el nivel de proveedor (un código de operación global). Si especifica un código de operación global, el valor del código de operación global no puede ser el mismo que uno de los códigos de operación locales para la tarea.<br /> Si hace referencia a un código de operación local, el atributo task debe hacer referencia a la tarea a la que pertenece el código de operación local.<br /> Si no especifica un código de operación, el descriptor de eventos contendrá un cero para el código de operación.<br /> | 
| símbolo | <a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a> | Símbolo que se va a usar para hacer referencia al descriptor de eventos para este evento en la aplicación. El <a href="message-compiler--mc-exe-.md"><strong>compilador de mensajes (MC.exe)</strong></a> usa el símbolo para crear una constante para el descriptor de eventos en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente. El descriptor se usa al llamar a la <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>función EventWrite</strong></a> para escribir el evento.<br /> | 
| task | <strong>QName</strong> | Nombre de una tarea que identifica el componente o subcomponente que genera este evento. Especifique el nombre de una tarea que definió en el manifiesto. Para obtener más información sobre cómo definir una tarea, vea el <a href="eventmanifestschema-tasktype-complextype.md"><strong>tipo complejo TaskType.</strong></a><br /> Si no especifica una tarea, el descriptor de eventos contendrá un cero para la tarea.<br /> | 
| template | token | Identificador de plantilla de la plantilla que define los elementos de datos que incluye este evento. Especifique el identificador de una plantilla que definió en el manifiesto. Para más información sobre cómo definir una plantilla, consulte el <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>tipo complejo TemplateItemType.</strong></a><br /> | 
| value | <a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a> | Identificador de evento. El identificador debe ser único dentro de la lista de eventos que defina.<br /> | 
| version | unsignedByte | Número de versión de un byte de la definición de evento.<br /> | 




## <a name="remarks"></a>Comentarios

Si usa [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para dar formato a la cadena de mensaje para el evento (o usa el Visor de eventos para ver la cadena del mensaje), la cadena del mensaje puede contener cadenas de inserción y cualquiera de las cadenas de formato que admite la función **FormatMessage** de Win32. Las cadenas de inserción se limitan a %*n* o %*n*!s! (por ejemplo, %1) donde *n* es la referencia basada en uno los elementos de datos definidos en la plantilla del evento. La cadena de mensaje también puede contener cadenas de inserción de parámetros con el formato %%*n* (por ejemplo, %%4). El número máximo de cadenas de inserción que el mensaje puede contener es 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

