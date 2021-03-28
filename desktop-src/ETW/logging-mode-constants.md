---
description: Las constantes siguientes representan los posibles modos de registro para una sesión de seguimiento de eventos.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Constantes de modo de registro
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984574"
---
# <a name="logging-mode-constants"></a>Constantes de modo de registro

Las constantes siguientes representan los posibles modos de registro para una sesión de seguimiento de eventos.

Las constantes se usan en los miembros **LogFileMode** del archivo [**de \_ \_ registro de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), [**\_ \_ las propiedades de seguimiento de eventos y las**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) estructuras de encabezado del archivo de [**\_ Registro \_ de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) . Estas constantes se definen en el archivo de encabezado *Evntrace. h* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mode</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>Igual que <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> sin el tamaño máximo de archivo especificado.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Escribe los eventos en un archivo de registro secuencialmente; se detiene cuando el archivo alcanza su tamaño máximo. No utilice con <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> o <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Escribe eventos en un archivo de registro. Una vez que el archivo alcanza el tamaño máximo, los eventos más antiguos se reemplazan por eventos entrantes. Tenga en cuenta que el contenido del archivo de registro circular puede aparecer desordenado en equipos con varios procesadores.<br/> No utilice con <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Anexa eventos a un archivo de registro secuencial existente. El archivo se creará si no existe. Use solo si especifica la <a href="wnode-header.md"><strong>hora del sistema</strong></a> para la resolución del reloj; de lo contrario, <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>ProcessTrace</strong></a> devolverá eventos con marcas de tiempo incorrectas. Al utilizar <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, los valores de <strong>BufferSize</strong>, <strong>NumberOfProcessors</strong>y <strong>ClockType</strong> deben proporcionarse explícitamente y deben ser los mismos en el registrador y en el archivo que se va a anexar.<br/> No utilice con <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Cambia automáticamente a un nuevo archivo de registro cuando el archivo alcanza el tamaño máximo. Debe establecerse el miembro <strong>maximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> . El nombre de archivo especificado debe ser una cadena con formato (por ejemplo, la cadena contiene un valor% d, como c:\test%d.ETL). Cada vez que se crea un nuevo archivo, se incrementa un contador y se usa su valor, se actualiza la cadena con formato y se usa la cadena resultante como nombre de archivo.<br/> Esta opción no está permitida para sesiones de seguimiento de eventos privado y no debe usarse para las sesiones del registrador del kernel de NT.<br/> No utilice con <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> o <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Reserva <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a> bytes de espacio en disco para el archivo de registro de antemano. El archivo ocupa todo el espacio durante el registro para los archivos de registro circular y secuencial. Al detener la sesión, el archivo de registro se reduce al tamaño necesario. Debe establecer <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. MaximumFileSize</strong></a>.<br/> No puede usar el modo para sesiones de seguimiento de eventos privados.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>No se puede detener la sesión de registro. Este modo solo es compatible con el registrador automático. esta opción es compatible con Windows Vista y versiones posteriores.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0X00000080)</td>
<td>Restringe quién puede registrar eventos en la sesión en los que tienen el permiso <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> . Esta opción es compatible con Windows Vista y versiones posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Entrega los eventos a los consumidores en tiempo real. Los eventos se entregan cuando se vacían los búferes, no en el momento en que el proveedor escribe el evento. No debe habilitar el modo en tiempo real si no hay consumidores que consuman los eventos, ya que se producirá un error en las llamadas a eventos de registro cuando se llenen los búferes. Antes de Windows Vista, si no se consumieron los eventos, los eventos se descartaron. No especifique más de un consumidor en tiempo real en un proceso en Windows XP orWindows Server 2003. En su lugar, un subproceso consume eventos y distribuye los eventos a otros usuarios.<br/> <strong>Antes de Windows Vista:</strong> No debe usar el modo en tiempo real porque la tasa de eventos admitidos es mucho menor que la lectura del archivo de registro (se pueden quitar eventos). Además, el orden de los eventos no se garantiza en equipos con varios procesadores. El modo en tiempo real es más adecuado para los eventos de bajo tráfico y tipo de notificación.<br/> <br/> Este modo se puede combinar con otros modos de archivo de registro. sin embargo, no utilice este modo con EVENT_TRACE_PRIVATE_LOGGER_MODE. Tenga en cuenta que si combina este modo con otros modos de archivo de registro, los búferes se vaciarán una vez por segundo, lo que provocará que se escriban en el archivo de registro. Por ejemplo, si usa búferes de 64k y la tasa de registro es de 1 evento cada segundo, el servicio escribirá 64k/s en el archivo de registro.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Este modo se usa para retrasar la apertura del archivo de registro hasta que se produce un evento. <br/>
<blockquote>
<strong>Nota:</strong><br />
En Windows Vista o posterior, no se puede usar este modo no aplicable.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Este modo escribe eventos en un búfer de memoria circular. Los eventos que se escriben más allá del tamaño total del búfer expulsan los eventos más antiguos que todavía quedan en el búfer. El tamaño de este búfer de memoria es el producto de <strong>MinimumBuffers</strong> y <strong>BufferSize</strong> (vea <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). Como consecuencia de esta fórmula, cualquier búfer que use <strong>EVENT_TRACE_BUFFERING_MODE</strong> omitirá el valor de <strong>MaximumBuffers</strong> .<br/> Los eventos no se escriben en un archivo de registro o se entregan en tiempo real, y ETW no vacía los búferes. Para obtener una instantánea del búfer, llame a la función <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>FlushTrace</strong></a> .<br/> Este modo es especialmente útil para depurar controladores de dispositivos junto con la capacidad de ver el contenido de los búferes en memoria con la extensión del depurador de kernel de <a href="/windows-hardware/drivers/devtest/trace-session">WMITrace</a> .<br/> No utilice con <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>o <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Crea una sesión de seguimiento de eventos de modo usuario que se ejecuta en el mismo proceso que su proveedor de seguimiento de eventos. La memoria de los búferes procede de la memoria del proceso. Los procesos que no requieren datos del kernel pueden eliminar la sobrecarga asociada con las transiciones de modo kernel mediante una sesión de seguimiento de eventos privados.<br/> Si el proveedor está registrado por varios procesos, ETW anexa el identificador de proceso al nombre del archivo de registro para crear un nombre de archivo de registro único. Por ejemplo, si el controlador especifica los nombres de archivo de registro como c:\mylogs\myprivatelog.ETL, ETW crea el archivo de registro como c:\mylogs\ myprivatelog.etl_nnnn, donde nnnn es el identificador de proceso. El identificador de proceso no se anexa al primer proceso que registra el proveedor, sino que solo se anexa a los procesos posteriores que registran el proveedor.<br/> Las sesiones de seguimiento de eventos privados tienen las siguientes limitaciones:<br/>
<ul>
<li>Una sesión privada solo puede registrar eventos de los subprocesos del proceso en el que se está ejecutando.</li>
<li>Puede haber hasta ocho sesiones privadas por proceso.</li>
<li>Las sesiones privadas no se pueden usar con la entrega en tiempo real.</li>
<li>Los eventos generados por una sesión privada no incluyen el tiempo de ejecución para el modo kernel frente a las instrucciones en modo de usuario, o detalles del nivel de subproceso del tiempo de CPU utilizado.</li>
</ul>
Los filtros de ID. de proceso y los filtros de nombre ejecutable ahora se pueden pasar a las API de control de sesión cuando se inician registradores privados del sistema. Para obtener los mejores resultados en escenarios de proceso cruzado, se deben pasar los mismos filtros a todas las operaciones de control durante la sesión, incluidas las llamadas de habilitación de proveedor/diasble. Tenga en cuenta que los filtros tienen el mismo formato que los consumidos por <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>. <br/> Puede usar este modo junto con el modo de <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> .<br/> <strong>Antes de Windows 10, versión 1703:</strong> Solo LocalSystem, el administrador y los usuarios del grupo de administradores que se ejecutan en un proceso con privilegios elevados pueden crear una sesión privada. Si incluye la marca <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> , cualquier usuario puede crear una sesión privada en proceso. Además, en versiones anteriores de Windows solo puede haber una sesión privada por proceso (a menos que también se especifique el modo EVENT_TRACE_PRIVATE_IN_PROC, en cuyo caso puede crear hasta tres sesiones privadas en proceso). <br/> <strong>Antes de Windows Vista:</strong> Los usuarios del grupo usuarios del registro de rendimiento también pueden crear una sesión privada.<br/> <br/> No utilice con EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>Antes de Windows 7 y Windows Server 2008 R2:</strong> No utilice con EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Esta opción agrega un encabezado al archivo de registro.<br/>
<blockquote>
<strong>Nota:</strong><br />
En Windows Vista o posterior, no se puede usar este modo no aplicable.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Use kilobytes como unidad de medida para especificar el tamaño de un archivo. La unidad de medida predeterminada es megabytes. Este modo se aplica al valor del registro <strong>maxfilesize</strong> para una sesión del <a href="configuring-and-starting-an-autologger-session.md">registrador automático</a> y al miembro de <strong>maximumFileSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Esta opción es compatible con Windows Vista y versiones posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Utiliza números de secuencia que son únicos en las sesiones de seguimiento de eventos. Este modo solo se aplica a los eventos registrados mediante la función <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Para obtener más información, consulte <strong>TraceMessage</strong> para obtener detalles de uso.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> y <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> se excluyen mutuamente.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Utiliza números de secuencia que solo son únicos para una sesión de seguimiento de eventos individual. Este modo solo se aplica a los eventos registrados mediante la función <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>TraceMessage</strong></a> . Para obtener más información, consulte <strong>TraceMessage</strong> para obtener detalles de uso.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> y <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> se excluyen mutuamente.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000)</td>
<td>Registra el evento sin incluir <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>.
<blockquote>
<strong>Nota:</strong><br />
Este modo no debe usarse. Está reservado para uso interno.
</blockquote>
<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Use junto con el modo de <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> para iniciar una sesión privada. Este modo exige que solo el proceso que registró el GUID del proveedor pueda iniciar la sesión del registrador con ese GUID.<br/> Puede crear hasta tres sesiones privadas en proceso por proceso.<br/> Esta opción es compatible con Windows Vista y versiones posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Esta opción se usa para indicar el montón y el seguimiento de la sección crítico. Esta opción es compatible con Windows Vista y versiones posteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Esta opción detiene el registro en el apagado híbrido. Si no se especifica <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ni <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW elegirá un valor predeterminado en función de si el llamador procede de la sesión 0 o no. Esta opción es compatible con Windows 8 y Windows Server 2012. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Esta opción sigue registrando el apagado híbrido. Si no se especifica <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> ni <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW elegirá un valor predeterminado en función de si el llamador procede de la sesión 0 o no. Esta opción es compatible con Windows 8 y Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Usa la memoria paginada. Se recomienda esta configuración para que los eventos no utilicen la memoria no paginada. Los búferes no paginados usan memoria no paginada para el espacio de búfer. Dado que nunca se paginan los búferes no paginados, una sesión de registro funciona bien. El uso de búferes paginables requiere menos recursos.<br/> Los proveedores de modo kernel y los registradores del sistema no pueden registrar eventos en las sesiones que especifican este modo de registro.<br/> Este modo se omite si se establece <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> .<br/> No puede usar este modo con el registrador del kernel de NT.<br/> <strong>Windows 2000:</strong> Este valor no se admite.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Esta opción recibirá eventos de SystemTraceProvider. Si el parámetro <strong>LogFileMode</strong> de<em>las propiedades</em> <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>StartTrace</strong></a>incluye esta marca, el Registrador será un registrador del sistema. Esta opción es compatible con Windows 8 y Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Indica que una sesión de registro no debe verse afectada por errores de <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> en otras sesiones. Sin esta marca, si un evento no se puede publicar en una de las sesiones en las que está habilitado un proveedor, el evento no se publicará en ninguna de las sesiones. Cuando se establece esta marca, un error al escribir un evento en una sesión no hará que la función <strong>EventWrite</strong> devuelva un código de error en otras sesiones. <br/> No utilice con <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Esta opción es compatible con Windows 8.1, Windows Server 2012 R2 y versiones posteriores.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Escribe eventos que se registraron en procesadores diferentes en un búfer común. El uso de este modo puede eliminar el problema de los eventos que aparecen desordenados cuando se publican eventos en diferentes procesadores con la hora del sistema. Este modo también puede eliminar el problema con los registros circulares que aparecen para colocar eventos en varios equipos del procesador.<br/> Si no utiliza este modo y usa la hora del sistema, los eventos pueden aparecer desordenados en varios equipos del procesador. Esto se debe a que los búferes ETW están asociados con un procesador en lugar de un subproceso. Como resultado, si un subproceso se cambia de una CPU a otra, el búfer asociado con la última CPU se puede vaciar en el disco antes del asociado a la CPU anterior.<br/> Si espera un gran volumen de eventos (por ejemplo, más de 1.000 eventos por segundo), no debería usar este modo.<br/> Tenga en cuenta que el número de procesador no se incluye con el evento.<br/> Esta opción es compatible con Windows 7, Windows Server 2008 R2 y versiones posteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Esta opción agrega búferes ETW a los volcados de memoria. Esta opción es compatible con Windows 8 y Windows Server 2012. <br/></td>
</tr>
</tbody>
</table>
