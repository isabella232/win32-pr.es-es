---
description: La sesión de seguimiento de eventos de registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configurar e iniciar la sesión del registrador global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8692e1f7321acc163e48cda7e3323f3d24adc1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985722"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configurar e iniciar la sesión del registrador global

La sesión de seguimiento de eventos de registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo. Las aplicaciones y los controladores de dispositivos pueden usar la sesión del registrador global para capturar seguimientos antes de que el usuario inicie sesión. Tenga en cuenta que algunos controladores de dispositivos, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión del registrador global.

> [!Note]  
> Si va a crear una sesión del registrador global en Windows Vista, considere la posibilidad de crear una [sesión de registrador automático](configuring-and-starting-an-autologger-session.md) en su lugar.

 

El registro se utiliza para configurar la sesión del registrador global. Agregue la clave **GlobalLogger** a la siguiente clave del registro, si aún no está presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

En la tabla siguiente se describen los valores que se pueden definir para la clave **GlobalLogger** . Debe tener privilegios de administrador para especificar estos valores del registro. Los valores del registro afectan a todos los proveedores que registran eventos en la sesión del registrador global. El valor **Start** es el único valor necesario para iniciar la sesión del registrador global; todos los demás valores tienen valores predeterminados que se utilizan si el valor no está presente en el registro. Normalmente, se deben usar los valores predeterminados. Si especifica un valor que ETW no admite, ETW invalidará el valor.



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
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Establezca este valor en 1 (activado) para iniciar la sesión del registrador global la próxima vez que se inicie el sistema. Para evitar que se inicie la sesión, establezca este valor en 0 (desactivado). <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño de cada búfer, en kilobytes. Este valor debe ser inferior a un megabyte. ETW utiliza el tamaño de la memoria física para calcular este valor. <br/></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>REG_BINARY</strong></td>
<td>Use este valor para habilitar uno o varios proveedores de kernel. Si habilita los proveedores de kernel, la sesión del registrador global cambiará de nombre al registrador del kernel de NT cuando se inicie. Para ver los valores posibles, vea el miembro <strong>EnableFlags</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>El número de archivos de registro de seguimiento de eventos generados por las sesiones del registrador global. El sistema incrementa este valor hasta que alcanza el valor de <strong>FileMax</strong>. A continuación, restablece el valor en 0. Este contador impide que el sistema sobrescriba un archivo de registro de seguimiento del registrador global. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de archivos de registro de seguimiento de eventos permitidos en el sistema. Cuando el número de registros de seguimiento alcanza el máximo especificado, el sistema empieza a sobrescribir los registros, empezando por el más antiguo. <br/> Si el archivo de registro especificado en <strong>filename</strong> existe, ETW anexa el valor de <strong>FileCounter</strong> al nombre de archivo. Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formato es%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br/> El valor predeterminado es 0, lo que significa que no hay ningún máximo. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Ruta de acceso completa del archivo de registro. La ruta de acceso a este archivo debe existir. El archivo de registro es un archivo de registro secuencial. Tenga en cuenta que todos los proveedores que escriben eventos en la sesión del registrador global escriben eventos en este archivo de registro. La ruta de acceso está limitada a 1024 caracteres. Si no se especifica <strong>filename</strong> , los eventos se escriben en%systemroot%\System32\LogFiles\WMI\GlobalLogger.ETL. <strong>Antes de Windows Vista:</strong> El archivo predeterminado es%SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Frecuencia, en segundos, con la que se eliminan forzosamente los búferes de seguimiento. El tiempo mínimo de vaciado es de 1 segundo. Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento. <br/> En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo. Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece en <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> El valor predeterminado es 0. De forma predeterminada, los búferes se vacían solo cuando están llenos. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifica las opciones de sesión de registro. Para ver los valores, consulte <a href="logging-mode-constants.md">constantes del modo de registro</a>. Estos valores se admiten en Windows Vista y versiones posteriores. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de búferes que se van a asignar. Normalmente, este valor es el número mínimo de búferes más veinte. ETW usa el tamaño de búfer y el tamaño de la memoria física para calcular este valor. Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño máximo, en megabytes, del archivo de registro de seguimiento de eventos. De manera predeterminada, no hay un tamaño máximo de archivo.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>El número mínimo de búferes que se asignan cuando se inicia la sesión del registrador global. El número mínimo de búferes que se pueden especificar es de dos búferes por procesador. Por ejemplo, en un equipo con un solo procesador, el número mínimo de búferes es dos. <br/> El valor predeterminado en un sistema de un solo procesador es 0X3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Estado</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>El estado de inicio del registrador global. Si el registrador global no se pudo iniciar, el valor de esta clave es el código de error de Win32 adecuado. Si el registrador global se inició correctamente, el valor de esta clave es ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Una vez que se ha modificado el registro y se ha reiniciado el equipo, la sesión del registrador global se inicia automáticamente y se usa como cualquier otra sesión con una excepción: se usa el identificador \_ \_ \_ de constante de identificador de registrador global de WMI (definido en Wmistr. h) para hacer referencia a la sesión del registrador global. Esta constante se puede usar como argumento para cualquier función de seguimiento de eventos que acepte un identificador de sesión. En las funciones que aceptan un nombre de sesión, use \_ el nombre del registrador global \_ .

El controlador de registrador global no llama a la función [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar los proveedores. El proveedor es responsable de determinar si se inicia la sesión del registrador global y, a continuación, se habilita a sí misma.

Para determinar si se inicia la sesión del registrador global, puede llamar a la función [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) , estableciendo *SessionHandle* en el \_ identificador de registrador global de WMI \_ \_ y *ControlCode* en la consulta de **control de seguimiento de eventos \_ \_ \_**. Si la llamada a **ControlTrace** es correcta, la sesión del registrador global existe y el proveedor puede habilitarse y registrar los eventos en la sesión del registrador global (la función **CONTROLTRACE** devuelve el error \_ \_ no se encuentra la instancia de WMI \_ \_ si el registrador global no está activo).

Normalmente, el controlador es responsable de pasar las marcas y el nivel de habilitación al proveedor cuando habilita el proveedor, pero como el controlador de registrador global no habilita el proveedor, es responsabilidad del proveedor pasar esta información a sí misma, si es necesario.

La sesión del registrador global es un recurso limitado y debe usarse con moderación. Los servicios que deseen capturar información durante el proceso de arranque deben considerar la posibilidad de agregar la lógica del controlador a sí misma en lugar de utilizar la sesión del registrador global.

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

Para obtener información detallada sobre cómo iniciar una sesión de registrador privada, vea [configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md).

Para obtener información detallada sobre cómo iniciar una sesión del registrador del kernel de NT, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).

