---
description: La sesión de seguimiento de eventos de registradores automáticos registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurar e iniciar una sesión de registrador automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986138"
---
# <a name="configuring-and-starting-an-autologger-session"></a>Configurar e iniciar una sesión de registrador automático

La sesión de seguimiento de eventos de registradores automáticos registra los eventos que se producen al principio del proceso de arranque del sistema operativo. Las aplicaciones y los controladores de dispositivos pueden usar la sesión del registrador automático para capturar seguimientos antes de que el usuario inicie sesión. Tenga en cuenta que algunos controladores de dispositivos, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión de registrador automático.

El registrador automático difiere del registrador global de las siguientes maneras:

-   Puede especificar una o más sesiones del registrador automático (el registrador global era una sesión única en la que todos los eventos registraron).
-   El registrador automático envía una notificación de habilitación a los proveedores cuando se inicia la sesión (el registrador global no envió una notificación de habilitación a los proveedores, por lo que los proveedores tenían que confiar en otros medios para saber si se inició la sesión del registrador global para empezar a registrar eventos).
-   El registrador automático no admite el registro de eventos del registrador del kernel de NT (vea el miembro **EnableFlags** de [**\_ \_ las propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)). Para registrar los eventos del registrador del kernel de NT, debe usar el [registrador global](configuring-and-starting-the-global-logger-session.md).

Para obtener más información sobre la audiencia global del registrador, vea [configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md).

> [!Note]  
> ETW es compatible con el registrador automático en Windows Vista y versiones posteriores. Usar el [registrador global](configuring-and-starting-the-global-logger-session.md) en sistemas operativos anteriores.

 

El registro se utiliza para configurar la sesión del registrador automático. Agregue la siguiente clave del registro, si aún no está presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

En la clave de **registrador automático** , cree una clave para cada sesión del registrador automático que desee configurar, tal y como se muestra en el ejemplo siguiente.

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

Para cada sesión, cree una clave para cada proveedor que desee habilitar para la sesión. Utilice el GUID del proveedor como la clave.

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

En la tabla siguiente se describen los valores que se pueden definir para cada sesión del registrador automático. Debe tener privilegios de administrador para especificar estos valores del registro. El valor **inicial** y el **GUID** son los únicos valores necesarios para iniciar la sesión del registrador automático; todos los demás valores tienen valores predeterminados que se utilizan si el valor no está presente en el registro. Normalmente, se deben usar los valores predeterminados. Si especifica un valor que ETW no admite, ETW invalidará el valor.



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
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño de cada búfer, en kilobytes. Debe ser inferior a un megabyte. ETW utiliza el tamaño de la memoria física para calcular este valor.<br/></td>
</tr>
<tr class="even">
<td><strong>ClockType</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Temporizador que se va a usar al registrar la marca de tiempo para cada evento.
<ul>
<li>1 = valor del contador de rendimiento (alta resolución)</li>
<li>2 = temporizador del sistema</li>
<li>3 = contador de ciclo de CPU</li>
</ul>
Para obtener una descripción de cada tipo de reloj, vea el miembro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br/> El valor predeterminado es 1 (valor del contador de rendimiento) en Windows Vista y versiones posteriores. Antes de Windows Vista, el valor predeterminado es 2 (temporizador del sistema).<br/></td>
</tr>
<tr class="odd">
<td><strong>DisableRealtimePersistence</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para deshabilitar la persistencia en tiempo real, establezca este valor en 1. El valor predeterminado es 0 (habilitado) para las sesiones en tiempo real.<br/> Si está habilitada la persistencia en tiempo real, se conservarán los eventos en tiempo real que no se hayan entregado en el momento en que se cerró el equipo. Los eventos se entregarán al consumidor la próxima vez que el consumidor se conecte a la sesión. <br/></td>
</tr>
<tr class="even">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>No establezca ni modifique este valor. Este valor es el número de serie que se usa para incrementar el nombre del archivo de registro si se especifica <strong>FileMax</strong> . Si el valor no es válido, se asumirá 1.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Ruta de acceso completa del archivo de registro. La ruta de acceso a este archivo debe existir. El archivo de registro es un archivo de registro secuencial. La ruta de acceso está limitada a 1024 caracteres.<br/> Si no se especifica <strong>filename</strong> , los eventos se escriben en%systemroot%\System32\LogFiles\WMI\ <sessionname> . ETL. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de instancias del archivo de registro que ETW crea. Si el archivo de registro especificado en <strong>filename</strong> existe, ETW anexa el valor de <strong>FileCounter</strong> al nombre de archivo. Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formulario es%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . ETL. NNNN. <br/> La primera vez que se inicia el equipo, el nombre de archivo es <sessionname> . ETL. 0001, la segunda vez que el nombre de archivo es <sessionname> . ETL. 0002, etc. Si <strong>FileMax</strong> es 3, en el cuarto reinicio del equipo, ETW restablece el contador en 1 y sobrescribe <sessionname> . ETL. 0001, si existe.<br/> El número máximo de instancias del archivo de registro que se admiten es 16.<br/> No use esta característica con el modo de archivo de registro de <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Frecuencia, en segundos, con la que se eliminan forzosamente los búferes de seguimiento. El tiempo mínimo de vaciado es de 1 segundo. Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento. <br/> En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo. Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece en <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> El valor predeterminado es 0. De forma predeterminada, los búferes se vacían solo cuando están llenos. <br/></td>
</tr>
<tr class="even">
<td><strong>Guid</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Cadena que contiene un GUID que identifica de forma única la sesión. Este valor es necesario.</td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifique uno o más modos de registro. Para ver los valores posibles, consulte <a href="logging-mode-constants.md">constantes del modo de registro</a>. El valor predeterminado es <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>. En lugar de escribir en un archivo de registro, puede especificar <strong>EVENT_TRACE_BUFFERING_MODE</strong> o <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> La especificación de <strong>EVENT_TRACE_BUFFERING_MODE</strong> evita el costo de vaciar el contenido de la sesión en el disco cuando el sistema de archivos está disponible. <br/> Tenga en cuenta que el uso de <strong>EVENT_TRACE_BUFFERING_MODE</strong> hará que el sistema omita el valor <strong>MaximumBuffers</strong> , ya que el tamaño del búfer es el producto de <strong>MinimumBuffers</strong> y <strong>BufferSize</strong>.<br/> Las sesiones del registrador automático no admiten el modo de registro de <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .<br/> Si se especifica <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> , <strong>BufferSize</strong> se debe proporcionar explícitamente y debe ser el mismo tanto en el registrador como en el archivo que se va a anexar.<br/></td>
</tr>
<tr class="even">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño máximo de archivo del archivo de registro, en megabytes. La sesión se cierra cuando se alcanza el tamaño máximo, a menos que esté en modo de archivo de registro circular. Para no especificar ningún límite, establezca el valor en 0. El valor predeterminado es 100 MB, si no se establece. El comportamiento que se produce cuando se alcanza el tamaño máximo de archivo depende del valor de <strong>LogFileMode</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de búferes que se van a asignar. Normalmente, este valor es el número mínimo de búferes más veinte. ETW usa el tamaño de búfer y el tamaño de la memoria física para calcular este valor. Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número mínimo de búferes que se van a asignar en el inicio. El número mínimo de búferes que se pueden especificar es de dos búferes por procesador. Por ejemplo, en un equipo con un solo procesador, el número mínimo de búferes es dos.<br/></td>
</tr>
<tr class="odd">
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Para que la sesión del registrador automático se inicie la próxima vez que se reinicie el equipo, establezca este valor en 1; en caso contrario, establezca este valor en 0.<br/></td>
</tr>
<tr class="even">
<td><strong>Estado</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>El estado de inicio del registrador automático. Si no se pudo iniciar el registrador automático, el valor de esta clave es el código de error de Win32 adecuado. Si el registrador automático se inició correctamente, el valor de esta clave es <strong>ERROR_SUCCESS</strong> (0).<br/></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se describen los valores que puede definir para cada proveedor que desea habilitar para la sesión. Debe tener privilegios de administrador para especificar estos valores del registro. Si especifica un valor que ETW no admite, ETW invalidará el valor.



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
<td><strong>Enabled</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Determina si el proveedor está habilitado. Para habilitar el proveedor, establezca este valor en 1. Para deshabilitar el proveedor, establezca este valor en 0. El valor predeterminado es 0.</td>
</tr>
<tr class="even">
<td><strong>EnableFlags</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido por el proveedor que especifica la clase de eventos para los que el proveedor genera eventos. Para obtener más información, consulte el parámetro <em>EnableFlags</em> de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> . Especifique este nombre de valor si el proveedor no admite <strong>MatchAnyKeyword</strong> o <strong>MatchAllKeyword</strong>.</td>
</tr>
<tr class="odd">
<td><strong>EnableLevel</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Valor definido por el proveedor que especifica el nivel de detalle incluido en el evento. Por ejemplo, puede usar este valor para indicar el nivel de gravedad de los eventos (informativo, ADVERTENCIA, error) que genera el proveedor. Para obtener una lista de niveles predefinidos, vea el parámetro <em>LEVEL</em> de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>EnableProperty</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Use este valor para incluir uno o varios de los siguientes elementos en el archivo de registro:
<ul>
<li><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = incluir en los datos extendidos el identificador de seguridad (SID) del usuario.</li>
<li><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = incluir en los datos extendidos el identificador de la sesión de terminal.</li>
<li><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = incluir en los datos extendidos seguimiento de la pila de llamadas para los eventos escritos mediante <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</li>
<li><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos los eventos que no tienen una palabra clave distinta de cero especificada.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica que esta llamada a <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> debe habilitar un <a href="provider-traits.md">grupo de proveedores</a> en lugar de un proveedor de eventos individual.</li>
<li><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = incluir la clave de inicio del proceso en los datos extendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = incluir la clave de evento en los datos extendidos.</li>
<li><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos los eventos que están marcados como eventos InPrivate o provienen de un proceso marcado como InPrivate.</li>
</ul>
Para obtener más información sobre estos elementos, vea <strong>EnableProperty</strong> de la estructura <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>MatchAnyKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Máscara de claves de palabras clave que determinan la categoría de eventos que desea que el proveedor escriba. El proveedor escribe el evento si cualquiera de los bits de la palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara. Para especificar que el proveedor escriba todos los eventos, establezca este valor en cero. Para obtener un ejemplo, vea la sección Comentarios de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
<tr class="even">
<td><strong>MatchAllKeyword</strong></td>
<td><strong>REG_QWORD</strong></td>
<td>Esta máscara de máscara es opcional. Esta máscara restringe aún más la categoría de eventos que desea que escriba el proveedor. Si la palabra clave del evento cumple la condición <em>MatchAnyKeyword</em> , el proveedor escribirá el evento solo si todos los bits de esta máscara existen en la palabra clave del evento. Esta máscara no se usa si <em>MatchAnyKeyword</em> es cero. Para obtener un ejemplo, vea la sección Comentarios de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</td>
</tr>
</tbody>
</table>



 

Una vez que se haya modificado el registro, la sesión del registrador automático se iniciará la próxima vez que se reinicie el equipo. La sesión del registrador automático llama a la función [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar los proveedores.

Las sesiones del registrador automático aumentan el tiempo de arranque del sistema y deben usarse con moderación. Los servicios que deseen capturar información durante el proceso de arranque deben considerar la posibilidad de agregar la lógica del controlador a sí misma en lugar de utilizar la sesión del registrador automático.

Para detener una sesión del registrador automático, llame a la función [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) . El nombre de sesión que se pasa a la función es el nombre de la clave del registro que se usó para definir la sesión en el registro.

En Windows 8.1, Windows Server 2012 R2 y versiones posteriores, los filtros de carga de eventos, ámbito y recorrido de pila se pueden usar con la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar según condiciones específicas en una sesión del registrador. Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , así como las estructuras de [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **habilitar \_ \_ parámetros de seguimiento**, **\_ \_ descriptor de filtro de eventos** y filtro de carga.

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obtener información detallada sobre cómo iniciar una sesión de registrador privada, vea [configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md).

Para obtener información detallada sobre cómo iniciar una sesión del registrador del kernel de NT, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configuración e inicio de la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**HABILITAR \_ parámetros de seguimiento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**descriptor de filtro de eventos \_ \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_predicado de filtro de carga \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Actualizar una sesión de seguimiento de eventos](updating-an-event-tracing-session.md)
</dt> </dl>
