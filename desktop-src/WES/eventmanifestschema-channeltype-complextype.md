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
# <a name="channeltype-complex-type"></a>Tipo complejo de ChannelType

Define un canal en el que los proveedores pueden registrar eventos.

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

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                                                   | Descripción                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**userenv**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Define las propiedades del archivo de registro que respalda el canal, como su capacidad y si el archivo de registro es secuencial o circular.<br/>                                                         |
| [**edición**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Define las propiedades de registro para la sesión que utiliza el canal. Solo los canales de depuración y de análisis y los canales que utilizan el aislamiento personalizado pueden especificar propiedades de registro para su sesión.<br/> |



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
<td>acceso</td>
<td>string</td>
<td>Un descriptor de acceso de <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">lenguaje de definición de descriptores de seguridad</a> (SDDL) que controla el acceso al archivo de registro que respalda el canal. Si el atributo de <strong>aislamiento</strong> se establece en aplicación o sistema, el descriptor de acceso controla el acceso de lectura al archivo (se omiten los permisos de escritura). Si el atributo de <strong>aislamiento</strong> está establecido en personalizado, el descriptor de acceso controla el acceso de escritura al canal y el acceso de lectura al archivo.<br/></td>
</tr>
<tr class="even">
<td>chid</td>
<td>token</td>
<td>Identificador que identifica de forma única el canal en la lista de canales que el proveedor define o importa. Use este valor cuando haga referencia al canal en un evento. Si no especifica un identificador de canal, utilice el nombre del canal para hacer referencia a este canal en una definición de evento.<br/></td>
</tr>
<tr class="odd">
<td>enabled</td>
<td>boolean</td>
<td>Determina si el canal está habilitado. Establézcalo en <strong>true</strong> para permitir el registro en el canal; en caso contrario, <strong>false</strong>. El valor predeterminado es <strong>false</strong> (el registro está deshabilitado).<br/> Dado que los tipos de canal de depuración y de análisis son canales de gran volumen, debe habilitar el canal solo cuando investigue un problema con un componente que escribe en ese canal. de lo contrario, el canal debe permanecer deshabilitado.<br/> Cada vez que se habilita un canal de depuración y análisis, el servicio borra los eventos del canal.<br/></td>
</tr>
<tr class="even">
<td>aislamiento de</td>
<td>string</td>
<td>El valor de aislamiento define los permisos de acceso predeterminados para el canal. Puede especificar uno de los siguientes valores:
<ul>
<li><strong>Aplicación</strong></li>
<li><strong>Sistema</strong></li>
<li><strong>Personalizada</strong></li>
</ul>
El aislamiento predeterminado es <strong>aplicación</strong>. Los permisos predeterminados para la <strong>aplicación</strong> se muestran mediante SDDL: <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Texto</th>
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

<p>Los permisos predeterminados para el <strong>sistema</strong> son (se muestran mediante SDDL):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Texto</th>
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
<p>Los permisos predeterminados para el aislamiento <strong>personalizado</strong> son los mismos que para la aplicación.</p>
<p>Los canales que especifican el aislamiento de <strong>aplicaciones</strong> usan la misma sesión de ETW. Lo mismo se aplica para el aislamiento <strong>del sistema</strong> . Sin embargo, si especifica el aislamiento <strong>personalizado</strong> , el servicio crea una sesión de ETW independiente para el canal. El uso del aislamiento <strong>personalizado</strong> le permite controlar los permisos de acceso para el canal y el archivo de respaldo. Dado que solo hay disponibles sesiones ETW 64, debe limitar el uso del aislamiento <strong>personalizado</strong> .</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>string</td>
<td><p>Nombre para mostrar localizado del canal. La cadena de mensaje hace referencia a una cadena localizada en la sección <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> del manifiesto.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>Nombre del canal. El nombre debe ser único en la lista de canales que utiliza el proveedor. La Convención para asignar nombres a los canales es anexar el tipo de canal al nombre del proveedor. Por ejemplo. Si el nombre del proveedor es Company-Product-Component y está definiendo un canal operativo, el nombre sería Company-Product-Component/Operational.</p>
<p>Los nombres de canal deben tener menos de 255 caracteres y no pueden contener los siguientes caracteres: ' > ', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>Símbolo que se va a usar para hacer referencia al canal en la aplicación. El <a href="message-compiler--mc-exe-.md"><strong>compilador de mensajes (MC.exe)</strong></a> utiliza el símbolo para crear una constante para el canal en el archivo de encabezado que genera el compilador. Si no especifica un símbolo, el compilador genera el nombre automáticamente.</p></td>
</tr>
<tr class="even">
<td>type</td>
<td>string</td>
<td><p>Identifica el tipo del canal. Puede especificar uno de los siguientes tipos:</p>
<ul>
<li><strong>Administrador</strong></li>
<li><strong>Operativos</strong></li>
<li><strong>Analíticos</strong></li>
<li><strong>Depurar</strong></li>
</ul>
<p>Los canales de tipo administrador admiten eventos dirigidos a usuarios finales, administradores y personal de soporte técnico. Los eventos escritos en los canales de administración deben tener una solución bien definida en la que el administrador pueda actuar. Un ejemplo de evento de administración es un evento que se produce cuando una aplicación no se puede conectar a una impresora. Estos eventos están bien documentados o tienen un mensaje asociado a ellos que proporciona al lector instrucciones directas de lo que se debe hacer para rectificar el problema.</p>
<p>Los canales de tipo operativo admiten eventos que se usan para analizar y diagnosticar un problema o una aparición. Se pueden utilizar para activar herramientas o tareas según el problema o la incidencia. Un ejemplo de un evento operativo es un evento que se produce cuando se agrega o se quita una impresora de un sistema.</p>
<p>Los canales de tipo analítico admiten eventos que se publican en un gran volumen. Describen el funcionamiento del programa e indican los problemas que el usuario no puede administrar.</p>
<p>Los canales de tipo depuración admiten eventos que solo usan los programadores para diagnosticar un problema para la depuración.</p>
<p>Los canales analíticos y de depuración están deshabilitados de forma predeterminada y solo deben habilitarse para determinar la causa de un problema. Por ejemplo, podría habilitar el canal, ejecutar el escenario que está causando el problema, deshabilitar el canal y, a continuación, consultar los eventos. Tenga en cuenta que al habilitar el canal se borra el canal de eventos existentes. Si el canal analítico y de depuración usa un archivo de respaldo circular, debe deshabilitar el canal para consultar sus eventos.</p>
<p>Todos los canales de administración usan la misma sesión de ETW; lo mismo se aplica a los canales operativos. Sin embargo, cada canal analítico y de depuración utiliza una sesión de ETW independiente, que es otra razón para habilitar solo estos tipos de canal cuando sea necesario (hay un número limitado de sesiones de ETW disponibles).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Identificador numérico que identifica de forma única el canal dentro de la lista de canales que define el proveedor. El compilador de mensajes asigna el valor si no se especifica.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Si el nombre del canal sigue la Convención de nomenclatura del canal, el Visor de eventos de Windows mostrará el canal mediante la cadena que sigue a la barra diagonal inversa. Por ejemplo, si el nombre del canal es Company-Product-Component/Operational, el Visor de eventos mostrará el canal como operativo en el proveedor Company-Product-Components. De lo contrario, el nombre del canal completo se muestra en el proveedor. Si se proporciona, se utiliza el nombre para mostrar localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




`
