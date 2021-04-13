---
title: Tipo complejo de ChannelType
description: Define un canal en el que los proveedores pueden registrar eventos.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- ChannelType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492035"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="2359f-104">Tipo complejo de ChannelType</span><span class="sxs-lookup"><span data-stu-id="2359f-104">ChannelType Complex Type</span></span>

<span data-ttu-id="2359f-105">Define un canal en el que los proveedores pueden registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="2359f-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2359f-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2359f-106">Child elements</span></span>



| <span data-ttu-id="2359f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2359f-107">Element</span></span>                                                                  | <span data-ttu-id="2359f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2359f-108">Type</span></span>                                                                                   | <span data-ttu-id="2359f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2359f-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2359f-110">**userenv**</span><span class="sxs-lookup"><span data-stu-id="2359f-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="2359f-111">**ChannelLoggingType**</span><span class="sxs-lookup"><span data-stu-id="2359f-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="2359f-112">Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si el archivo de registro es secuencial o circular.</span><span class="sxs-lookup"><span data-stu-id="2359f-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="2359f-113">**edición**</span><span class="sxs-lookup"><span data-stu-id="2359f-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="2359f-114">**ChannelPublishingType**</span><span class="sxs-lookup"><span data-stu-id="2359f-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="2359f-115">Define las propiedades de registro para la sesión que utiliza el canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="2359f-116">Solo los canales de depuración y de análisis y los canales que utilizan el aislamiento personalizado pueden especificar propiedades de registro para su sesión.</span><span class="sxs-lookup"><span data-stu-id="2359f-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2359f-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="2359f-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2359f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2359f-118">Name</span></span></th>
<th><span data-ttu-id="2359f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="2359f-119">Type</span></span></th>
<th><span data-ttu-id="2359f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2359f-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2359f-121">acceso</span><span class="sxs-lookup"><span data-stu-id="2359f-121">access</span></span></td>
<td><span data-ttu-id="2359f-122">string</span><span class="sxs-lookup"><span data-stu-id="2359f-122">string</span></span></td>
<td><span data-ttu-id="2359f-123">Un descriptor de acceso de <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">lenguaje de definición de descriptores de seguridad</a> (SDDL) que controla el acceso al archivo de registro que respalda el canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="2359f-124">Si el atributo de <strong>aislamiento</strong> se establece en aplicación o sistema, el descriptor de acceso controla el acceso de lectura al archivo (se omiten los permisos de escritura).</span><span class="sxs-lookup"><span data-stu-id="2359f-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="2359f-125">Si el atributo de <strong>aislamiento</strong> está establecido en personalizado, el descriptor de acceso controla el acceso de escritura al canal y el acceso de lectura al archivo.</span><span class="sxs-lookup"><span data-stu-id="2359f-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2359f-126">chid</span><span class="sxs-lookup"><span data-stu-id="2359f-126">chid</span></span></td>
<td><span data-ttu-id="2359f-127">token</span><span class="sxs-lookup"><span data-stu-id="2359f-127">token</span></span></td>
<td><span data-ttu-id="2359f-128">Identificador que identifica de forma única el canal en la lista de canales que el proveedor define o importa.</span><span class="sxs-lookup"><span data-stu-id="2359f-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="2359f-129">Use este valor cuando haga referencia al canal en un evento.</span><span class="sxs-lookup"><span data-stu-id="2359f-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="2359f-130">Si no especifica un identificador de canal, utilice el nombre del canal para hacer referencia a este canal en una definición de evento.</span><span class="sxs-lookup"><span data-stu-id="2359f-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2359f-131">enabled</span><span class="sxs-lookup"><span data-stu-id="2359f-131">enabled</span></span></td>
<td><span data-ttu-id="2359f-132">boolean</span><span class="sxs-lookup"><span data-stu-id="2359f-132">boolean</span></span></td>
<td><span data-ttu-id="2359f-133">Determina si el canal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2359f-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="2359f-134">Establézcalo en <strong>true</strong> para permitir el registro en el canal; en caso contrario, <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="2359f-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="2359f-135">El valor predeterminado es <strong>false</strong> (el registro está deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="2359f-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="2359f-136">Dado que los tipos de canal de depuración y de análisis son canales de gran volumen, debe habilitar el canal solo cuando investigue un problema con un componente que escribe en ese canal. de lo contrario, el canal debe permanecer deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2359f-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="2359f-137">Cada vez que se habilita un canal de depuración y análisis, el servicio borra los eventos del canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2359f-138">aislamiento de</span><span class="sxs-lookup"><span data-stu-id="2359f-138">isolation</span></span></td>
<td><span data-ttu-id="2359f-139">string</span><span class="sxs-lookup"><span data-stu-id="2359f-139">string</span></span></td>
<td><span data-ttu-id="2359f-140">El valor de aislamiento define los permisos de acceso predeterminados para el canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="2359f-141">Puede especificar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2359f-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="2359f-142"><strong>Aplicación</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="2359f-143"><strong>Sistema</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="2359f-144"><strong>Personalizada</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="2359f-145">El aislamiento predeterminado es <strong>aplicación</strong>.</span><span class="sxs-lookup"><span data-stu-id="2359f-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="2359f-146">Los permisos predeterminados para la <strong>aplicación</strong> se muestran mediante SDDL:</span><span class="sxs-lookup"><span data-stu-id="2359f-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2359f-147">Texto</span><span class="sxs-lookup"><span data-stu-id="2359f-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="2359f-148">Los permisos predeterminados para el <strong>sistema</strong> son (se muestran mediante SDDL):</span><span class="sxs-lookup"><span data-stu-id="2359f-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2359f-149">Texto</span><span class="sxs-lookup"><span data-stu-id="2359f-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="2359f-150">Los permisos predeterminados para el aislamiento <strong>personalizado</strong> son los mismos que para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2359f-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="2359f-151">Los canales que especifican el aislamiento de <strong>aplicaciones</strong> usan la misma sesión de ETW.</span><span class="sxs-lookup"><span data-stu-id="2359f-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="2359f-152">Lo mismo se aplica para el aislamiento <strong>del sistema</strong> .</span><span class="sxs-lookup"><span data-stu-id="2359f-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="2359f-153">Sin embargo, si especifica el aislamiento <strong>personalizado</strong> , el servicio crea una sesión de ETW independiente para el canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="2359f-154">El uso del aislamiento <strong>personalizado</strong> le permite controlar los permisos de acceso para el canal y el archivo de respaldo.</span><span class="sxs-lookup"><span data-stu-id="2359f-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="2359f-155">Dado que solo hay disponibles sesiones ETW 64, debe limitar el uso del aislamiento <strong>personalizado</strong> .</span><span class="sxs-lookup"><span data-stu-id="2359f-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2359f-156">message</span><span class="sxs-lookup"><span data-stu-id="2359f-156">message</span></span></td>
<td><span data-ttu-id="2359f-157">string</span><span class="sxs-lookup"><span data-stu-id="2359f-157">string</span></span></td>
<td><p><span data-ttu-id="2359f-158">Nombre para mostrar localizado del canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-158">The localized display name for the channel.</span></span> <span data-ttu-id="2359f-159">La cadena de mensaje hace referencia a una cadena localizada en la sección <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="2359f-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2359f-160">name</span><span class="sxs-lookup"><span data-stu-id="2359f-160">name</span></span></td>
<td><span data-ttu-id="2359f-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="2359f-161">anyURI</span></span></td>
<td><p><span data-ttu-id="2359f-162">Nombre del canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-162">The name of the channel.</span></span> <span data-ttu-id="2359f-163">El nombre debe ser único en la lista de canales que utiliza el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2359f-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="2359f-164">La Convención para asignar nombres a los canales es anexar el tipo de canal al nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2359f-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="2359f-165">Por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2359f-165">For example.</span></span> <span data-ttu-id="2359f-166">Si el nombre del proveedor es Company-Product-Component y está definiendo un canal operativo, el nombre sería Company-Product-Component/Operational.</span><span class="sxs-lookup"><span data-stu-id="2359f-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="2359f-167">Los nombres de canal deben tener menos de 255 caracteres y no pueden contener los siguientes caracteres: ' > ', '</span><span class="sxs-lookup"><span data-stu-id="2359f-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2359f-168">símbolo</span><span class="sxs-lookup"><span data-stu-id="2359f-168">symbol</span></span></td>
<td><span data-ttu-id="2359f-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="2359f-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="2359f-170">Símbolo que se va a usar para hacer referencia al canal en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2359f-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="2359f-171">El <a href="message-compiler--mc-exe-.md"><strong>compilador de mensajes (MC.exe)</strong></a> utiliza el símbolo para crear una constante para el canal en el archivo de encabezado que genera el compilador.</span><span class="sxs-lookup"><span data-stu-id="2359f-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="2359f-172">Si no especifica un símbolo, el compilador genera el nombre automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2359f-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2359f-173">type</span><span class="sxs-lookup"><span data-stu-id="2359f-173">type</span></span></td>
<td><span data-ttu-id="2359f-174">string</span><span class="sxs-lookup"><span data-stu-id="2359f-174">string</span></span></td>
<td><p><span data-ttu-id="2359f-175">Identifica el tipo del canal.</span><span class="sxs-lookup"><span data-stu-id="2359f-175">Identifies the channel's type.</span></span> <span data-ttu-id="2359f-176">Puede especificar uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="2359f-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="2359f-177"><strong>Administrador</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="2359f-178"><strong>Operativos</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="2359f-179"><strong>Analíticos</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="2359f-180"><strong>Depurar</strong></span><span class="sxs-lookup"><span data-stu-id="2359f-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="2359f-181">Los canales de tipo administrador admiten eventos dirigidos a usuarios finales, administradores y personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="2359f-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="2359f-182">Los eventos escritos en los canales de administración deben tener una solución bien definida en la que el administrador pueda actuar. Un ejemplo de evento de administración es un evento que se produce cuando una aplicación no se puede conectar a una impresora.</span><span class="sxs-lookup"><span data-stu-id="2359f-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="2359f-183">Estos eventos están bien documentados o tienen un mensaje asociado a ellos que proporciona al lector instrucciones directas de lo que se debe hacer para rectificar el problema.</span><span class="sxs-lookup"><span data-stu-id="2359f-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="2359f-184">Los canales de tipo operativo admiten eventos que se usan para analizar y diagnosticar un problema o una aparición.</span><span class="sxs-lookup"><span data-stu-id="2359f-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="2359f-185">Se pueden utilizar para activar herramientas o tareas según el problema o la incidencia.</span><span class="sxs-lookup"><span data-stu-id="2359f-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="2359f-186">Un ejemplo de un evento operativo es un evento que se produce cuando se agrega o se quita una impresora de un sistema.</span><span class="sxs-lookup"><span data-stu-id="2359f-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="2359f-187">Los canales de tipo analítico admiten eventos que se publican en un gran volumen.</span><span class="sxs-lookup"><span data-stu-id="2359f-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="2359f-188">Describen el funcionamiento del programa e indican los problemas que el usuario no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="2359f-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="2359f-189">Los canales de tipo depuración admiten eventos que solo usan los programadores para diagnosticar un problema para la depuración.</span><span class="sxs-lookup"><span data-stu-id="2359f-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="2359f-190">Los canales analíticos y de depuración están deshabilitados de forma predeterminada y solo deben habilitarse para determinar la causa de un problema.</span><span class="sxs-lookup"><span data-stu-id="2359f-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="2359f-191">Por ejemplo, podría habilitar el canal, ejecutar el escenario que está causando el problema, deshabilitar el canal y, a continuación, consultar los eventos.</span><span class="sxs-lookup"><span data-stu-id="2359f-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="2359f-192">Tenga en cuenta que al habilitar el canal se borra el canal de eventos existentes.</span><span class="sxs-lookup"><span data-stu-id="2359f-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="2359f-193">Si el canal analítico y de depuración usa un archivo de respaldo circular, debe deshabilitar el canal para consultar sus eventos.</span><span class="sxs-lookup"><span data-stu-id="2359f-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="2359f-194">Todos los canales de administración usan la misma sesión de ETW; lo mismo se aplica a los canales operativos.</span><span class="sxs-lookup"><span data-stu-id="2359f-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="2359f-195">Sin embargo, cada canal analítico y de depuración utiliza una sesión de ETW independiente, que es otra razón para habilitar solo estos tipos de canal cuando sea necesario (hay un número limitado de sesiones de ETW disponibles).</span><span class="sxs-lookup"><span data-stu-id="2359f-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2359f-196">value</span><span class="sxs-lookup"><span data-stu-id="2359f-196">value</span></span></td>
<td><span data-ttu-id="2359f-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="2359f-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="2359f-198">Identificador numérico que identifica de forma única el canal dentro de la lista de canales que define el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2359f-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="2359f-199">El compilador de mensajes asigna el valor si no se especifica.</span><span class="sxs-lookup"><span data-stu-id="2359f-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="2359f-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2359f-200">Remarks</span></span>

<span data-ttu-id="2359f-201">Si el nombre del canal sigue la Convención de nomenclatura del canal, el Visor de eventos de Windows mostrará el canal mediante la cadena que sigue a la barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="2359f-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="2359f-202">Por ejemplo, si el nombre del canal es Company-Product-Component/Operational, el Visor de eventos mostrará el canal como operativo en el proveedor Company-Product-Components.</span><span class="sxs-lookup"><span data-stu-id="2359f-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="2359f-203">De lo contrario, el nombre del canal completo se muestra en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2359f-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="2359f-204">Si se proporciona, se utiliza el nombre para mostrar localizado.</span><span class="sxs-lookup"><span data-stu-id="2359f-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="2359f-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2359f-205">Requirements</span></span>



| <span data-ttu-id="2359f-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="2359f-206">Requirement</span></span> | <span data-ttu-id="2359f-207">Value</span><span class="sxs-lookup"><span data-stu-id="2359f-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2359f-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2359f-208">Minimum supported client</span></span><br/> | <span data-ttu-id="2359f-209">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2359f-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2359f-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2359f-210">Minimum supported server</span></span><br/> | <span data-ttu-id="2359f-211">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2359f-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
