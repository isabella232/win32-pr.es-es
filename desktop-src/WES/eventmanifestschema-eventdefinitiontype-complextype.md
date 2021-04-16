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
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="b9641-104">Tipo complejo de EventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="b9641-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="b9641-105">Define un evento que el proveedor puede escribir.</span><span class="sxs-lookup"><span data-stu-id="b9641-105">Defines an event that your provider can write.</span></span>

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

## <a name="attributes"></a><span data-ttu-id="b9641-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9641-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9641-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9641-107">Name</span></span></th>
<th><span data-ttu-id="b9641-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9641-108">Type</span></span></th>
<th><span data-ttu-id="b9641-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9641-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9641-110">canal</span><span class="sxs-lookup"><span data-stu-id="b9641-110">channel</span></span></td>
<td><span data-ttu-id="b9641-111">token</span><span class="sxs-lookup"><span data-stu-id="b9641-111">token</span></span></td>
<td><span data-ttu-id="b9641-112">Identificador que identifica el canal en el que se escribe el evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="b9641-113">Especifique un identificador de canal de uno de los canales que definió o importó.</span><span class="sxs-lookup"><span data-stu-id="b9641-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="b9641-114">Si el canal no especifica un identificador de canal, utilice el nombre del canal.</span><span class="sxs-lookup"><span data-stu-id="b9641-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="b9641-115">Para obtener más información sobre cómo definir o importar un canal, vea el tipo complejo de <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b9641-116">Si no especifica un canal, el evento no se escribe en un canal.</span><span class="sxs-lookup"><span data-stu-id="b9641-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="b9641-117">Normalmente, la única razón para no especificar un canal es si está escribiendo eventos solo en una sesión de ETW.</span><span class="sxs-lookup"><span data-stu-id="b9641-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="b9641-118">Para obtener más información, vea crear una sesión de ETW, consulte <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controlar sesiones de seguimiento de eventos</a>.</span><span class="sxs-lookup"><span data-stu-id="b9641-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9641-119">keywords</span><span class="sxs-lookup"><span data-stu-id="b9641-119">keywords</span></span></td>
<td><span data-ttu-id="b9641-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9641-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="b9641-121">Lista separada por espacios de nombres de palabras clave que identifican la categoría de eventos a los que pertenece este evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="b9641-122">Especifique un nombre de palabra clave en la lista de palabras clave que defina.</span><span class="sxs-lookup"><span data-stu-id="b9641-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="b9641-123">Para obtener más información sobre cómo definir palabras clave, vea el tipo complejo de <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b9641-124">Si no especifica palabras clave, el descriptor de eventos contendrá un cero para las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="b9641-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9641-125">Nivel</span><span class="sxs-lookup"><span data-stu-id="b9641-125">level</span></span></td>
<td><span data-ttu-id="b9641-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="b9641-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="b9641-127">Nivel de detalle que se va a usar al escribir el evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="b9641-128">Especifique el nombre de un nivel que haya definido en el manifiesto o uno de los niveles definidos en el archivo \Include\Winmeta.xml que se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b9641-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="b9641-129">Para obtener más información sobre cómo definir un nivel, vea el tipo complejo de <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b9641-130">Si no especifica un nivel, el descriptor de eventos contendrá un cero para el nivel.</span><span class="sxs-lookup"><span data-stu-id="b9641-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="b9641-131">Debe especificar un nivel si el tipo de canal en el que se escribe el evento es admin; el nivel debe ser uno de los siguientes niveles definidos en Winmeata.xml:</span><span class="sxs-lookup"><span data-stu-id="b9641-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="b9641-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="b9641-132">win:Critical</span></span></li>
<li><span data-ttu-id="b9641-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="b9641-133">win:Error</span></span></li>
<li><span data-ttu-id="b9641-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="b9641-134">win:Warning</span></span></li>
<li><span data-ttu-id="b9641-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="b9641-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9641-136">message</span><span class="sxs-lookup"><span data-stu-id="b9641-136">message</span></span></td>
<td><span data-ttu-id="b9641-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9641-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="b9641-138">El mensaje localizado para el evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-138">The localized message for the event.</span></span> <span data-ttu-id="b9641-139">La cadena de mensaje hace referencia a una cadena localizada en la sección <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b9641-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="b9641-140">Debe especificar un mensaje si el tipo de canal en el que se escribe el evento es admin.</span><span class="sxs-lookup"><span data-stu-id="b9641-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9641-141">notLogged</span><span class="sxs-lookup"><span data-stu-id="b9641-141">notLogged</span></span></td>
<td><span data-ttu-id="b9641-142">boolean</span><span class="sxs-lookup"><span data-stu-id="b9641-142">boolean</span></span></td>
<td><span data-ttu-id="b9641-143">Determina si el proveedor registra este evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="b9641-144">Especifique true si el proveedor registra este evento; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="b9641-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="b9641-145">Utilice este atributo para indicar que el proveedor ya no registra este evento en lugar de quitar el evento del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b9641-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="b9641-146">Conservar el evento en el manifiesto permitirá a los consumidores descodificar los archivos ETL más antiguos que incluyen el evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="b9641-147"><strong>Windows Server 2008 y Windows Vista:</strong> Este atributo no se admite en las versiones del compilador de mensajes que se enviaron antes de la versión de Windows 7 del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b9641-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9641-148">Código</span><span class="sxs-lookup"><span data-stu-id="b9641-148">opcode</span></span></td>
<td><span data-ttu-id="b9641-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="b9641-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="b9641-150">Nombre de un código de operación que identifica una operación dentro de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9641-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="b9641-151">Especifique el nombre de un código de operación que haya definido en el manifiesto o uno de los códigos de operación definidos en Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="b9641-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="b9641-152">Para obtener más información sobre cómo definir un código de operación, vea el tipo complejo de <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b9641-153">Si la tarea a la que se hace referencia contiene códigos de operación específicos de la tarea (locales), puede especificar uno de sus códigos de operación específicos de la tarea o un código de operación definido en el nivel de proveedor (código de operación global).</span><span class="sxs-lookup"><span data-stu-id="b9641-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="b9641-154">Si especifica un código de operación global, el valor del código de operación global no puede ser el mismo que uno de los códigos de operación locales de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9641-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="b9641-155">Si hace referencia a un código de operación local, el atributo Task debe hacer referencia a la tarea a la que pertenece el código de operación local.</span><span class="sxs-lookup"><span data-stu-id="b9641-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="b9641-156">Si no especifica un código de operación, el descriptor de eventos contendrá un cero para OpCode.</span><span class="sxs-lookup"><span data-stu-id="b9641-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9641-157">símbolo</span><span class="sxs-lookup"><span data-stu-id="b9641-157">symbol</span></span></td>
<td><span data-ttu-id="b9641-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9641-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="b9641-159">Símbolo que se va a usar para hacer referencia al descriptor de eventos para este evento en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b9641-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="b9641-160">El <a href="message-compiler--mc-exe-.md"><strong>compilador de mensajes (MC.exe)</strong></a> utiliza el símbolo para crear una constante para el descriptor de eventos en el archivo de encabezado generado por el compilador.</span><span class="sxs-lookup"><span data-stu-id="b9641-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="b9641-161">Si no especifica un símbolo, el compilador genera uno automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b9641-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="b9641-162">El descriptor se usa cuando se llama a la función <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> para escribir el evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9641-163">task</span><span class="sxs-lookup"><span data-stu-id="b9641-163">task</span></span></td>
<td><span data-ttu-id="b9641-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="b9641-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="b9641-165">Nombre de una tarea que identifica el componente o subcomponente que genera este evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="b9641-166">Especifique el nombre de una tarea que haya definido en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b9641-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="b9641-167">Para obtener más información sobre cómo definir una tarea, vea el tipo complejo <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b9641-168">Si no especifica una tarea, el descriptor de eventos contendrá un cero para la tarea.</span><span class="sxs-lookup"><span data-stu-id="b9641-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9641-169">template</span><span class="sxs-lookup"><span data-stu-id="b9641-169">template</span></span></td>
<td><span data-ttu-id="b9641-170">token</span><span class="sxs-lookup"><span data-stu-id="b9641-170">token</span></span></td>
<td><span data-ttu-id="b9641-171">Identificador de plantilla de la plantilla que define los elementos de datos que este evento incluye.</span><span class="sxs-lookup"><span data-stu-id="b9641-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="b9641-172">Especifique el identificador de la plantilla que ha definido en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b9641-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="b9641-173">Para obtener más información sobre cómo definir una plantilla, vea el tipo complejo de <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9641-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9641-174">value</span><span class="sxs-lookup"><span data-stu-id="b9641-174">value</span></span></td>
<td><span data-ttu-id="b9641-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9641-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="b9641-176">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-176">The event identifier.</span></span> <span data-ttu-id="b9641-177">El identificador debe ser único en la lista de eventos que defina.</span><span class="sxs-lookup"><span data-stu-id="b9641-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9641-178">version</span><span class="sxs-lookup"><span data-stu-id="b9641-178">version</span></span></td>
<td><span data-ttu-id="b9641-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b9641-179">unsignedByte</span></span></td>
<td><span data-ttu-id="b9641-180">Número de versión de un byte de la definición del evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b9641-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9641-181">Remarks</span></span>

<span data-ttu-id="b9641-182">Si usa [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para dar formato a la cadena de mensaje para el evento (o utiliza el visor de eventos para ver la cadena de mensaje), la cadena de mensaje puede contener cadenas de inserción y cualquiera de las cadenas de formato que admite la función **FormatMessage** de Win32.</span><span class="sxs-lookup"><span data-stu-id="b9641-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="b9641-183">Las cadenas de inserción están limitadas a%*n* o%*n*! s!</span><span class="sxs-lookup"><span data-stu-id="b9641-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="b9641-184">(por ejemplo, %1), donde *n* es la referencia basada en uno de los elementos de datos definidos en la plantilla del evento.</span><span class="sxs-lookup"><span data-stu-id="b9641-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="b9641-185">La cadena de mensaje también puede contener cadenas de inserción de parámetros con el formato%%*n* (por ejemplo,% %4).</span><span class="sxs-lookup"><span data-stu-id="b9641-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="b9641-186">El número máximo de cadenas de inserción que puede contener el mensaje es 100.</span><span class="sxs-lookup"><span data-stu-id="b9641-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9641-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9641-187">Requirements</span></span>



| <span data-ttu-id="b9641-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9641-188">Requirement</span></span> | <span data-ttu-id="b9641-189">Value</span><span class="sxs-lookup"><span data-stu-id="b9641-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9641-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9641-190">Minimum supported client</span></span><br/> | <span data-ttu-id="b9641-191">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b9641-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9641-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9641-192">Minimum supported server</span></span><br/> | <span data-ttu-id="b9641-193">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9641-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

