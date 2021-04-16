---
title: Tipo complejo de EventDefinitionType
description: Define un evento que el proveedor puede escribir.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696054"
---
# <a name="eventdefinitiontype-complex-type"></a>Tipo complejo de EventDefinitionType

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



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>canal</td>
<td>token</td>
<td>Identificador que identifica el canal en el que se escribe el evento. Especifique un identificador de canal de uno de los canales que definió o importó. Si el canal no especifica un identificador de canal, utilice el nombre del canal. Para obtener más información sobre cómo definir o importar un canal, vea el tipo complejo de <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .<br/> Si no especifica un canal, el evento no se escribe en un canal. Normalmente, la única razón para no especificar un canal es si está escribiendo eventos solo en una sesión de ETW. Para obtener más información, vea crear una sesión de ETW, consulte <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controlar sesiones de seguimiento de eventos</a>.<br/></td>
</tr>
<tr class="even">
<td>keywords</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></td>
<td>Lista separada por espacios de nombres de palabras clave que identifican la categoría de eventos a los que pertenece este evento. Especifique un nombre de palabra clave en la lista de palabras clave que defina. Para obtener más información sobre cómo definir palabras clave, vea el tipo complejo de <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .<br/> Si no especifica palabras clave, el descriptor de eventos contendrá un cero para las palabras clave.<br/></td>
</tr>
<tr class="odd">
<td>Nivel</td>
<td><strong>QName</strong></td>
<td>Nivel de detalle que se va a usar al escribir el evento. Especifique el nombre de un nivel que haya definido en el manifiesto o uno de los niveles definidos en el archivo \Include\Winmeta.xml que se incluye en el Windows SDK. Para obtener más información sobre cómo definir un nivel, vea el tipo complejo de <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .<br/> Si no especifica un nivel, el descriptor de eventos contendrá un cero para el nivel.<br/> Debe especificar un nivel si el tipo de canal en el que se escribe el evento es admin; el nivel debe ser uno de los siguientes niveles definidos en Winmeata.xml:
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></td>
<td>El mensaje localizado para el evento. La cadena de mensaje hace referencia a una cadena localizada en la sección <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> del manifiesto.<br/> Debe especificar un mensaje si el tipo de canal en el que se escribe el evento es admin.<br/></td>
</tr>
<tr class="odd">
<td>notLogged</td>
<td>boolean</td>
<td>Determina si el proveedor registra este evento. Especifique true si el proveedor registra este evento; en caso contrario, false. Utilice este atributo para indicar que el proveedor ya no registra este evento en lugar de quitar el evento del manifiesto. Conservar el evento en el manifiesto permitirá a los consumidores descodificar los archivos ETL más antiguos que incluyen el evento.<br/> <strong>Windows Server 2008 y Windows Vista:</strong> Este atributo no se admite en las versiones del compilador de mensajes que se enviaron antes de la versión de Windows 7 del Windows SDK.<br/></td>
</tr>
<tr class="even">
<td>Código</td>
<td><strong>QName</strong></td>
<td>Nombre de un código de operación que identifica una operación dentro de la tarea. Especifique el nombre de un código de operación que haya definido en el manifiesto o uno de los códigos de operación definidos en Winmeta.xml. Para obtener más información sobre cómo definir un código de operación, vea el tipo complejo de <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .<br/> Si la tarea a la que se hace referencia contiene códigos de operación específicos de la tarea (locales), puede especificar uno de sus códigos de operación específicos de la tarea o un código de operación definido en el nivel de proveedor (código de operación global). Si especifica un código de operación global, el valor del código de operación global no puede ser el mismo que uno de los códigos de operación locales de la tarea.<br/> Si hace referencia a un código de operación local, el atributo Task debe hacer referencia a la tarea a la que pertenece el código de operación local.<br/> Si no especifica un código de operación, el descriptor de eventos contendrá un cero para OpCode.<br/></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td>Símbolo que se va a usar para hacer referencia al descriptor de eventos para este evento en la aplicación. El <a href="message-compiler--mc-exe-.md"><strong>compilador de mensajes (MC.exe)</strong></a> utiliza el símbolo para crear una constante para el descriptor de eventos en el archivo de encabezado generado por el compilador. Si no especifica un símbolo, el compilador genera uno automáticamente. El descriptor se usa cuando se llama a la función <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> para escribir el evento.<br/></td>
</tr>
<tr class="even">
<td>task</td>
<td><strong>QName</strong></td>
<td>Nombre de una tarea que identifica el componente o subcomponente que genera este evento. Especifique el nombre de una tarea que haya definido en el manifiesto. Para obtener más información sobre cómo definir una tarea, vea el tipo complejo <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .<br/> Si no especifica una tarea, el descriptor de eventos contendrá un cero para la tarea.<br/></td>
</tr>
<tr class="odd">
<td>template</td>
<td>token</td>
<td>Identificador de plantilla de la plantilla que define los elementos de datos que este evento incluye. Especifique el identificador de la plantilla que ha definido en el manifiesto. Para obtener más información sobre cómo definir una plantilla, vea el tipo complejo de <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>value</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>Identificador de evento. El identificador debe ser único en la lista de eventos que defina.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Número de versión de un byte de la definición del evento.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Si usa [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para dar formato a la cadena de mensaje para el evento (o utiliza el visor de eventos para ver la cadena de mensaje), la cadena de mensaje puede contener cadenas de inserción y cualquiera de las cadenas de formato que admite la función **FormatMessage** de Win32. Las cadenas de inserción están limitadas a%*n* o%*n*! s! (por ejemplo, %1), donde *n* es la referencia basada en uno de los elementos de datos definidos en la plantilla del evento. La cadena de mensaje también puede contener cadenas de inserción de parámetros con el formato%%*n* (por ejemplo,% %4). El número máximo de cadenas de inserción que puede contener el mensaje es 100.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

