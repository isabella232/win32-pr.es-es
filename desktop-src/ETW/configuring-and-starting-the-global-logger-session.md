---
description: La sesión de seguimiento de eventos del registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configuración e inicio de la sesión de registrador global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc15ad9fdb5150a976b9d7bccfb6315649617271c5ece2a7c676fbdb9f6f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395500"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configuración e inicio de la sesión de registrador global

La sesión de seguimiento de eventos del registrador global registra los eventos que se producen al principio del proceso de arranque del sistema operativo. Las aplicaciones y los controladores de dispositivos pueden usar la sesión del registrador global para capturar seguimientos antes de que el usuario inicie sesión. Tenga en cuenta que algunos controladores de dispositivo, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión del registrador global.

> [!Note]  
> Si va a crear una sesión de registrador global en Windows Vista, considere la posibilidad de crear una [sesión de AutoLogger](configuring-and-starting-an-autologger-session.md) en su lugar.

 

El Registro se usa para configurar la sesión del registrador global. Agregue la **clave GlobalLogger** a la siguiente clave del Registro, si aún no está presente:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

En la tabla siguiente se describen los valores que puede definir para la **clave GlobalLogger.** Debe tener privilegios de administrador para especificar estos valores del Registro. Los valores del Registro afectan a todos los proveedores que registren eventos en la sesión del registrador global. El **valor** Start es el único valor necesario para iniciar la sesión del registrador global. todos los demás valores tienen una configuración predeterminada que se usa si el valor no está presente en el Registro. Normalmente, debe usar los valores predeterminados. Si especifica un valor que ETW no admite, ETW invalidará el valor.



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
<td><strong>Iniciar</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Establezca este valor en 1 (on) para iniciar la sesión del registrador global la próxima vez que se inicie el sistema. Para detener el inicio de la sesión, establezca este valor en 0 (desactivado). <br/></td>
</tr>
<tr class="even">
<td><strong>BufferSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño de cada búfer, en kilobytes. Este valor debe ser inferior a un megabyte. ETW usa el tamaño de la memoria física para calcular este valor. <br/></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td><strong>EnableKernelFlags</strong></td>
<td><strong>Reg_binary</strong></td>
<td>Use este valor para habilitar uno o varios proveedores de kernel. Si habilita los proveedores de kernel, la sesión del registrador global cambiará su nombre a NT Kernel Logger cuando se inicie. Para ver los valores posibles, <strong>vea el miembro EnableFlags</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>de EVENT_TRACE_PROPERTIES</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>FileCounter</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número de archivos de registro de seguimiento de eventos generados por sesiones de Registrador global. El sistema incrementa este valor hasta que alcanza el valor de <strong>FileMax</strong>. A continuación, restablece el valor a 0. Este contador impide que el sistema sobrescriba un archivo de registro de seguimiento del registrador global. <br/></td>
</tr>
<tr class="even">
<td><strong>FileMax</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de archivos de registro de seguimiento de eventos permitidos en el sistema. Cuando el número de registros de seguimiento alcanza el máximo especificado, el sistema comienza a sobrescribir los registros, empezando por el más antiguo. <br/> Si el archivo de registro especificado en <strong>FileName</strong> existe, ETW anexa el valor <strong>fileCounter</strong> al nombre de archivo. Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formulario es %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br/> El valor predeterminado es 0, lo que significa que no hay ningún máximo. <br/></td>
</tr>
<tr class="odd">
<td><strong>FileName</strong></td>
<td><strong>REG_SZ</strong></td>
<td>Ruta de acceso completa del archivo de registro. La ruta de acceso a este archivo debe existir. El archivo de registro es un archivo de registro secuencial. Tenga en cuenta que todos los proveedores que escriben eventos en la sesión del registrador global escriben eventos en este archivo de registro. La ruta de acceso está limitada a 1024 caracteres. Si <strong>no se especifica FileName,</strong> los eventos se escriben en %SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>Antes de Windows Vista:</strong> El archivo predeterminado es %SystemRoot%\System32\LogFiles\WMI\Trace.log.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>FlushTimer</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Con qué frecuencia, en segundos, se vacían forzadamente los búferes de seguimiento. El tiempo mínimo de vaciado es de 1 segundo. Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento. <br/> En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo. Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece <strong>en EVENT_TRACE_REAL_TIME_MODE</strong>.<br/> El valor predeterminado es 0. De forma predeterminada, los búferes solo se vacían cuando están llenos. <br/></td>
</tr>
<tr class="odd">
<td><strong>LogFileMode</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Especifica las opciones de sesión de registro. Para obtener valores, vea <a href="logging-mode-constants.md">Constantes de modo de registro.</a> Estos valores se admiten en Windows Vista y versiones posteriores. <br/></td>
</tr>
<tr class="even">
<td><strong>MaximumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número máximo de búferes que se asignarán. Normalmente, este valor es el número mínimo de búferes más veinte. ETW usa el tamaño del búfer y el tamaño de la memoria física para calcular este valor. Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>MaxFileSize</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Tamaño máximo, en megabytes, del archivo de registro de seguimiento de eventos. De manera predeterminada, no hay un tamaño máximo de archivo.<br/></td>
</tr>
<tr class="even">
<td><strong>MinimumBuffers</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Número mínimo de búferes que se asignarán cuando se inicie la sesión del registrador global. El número mínimo de búferes que puede especificar es dos búferes por procesador. Por ejemplo, en un único equipo procesador, el número mínimo de búferes es dos. <br/> El valor predeterminado en un sistema de un solo procesador es 0x3.<br/></td>
</tr>
<tr class="odd">
<td><strong>Estado</strong></td>
<td><strong>REG_DWORD</strong></td>
<td>Estado de inicio del registrador global. Si el registrador global no se pudo iniciar, el valor de esta clave es el código de error de Win32 adecuado. Si el registrador global se inició correctamente, el valor de esta clave ERROR_SUCCESS (0).<br/></td>
</tr>
</tbody>
</table>



 

Una vez que se ha modificado el Registro y se ha reiniciado el equipo, la sesión del registrador global se inicia automáticamente y se usa como cualquier otra sesión con una excepción: se usa el identificador constante del identificador de registrador global de WMI (definido en \_ \_ Wmistr.h) para hacer referencia a la sesión del registrador \_ global. Esta constante se puede usar como argumento para cualquier función de seguimiento de eventos que acepte un identificador de sesión. En las funciones que aceptan un nombre de sesión, use GLOBAL \_ LOGGER \_ NAME.

El controlador del registrador global no llama a la [**función EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) para habilitar proveedores. El proveedor es responsable de determinar si se inicia la sesión del registrador global y, a continuación, habilitarse.

Para determinar si se inicia la sesión del registrador global, puede llamar a la función [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) estableciendo *SessionHandle* en IDENTIFICADOR GLOBAL DE REGISTRADOR WMI y \_ \_ \_ *ControlCode* en **EVENT TRACE CONTROL \_ \_ \_ QUERY**. Si la **llamada a ControlTrace** se realiza correctamente, la sesión del registrador global existe y el proveedor puede habilitarse y registrar eventos en la sesión del registrador global (la función **ControlTrace** devuelve ERROR WMI INSTANCE NOT FOUND si el registrador global no está \_ \_ \_ \_ activo).

Normalmente, el controlador es responsable de pasar las marcas de habilitación y el nivel al proveedor cuando habilita el proveedor, pero como el controlador del registrador global no habilita el proveedor, es responsabilidad del proveedor pasar esta información a sí mismo, si es necesario.

La sesión del registrador global es un recurso limitado y se debe usar con moderación. Los servicios que desean capturar información durante el proceso de arranque deben considerar la posibilidad de agregar lógica de controlador a sí mismo en lugar de usar la sesión del registrador global.

Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador privado, vea [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).

Para obtener más información sobre cómo iniciar una sesión de registrador de kernel nt, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

