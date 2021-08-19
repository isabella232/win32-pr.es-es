---
description: La sesión de seguimiento de eventos de AutoLogger registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configuración e inicio de una sesión de Registrador automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242b0a0cbcd9b633fd838d133240d1e78464351a5d3970de30516d60481905bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638615"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configuración e inicio de una sesión de Registrador automático

La sesión de seguimiento de eventos de AutoLogger registra los eventos que se producen al principio del proceso de arranque del sistema operativo. Las aplicaciones y los controladores de dispositivos pueden usar la sesión de AutoLogger para capturar seguimientos antes de que el usuario inicie sesión. Tenga en cuenta que algunos controladores de dispositivo, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión del registrador automático.

El registrador automático difiere del registrador global de las maneras siguientes:

-   Puede especificar una o varias sesiones de AutoLogger (el registrador global era una sesión única en la que todos los usuarios registraba eventos).
-   El registrador automático envía una notificación de habilitación a los proveedores cuando se inicia la sesión (el registrador global no envió una notificación de habilitación a los proveedores, por lo que los proveedores tenían que basarse en otros medios para saber si se inició la sesión del registrador global para iniciar el registro de eventos).
-   El registrador automático no admite el registro de eventos del registrador de kernel nt (vea el **miembro EnableFlags** de [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Para registrar eventos del registrador de kernel de NT, debe usar el [registrador global](configuring-and-starting-the-global-logger-session.md).

Para obtener más información sobre la consulta del registrador global, vea [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).

> [!Note]  
> ETW admite AutoLogger en Windows Vista y versiones posteriores. Use global [Logger en](configuring-and-starting-the-global-logger-session.md) sistemas operativos anteriores.

 

Use el Registro para configurar la sesión de AutoLogger. Agregue la siguiente clave del Registro, si aún no está presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

En la **tecla Registrador** automático, cree una clave para cada sesión de AutoLogger que quiera configurar, como se muestra en el ejemplo siguiente.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

Para cada sesión, cree una clave para cada proveedor que desee habilitar para la sesión. Use el GUID del proveedor como clave.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

En la tabla siguiente se describen los valores que puede definir para cada sesión de AutoLogger. Debe tener privilegios de administrador para especificar estos valores del Registro. Los **valores Start** y **Guid** son los únicos valores necesarios para iniciar la sesión de AutoLogger. todos los demás valores tienen valores predeterminados que se usan si el valor no está presente en el Registro. Normalmente, debe usar los valores predeterminados. Si especifica un valor que ETW no admite, ETW invalidará el valor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño de cada búfer, en kilobytes. Debe ser menor que un megabyte. ETW usa el tamaño de la memoria física para calcular este valor.<br/></td>
</tr>
<tr class="even">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Temporizador que se usará al registrar la marca de tiempo para cada evento.
<ul>
<li>1 = Valor del contador de rendimiento (alta resolución)</li>
<li>2 = Temporizador del sistema</li>
<li>3 = Contador de ciclo de CPU</li>
</ul>
Para obtener una descripción de cada tipo de reloj, vea el <strong>miembro ClientContext</strong> <a href="wnode-header.md"><strong>de WNODE_HEADER</strong></a>.<br/> El valor predeterminado es 1 (valor del contador de rendimiento) en Windows Vista y versiones posteriores. Antes de Windows Vista, el valor predeterminado es 2 (temporizador del sistema).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para deshabilitar la persistencia en tiempo real, establezca este valor en 1. El valor predeterminado es 0 (habilitado) para las sesiones en tiempo real.<br/> Si la persistencia en tiempo real está habilitada, se conservarán los eventos en tiempo real que no se entregaron en el momento en que el equipo se apagó. Los eventos se entregarán al consumidor la próxima vez que el consumidor se conecte a la sesión. <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>No establezca ni modifique este valor. Este valor es el número de serie utilizado para incrementar el nombre del archivo de registro si <strong>se especifica FileMax.</strong> Si el valor no es válido, se asumirá 1.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Ruta de acceso completa del archivo de registro. La ruta de acceso a este archivo debe existir. El archivo de registro es un archivo de registro secuencial. La ruta de acceso está limitada a 1024 caracteres.<br/> Si <strong>no se especifica FileName,</strong> los eventos se escriben en %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de instancias del archivo de registro que crea ETW. Si existe el archivo de registro especificado en <strong>FileName,</strong> ETW anexa el valor <strong>fileCounter</strong> al nombre de archivo. Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formulario es %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl. Nnnn. <br/> La primera vez que se inicia el equipo, el nombre de archivo es sessionname .etl.0001, la segunda vez el nombre de archivo es &lt; &gt; &lt; sessionname &gt; .etl.0002, y así sucesivamente. Si <strong>FileMax</strong> es 3, en el cuarto reinicio del equipo, ETW restablece el contador a 1 y sobrescribe &lt; sessionname &gt; .etl.0001, si existe.<br/> El número máximo de instancias del archivo de registro que se admiten es 16.<br/> No use esta característica con el modo <a href="logging-mode-constants.md">de</a> EVENT_TRACE_FILE_MODE_NEWFILE de registro.<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Con qué frecuencia, en segundos, los búferes de seguimiento se vacían a la fuerza. El tiempo mínimo de vaciado es de 1 segundo. Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento. <br/> En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo. Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece en <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> El valor predeterminado es 0. De forma predeterminada, los búferes solo se vacían cuando están llenos. <br/></td>
</tr>
<tr class="even">
<td><strong>Guid</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Cadena que contiene un GUID que identifica de forma única la sesión. Este valor es necesario.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifique uno o varios modos de registro. Para obtener los valores posibles, <a href="logging-mode-constants.md">vea Constantes de modo de registro</a>. El valor predeterminado <strong>es EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. En lugar de escribir en un archivo de registro, puede especificar EVENT_TRACE_BUFFERING_MODE <strong>o</strong> <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> La <strong>especificación EVENT_TRACE_BUFFERING_MODE</strong> evita el costo de vaciar el contenido de la sesión en el disco cuando el sistema de archivos esté disponible. <br/> Tenga en <strong>cuenta</strong> que EVENT_TRACE_BUFFERING_MODE el sistema omitirá el valor <strong>MaximumBuffers,</strong> ya que el tamaño del búfer es en su lugar el producto <strong>de MinimumBuffers</strong> y <strong>BufferSize</strong>.<br/> Las sesiones de AutoLogger no admiten el <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> de registro.<br/> Si <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> especificado, <strong>BufferSize</strong> debe proporcionarse explícitamente y debe ser el mismo en el registrador y el archivo que se va a anexar.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño máximo del archivo de registro, en megabytes. La sesión se cierra cuando se alcanza el tamaño máximo, a menos que esté en modo de archivo de registro circular. Para no especificar ningún límite, establezca el valor en 0. El valor predeterminado es 100 MB, si no se establece. El comportamiento que se produce cuando se alcanza el tamaño máximo de archivo depende del valor <strong>de LogFileMode</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de búferes que se asignarán. Normalmente, este valor es el número mínimo de búferes más veinte. ETW usa el tamaño del búfer y el tamaño de memoria física para calcular este valor. Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número mínimo de búferes que se asignarán en el inicio. El número mínimo de búferes que puede especificar es de dos búferes por procesador. Por ejemplo, en un equipo con un solo procesador, el número mínimo de búferes es dos.<br/></td>
</tr>
<tr class="odd">
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para que la sesión de AutoLogger se inicie la próxima vez que se reinicie el equipo, establezca este valor en 1; De lo contrario, establezca este valor en 0.<br/></td>
</tr>
<tr class="even">
<td><strong>Estado</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Estado de inicio del registrador automático. Si el registrador automático no se pudo iniciar, el valor de esta clave es el código de error de Win32 adecuado. Si el registrador automático se inició correctamente, el valor de esta clave <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se describen los valores que puede definir para cada proveedor que desea habilitar para la sesión. Debe tener privilegios de administrador para especificar estos valores del Registro. Si especifica un valor que ETW no admite, ETW invalidará el valor.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Tipo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Habilitado</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Determina si el proveedor está habilitado. Para habilitar el proveedor, establezca este valor en 1. Para deshabilitar el proveedor, establezca este valor en 0. El valor predeterminado es 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido por el proveedor que especifica la clase de eventos para la que el proveedor genera eventos. Para más información, consulte <em>el parámetro EnableFlags</em> de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>función EnableTrace.</strong></a> Especifique este nombre de valor si el proveedor no admite <strong>MatchAnyKeyword</strong> o <strong>MatchAllKeyword.</strong></td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido por el proveedor que especifica el nivel de detalle incluido en el evento. Por ejemplo, puede usar este valor para indicar el nivel de gravedad de los eventos (informativo, advertencia, error) que genera el proveedor. Para obtener una lista de los niveles predefinidos, vea el <em>parámetro level</em> de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Use este valor para incluir uno o varios de los siguientes elementos en el archivo de registro:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Incluir en los datos extendidos el identificador de seguridad (SID) del usuario.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Incluir en los datos extendidos el identificador de sesión de terminal.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Incluir en los datos extendidos un seguimiento de la pila de llamadas para los eventos escritos mediante <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos los eventos que no tienen especificada una palabra clave que no sea cero.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indica que esta llamada <a href="provider-traits.md">a</a> <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> debe habilitar un grupo de proveedores en lugar de un proveedor de eventos individual.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Incluir la clave de inicio del proceso en los datos extendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Incluir la clave de evento en los datos extendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos los eventos marcados como un evento InPrivate o proceden de un proceso marcado como InPrivate.</li>
</ul>
Para obtener más información sobre estos elementos, vea <strong>EnableProperty</strong> de la <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> estructura.<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Máscara de bits de palabras clave que determinan la categoría de eventos que desea que escriba el proveedor. El proveedor escribe el evento si alguno de los bits de palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara. Para especificar que el proveedor escriba todos los eventos, establezca este valor en cero. Para obtener un ejemplo, vea la sección Comentarios de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Esta máscara de bits es opcional. Esta máscara restringe aún más la categoría de eventos que desea que escriba el proveedor. Si la palabra clave del evento cumple la condición <em>MatchAnyKeyword,</em> el proveedor escribirá el evento solo si todos los bits de esta máscara existen en la palabra clave del evento. Esta máscara no se usa si <em>MatchAnyKeyword</em> es cero. Para obtener un ejemplo, vea la sección Comentarios de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></td>
</tr>
</tbody>
</table>



 

Una vez modificado el Registro, la sesión de AutoLogger se inicia la próxima vez que se reinicia el equipo. La sesión de AutoLogger llama a [**la función EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar los proveedores.

Las sesiones de AutoLogger aumentan el tiempo de arranque del sistema y se deben usar con moderación. Los servicios que desean capturar información durante el proceso de arranque deben considerar la posibilidad de agregar lógica de controlador a sí mismo en lugar de usar la sesión de AutoLogger.

Para detener una sesión de AutoLogger, llame a la [**función ControlTrace.**](/windows/win32/api/evntrace/nf-evntrace-controltracea) El nombre de sesión que pasa a la función es el nombre de la clave del Registro que usó para definir la sesión en el Registro.

En Windows 8.1,Windows Server 2012 R2 y versiones posteriores, la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras ENABLE TRACE [**\_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT \_ FILTER \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) pueden usar filtros de carga de eventos, ámbito y recorrido de pila para filtrar por condiciones específicas en una sesión de registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) y las estructuras **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** y [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador privado, vea [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador de kernel nt, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración e inicio de una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configuración e inicio de una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador de kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ PARÁMETROS DE \_ SEGUIMIENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**DESCRIPTOR \_ DE FILTRO DE \_ EVENTOS**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PREDICADO \_ DE FILTRO DE CARGA \_ ÚTIL**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>
