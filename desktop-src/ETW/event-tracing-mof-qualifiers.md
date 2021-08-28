---
description: Use los calificadores definidos en esta sección al crear la clase MOF del proveedor, la clase MOF de evento, la clase MOF del tipo de evento y las propiedades de la clase MOF del tipo de evento.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Calificadores MOF de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 578699b04c5ba2d0f39afb2e8ff5141151bd208b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628444"
---
# <a name="event-tracing-mof-qualifiers"></a>Calificadores MOF de seguimiento de eventos

Use los calificadores definidos en esta sección al crear la clase [MOF](#provider-mof-class-qualifiers)del proveedor , la clase [MOF](#event-mof-class-qualifiers)de evento , la clase [MOF](#event-type-mof-class-qualifiers)del tipo de evento y las propiedades de la clase [MOF](#property-qualifiers)del tipo de evento . Para obtener un ejemplo que incluya algunos de estos calificadores, vea [Publishing Your Event Schema](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>Calificadores de clase MOF del proveedor

En la tabla siguiente se enumeran los calificadores que puede especificar en una clase MOF del proveedor.



| Qualifier | Tipo de datos  | Descripción                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **String** | Necesario. Guid de cadena que identifica de forma única un proveedor. Por ejemplo, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Se trata del mismo GUID que se usa al llamar a la [**función RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar el proveedor. |



 

## <a name="event-mof-class-qualifiers"></a>Calificadores de clase MOF de eventos

En la tabla siguiente se enumeran los calificadores que puede especificar en una clase de evento (la clase primaria que agrupa las clases de tipo de evento relacionadas).

| Qualifier        | Tipo de datos   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **String**  | Necesario. Guid de cadena que identifica una clase de eventos. Por ejemplo, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Los proveedores de eventos usan el GUID para establecer [**el ENCABEZADO DE SEGUIMIENTO DE \_ \_ EVENTOS. Miembro**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) GUID, para que los consumidores puedan determinar la clase de eventos que reciben.                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **Entero** | Este calificador es opcional para la versión más reciente de una clase de seguimiento de eventos y es necesario para todas las versiones anteriores de la clase. La versión más reciente de la clase no especifica el **calificador EventVersion** o tiene el número de versión más alto. Los números de versión comienzan por 0, por ejemplo, EventVersion(0). Normalmente, cuando se crea una nueva versión de la clase , también se cambia el nombre de la versión anterior a Vn, donde n es un número incremental a partir <classname> \_ de 0. Para obtener un ejemplo, [**vea FileIo**](fileio.md) y [**FileIo \_ V0.**](fileio-v0.md)<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>Calificadores de clase MOF de tipo de evento

En la tabla siguiente se enumeran los calificadores que puede especificar en una clase de tipo de evento (la clase que define los datos de la propiedad de evento).



| Qualifier         | Value       | Descripción                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Entero** | Necesario. Identifica la clase de tipo de evento. Por ejemplo, EventType(1). El proveedor de eventos usa el mismo valor de tipo de evento para establecer [**EVENT \_ TRACE \_ HEADER. Class.Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Si se usa la misma clase MOF para varios tipos de eventos (porque usan los mismos datos de evento), especifique el valor del tipo de evento como una matriz de enteros, por ejemplo, EventType {12,15} . |
| **EventTypeName** | **String**  | Opcional. Describe el tipo de evento. Por ejemplo, EventTypeName("Start"). Si se usa la misma clase MOF para varios tipos de eventos (porque usan los mismos datos de evento), especifique el valor del nombre del tipo de evento como una matriz de cadenas, por ejemplo, EventTypeName{"Start", "End"}. Los elementos de la matriz EventTypeName corresponden directamente a la matriz EventType.                 |



 

## <a name="property-qualifiers"></a>Calificadores de propiedad

En la tabla siguiente se enumeran los calificadores que puede especificar en una propiedad.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Qualifier</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bits</strong></td>
<td>Especifica las posiciones de bits que se asignan a valores de cadena. Si especifica este calificador, también debe especificar el <strong>calificador BitValues.</strong></td>
</tr>
<tr class="even">
<td><strong>BitValues</strong></td>
<td>Valores de cadena. Si también se especifica el calificador <strong>BitMap,</strong> las cadenas se corresponden directamente con los valores del <strong>calificador BitMap.</strong> De lo contrario, suponga que el valor de propiedad es un índice basado en una en las cadenas de valor (el bit uno corresponde a la primera cadena de la lista).</td>
</tr>
<tr class="odd">
<td><strong>Extensión</strong></td>
<td>Proporciona información adicional sobre cómo consumir (interpretar) los datos. El valor de extensión no tiene en cuenta las mayúsculas y minúsculas. Incluya el valor entre comillas, por ejemplo, Extension( &quot; Guid &quot; ). Los valores de extensión posibles son: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> <dd> Indica que los datos de propiedad son guid. El tipo de datos MOF debe ser <strong>el objeto</strong>. Se espera que la carga sea una <strong>estructura GUID.</strong><br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr e IPAddrV4</dt> <dd> Los datos son una dirección IP V4. El tipo de datos MOF debe ser <strong>el objeto</strong>. Se espera que la carga sea larga sin signo. Cada byte del largo sin signo representa una de las cuatro partes de la dirección IP (p1.p2.p3.p4). El byte de orden bajo contiene el valor de p1, el byte siguiente contiene el valor de p2, y así sucesivamente.<br/> <strong>Antes de Windows Vista:</strong> No se admite la extensión IPAddrV4.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Los datos son una dirección IP V6. El tipo de datos MOF debe ser <strong>el objeto</strong>. Se espera que la carga sea una <strong>IN6_ADDR</strong> estructura. <br/> <strong>Antes de Windows Vista:</strong> No se admite la extensión IPAddrV6.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> <dd> Indica que el consumidor no debe imprimir estos datos.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Puerto</dt> <dd> Los datos identifican un número de puerto. El tipo de datos MOF debe ser <strong>el objeto</strong>. Se espera que la carga sea un short sin signo.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> Los caracteres de nueva línea se reemplazaron por espacios. Se espera que la carga sea una cadena ANSI terminada en NULL.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> Los caracteres de nueva línea se reemplazaron por espacios. Se espera que la carga sea una cadena de caracteres anchos terminada en NULL.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> <dd> Los datos representan un SID de blob binario. El tipo de datos MOF debe ser <strong>el objeto</strong>. <br/> El SID tiene una longitud variable. El valor contenido en los primeros 4 bytes<strong>(ULONG)</strong>indica si el blob contiene un SID. Si los primeros 4 bytes<strong>(ULONG)</strong>del blob son distintos de cero, el blob contiene un SID. La primera parte del blob contiene el TOKEN_USER (la estructura está alineada en un límite de 8 bytes) y la segunda parte contiene el SID. Para solucionar la parte del SID del blob:<br/>
<ul>
<li>Establecer un puntero de bytes al principio del blob</li>
<li>Multiplique el tamaño del puntero para el registro de eventos por 2 y agregue el producto al puntero de bytes (el <strong>miembro PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> contiene el valor de tamaño del puntero)</li>
</ul>
<br/> Puede usar la macro siguiente para determinar la longitud del SID. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Indica que la propiedad contiene un valor de puntero. El tamaño del valor del puntero depende del sistema operativo utilizado para registrar el evento. la carga contendrá un valor de 4 bytes para sistemas de 32 bits o un valor de 8 bytes para sistemas de 64 bits. El tipo de datos MOF debe ser <strong>el objeto</strong>.<br/> Los consumidores deben omitir el tipo de datos y <strong>el calificador Format</strong> si la propiedad incluye la <strong>extensión SizeT.</strong> Para determinar el tamaño de los datos que se leerán para la propiedad , use:
<ul>
<li>Miembro <strong>PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Miembro <strong>Flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>Antes de Windows Vista:</strong> Es posible que el valor <strong>PointerSize</strong> no sea preciso. Por ejemplo, en un equipo de 64 bits, una aplicación de 32 bits registrará punteros de 4 bytes; sin embargo, la sesión establecerá <strong>PointerSize</strong> en 8.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Variante</dt> <dd> Los datos representan un blob. Los cuatro primeros bytes (uint32) indican el tamaño del blob. El tipo de datos MOF debe ser <strong>el objeto</strong>. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> <dd> Traduce la marca de tiempo a la hora del sistema. El tipo de datos MOF debe ser <strong>el objeto</strong>. Se espera que la carga sea un entero de 64 bits sin signo.<br/> <strong>Antes de Windows Vista:</strong> No disponible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Format</strong></td>
<td>Define el formato de los datos de propiedad. Por ejemplo, incluir Format( &quot; w ) en una propiedad de cadena indica que la cadena es una cadena &quot; ancha. Los valores posibles son:
<table>
<thead>
<tr class="header">
<th>Término</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>C<br/></td>
<td>Muestra el valor de propiedad como un carácter ASCII. Puede usar este calificador con tipos <strong>de datos uint8.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>s<br/></td>
<td>Trate la matriz de caracteres como una cadena terminada en NULL. La cadena es una cadena de caracteres anchos si el tipo de datos es <strong>char16</strong>; De lo contrario, la cadena es una cadena de caracteres ASCII.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>W<br/></td>
<td>El valor de propiedad es una cadena de caracteres anchos. Puede usar este calificador con tipos <strong>de datos de</strong> cadena. <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>X<br/></td>
<td>Muestra el valor de propiedad como un número hexadecimal. Puede usar este calificador con tipos de datos enteros de 16, 32 y 64 bits.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Puntero</strong></td>
<td><p>Indica que la propiedad contiene un valor de puntero. El tamaño del valor del puntero depende del sistema operativo utilizado para registrar el evento. la carga contendrá un valor de 4 bytes para sistemas de 32 bits o un valor de 8 bytes para sistemas de 64 bits. El tipo de datos MOF debe ser <strong>el objeto</strong>.</p>
<p>Los consumidores deben omitir el tipo de datos y <strong>el calificador Format</strong> si la propiedad incluye la <strong>extensión SizeT.</strong> Para determinar el tamaño de los datos que se leerán para la propiedad , use:</p>
<ul>
<li>Miembro <strong>PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Miembro <strong>Flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>Antes de Windows Vista:</strong> Es posible que el valor <strong>PointerSize</strong> no sea preciso. Por ejemplo, en un equipo de 64 bits, una aplicación de 32 bits registrará punteros de 4 bytes; sin embargo, la sesión establecerá <strong>PointerSize</strong> en 8.</p>
<p>Tenga en cuenta que algunos eventos <strong>usan PointerType en</strong> lugar de <strong>Pointer</strong>; no use <strong>PointerType</strong>.</p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>Indica cómo finaliza la propiedad de cadena. Por ejemplo, StringTermination( &quot; NullTerminated &quot; ) indica que la propiedad de cadena termina en NULL. Los valores posibles son:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Contado</strong></dt> <dd>
<p>La longitud de la cadena se incrusta al principio de la cadena como <strong>un valor USHORT.</strong></p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> <dd>
<p>La cadena no termina en NULL y la longitud de la cadena no se incrusta al principio de la cadena. En este caso, la cadena debe ser el último elemento y ocupar todo el espacio hasta el final de los datos del evento.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>La cadena termina en NULL. Si no especifica el <strong>calificador StringTermination,</strong> se supone que la cadena termina en NULL.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>La longitud de la cadena se incrusta al principio de la cadena como un valor <strong>USHORT</strong> en formato big-endian.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>Proporciona descripciones para cada valor del <strong>calificador Valores.</strong> Las <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>funciones TdhEnumerateProviderFieldInformation</strong></a> y <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> devuelven estas descripciones al intentar recuperar información de nivel y palabra clave. Las descripciones son opcionales. Si no proporciona las descripciones, las funciones devuelven <strong>NULL.</strong> Consulte <a href="#specifying-level-and-enable-flags-values-for-a-provider">Especificación de valores de nivel y habilitación de marcas para un proveedor</a> para obtener más detalles.</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Especifica los valores de índice entero o marca que se asignan a valores de cadena. Si especifica este calificador, también debe especificar el calificador <strong>Values</strong> y, opcionalmente, el <strong>calificador ValueType.</strong> Tenga en cuenta que ETW no admite la opción WMI de tener cadenas para los valores de asignación de valores.
<p>En el ejemplo siguiente se muestra cómo usar los calificadores ValueMap, Values y ValueType.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Valores</strong></td>
<td>Valores de cadena. Si también se especifica el calificador <strong>ValueMap,</strong> las cadenas se corresponden directamente con los valores del <strong>calificador ValueMap.</strong> De lo contrario, suponga que el valor de propiedad es un índice de base cero en las cadenas de valor.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Indica si los valores <strong>de ValueMap</strong> son valores de índice entero o valores de marca de bits. Si no especifica este calificador, se suponen valores de índice entero. Para especificar que los valores son valores de índice entero, use ValueType( &quot; index &quot; ). Para especificar que los valores son valores de marca de bits, use ValueType( &quot; flag &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>Cada propiedad debe contener el <strong>calificador WmiDataId.</strong> <strong>WmiDataId define</strong> el orden en el que el consumidor lee los datos del evento. El valor de <strong>WmiDataId</strong> comienza en 1 e incrementa para cada propiedad de la clase . Por ejemplo, WmiDataId(1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Indica que los datos están en formato XML y listos para mostrarse sin formato adicional.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Especificación de valores de nivel y habilitación de marcas para un proveedor

Para documentar el nivel y habilitar las marcas que un controlador usaría para habilitar el proveedor, incluya las propiedades "Level" y "Flags" en la clase MOF del proveedor. Los nombres de propiedad Level y Flags distinguen mayúsculas de minúsculas. Las propiedades deben incluir los **calificadores Values** **y ValueMap,** que especifican el nivel posible y habilitan los valores de marca. ValueMap **para** los valores de marca de habilitación debe ser valores de bits (marca). El **calificador ValueDescriptions** es opcional, pero debe usarlo para proporcionar descripciones para cada valor posible. Las descripciones se usan cuando alguien llama a las funciones [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) y [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) para obtener el nivel posible y habilitar los valores de marcas (palabras clave) para el proveedor.

A continuación se muestra una clase de proveedor que especifica el nivel posible y habilita los valores de las marcas.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
