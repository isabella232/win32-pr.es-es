---
description: 'El registro de eventos contiene los siguientes registros estándar, así como registros personalizados:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Clave EventLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965c850dd31ab722786cf4da41c7d3a67f5d980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812895"
---
# <a name="eventlog-key"></a>Clave EventLog

El registro de eventos contiene los siguientes registros estándar, así como registros personalizados:



| Log             | Descripción                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aplicación** | Contiene los eventos registrados por las aplicaciones. Por ejemplo, una aplicación de base de datos puede registrar un error de archivo. El desarrollador de aplicaciones decide qué eventos se registran.                                                                             |
| **Seguridad**    | Contiene eventos como intentos de inicio de sesión válidos y no válidos, así como eventos relacionados con el uso de recursos, como la creación, apertura o eliminación de archivos u otros objetos. Un administrador puede iniciar la auditoría para registrar eventos en el registro de seguridad. |
| **Sistema**      | Contiene eventos registrados por componentes del sistema, como el error de carga de un controlador u otro componente del sistema durante el inicio.                                                                                                               |
| *CustomLog*     | Contiene los eventos registrados por las aplicaciones que crean un registro personalizado. El uso de un registro personalizado permite a una aplicación controlar el tamaño del registro o adjuntar ACL por motivos de seguridad sin afectar a otras aplicaciones.                         |



 

El servicio de registro de eventos utiliza la información almacenada en la clave del registro **EventLog** . La clave **EventLog** contiene varias subclaves, denominadas *registros*. Cada registro contiene información que utiliza el servicio de registro de eventos para buscar recursos cuando una aplicación escribe y lee en el registro de eventos.

La estructura de la clave **EventLog** es la siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

Tenga en cuenta que los controladores de dominio registran eventos en el **servicio de directorio** y los registros del servicio de **replicación de archivos** y los servidores DNS registran los eventos en el **servidor DNS**.

Cada registro puede contener los siguientes valores del registro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor del Registro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Con aduana</strong></td>
<td>Restringe el acceso al registro de eventos. Este valor es de tipo REG_SZ. El formato utilizado es el <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">lenguaje de definición de descriptores de seguridad</a> (SDDL). Construya una ACL que conceda uno o varios de los siguientes derechos:<dl> Clear (0x0004)<br />
Lectura (0x0001)<br />
Escritura (0x0002)<br />
</dl> Para ser un SDDL válido sintácticamente, el valor de la aduana debe especificar un propietario y un propietario del grupo (por ejemplo, O:BAG: SY), pero no se usarán el propietario y el propietario del grupo. Si se establece el valor de con la opción con un valor incorrecto, se desencadena un evento en el registro de eventos del sistema cuando se inicia el servicio registro de eventos, y el registro de eventos obtiene un descriptor de seguridad predeterminado que es idéntico al valor de aduana original para el registro de la aplicación. No se admiten las SACL.<br/> Para obtener más información, consulte <a href="event-logging-security.md">seguridad del registro de eventos</a>.<br/> <strong>Windows Server 2003:</strong> Se admiten las SACL.<br/> <strong>Windows XP/2000:</strong> Este valor no se admite.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:  </strong> Nombre del archivo que almacena el nombre localizado del registro de eventos. El nombre almacenado en este archivo aparece como el nombre de registro en Visor de eventos. Si esta entrada no aparece en el registro de un registro de eventos, Visor de eventos muestra el nombre de la subclave del registro como el nombre del registro. Este valor es de tipo REG_EXPAND_SZ. El valor predeterminado es% SystemRoot% \system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:  </strong> Número de identificación del mensaje de la cadena de nombre de registro. Este número indica el mensaje en el que aparece el nombre para mostrar localizado. El mensaje se almacena en el archivo especificado por el valor de <strong>DisplayNameFile</strong> . Este valor es de tipo REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>Archivo</strong></td>
<td>Ruta de acceso completa al archivo donde se almacena cada registro de eventos. Esto permite que Visor de eventos y otras aplicaciones encuentren los archivos de registro. Este valor es de tipo REG_SZ o REG_EXPAND_SZ. Este valor es opcional. Si no se especifica el valor, se toma como valor predeterminado%SystemRoot%\system32\winevt\logs\ seguido de un nombre de archivo que se basa en el nombre de la clave del registro del registro de eventos. La ruta de acceso del archivo de registro de eventos específica debe establecerse mediante la utilidad de línea de comandos wevtutil.exe o mediante la función <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> con EvtChannelLoggingConfigLogFilePath pasado en el parámetro <em>PropertyId</em> .<br/> Si se establece un archivo específico, asegúrese de que el servicio registro de eventos tenga permisos completos en el archivo.<br/> Este valor debe ser un nombre de archivo válido para un archivo que se encuentra en un directorio local (no en un equipo remoto, no en un dispositivo de DOS, no en un disquete y no en una canalización). Si la configuración del archivo es incorrecta, se desencadena un evento en el registro de eventos del sistema cuando se inicia el servicio registro de eventos.<br/> No use variables de entorno, en la ruta de acceso al archivo, que no se pueden expandir en el contexto del servicio registro de eventos.<br/> <strong>Windows Server 2003 y Windows XP/2000:</strong> De forma predeterminada, este valor es%SystemRoot%\system32\config\ seguido de un nombre de archivo que se basa en el nombre de la clave del registro del registro de eventos. Si la configuración del archivo se establece en un valor no válido, el registro no se inicializará correctamente o todas las solicitudes Irán al registro predeterminado (aplicación).<br/></td>
</tr>
<tr class="odd">
<td><strong>Tamañomáximo</strong></td>
<td>Tamaño máximo, en bytes, del archivo de registro. Este valor es de tipo REG_DWORD. El valor se debe establecer en un múltiplo de 64K para un sistema, una aplicación o un registro de seguridad. El valor predeterminado es 1 MB. <strong>Windows Server 2003 y Windows XP/2000:</strong> El valor se limita a 0xFFFFFFFF y el valor predeterminado es 512 k.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:</strong> Este valor es el nombre de la subclave que contiene los valores predeterminados de las entradas de la subclave del origen del evento. Este valor es de tipo REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Retención</strong></td>
<td>Este valor es de tipo REG_DWORD. El valor predeterminado es 0. Si este valor es 0, los registros de eventos siempre se sobrescriben. Si este valor es 0xFFFFFFFF o cualquier valor distinto de cero, los registros nunca se sobrescriben. Cuando el archivo de registro alcanza su tamaño máximo, debe borrar el registro manualmente; de lo contrario, se descartan los nuevos eventos. También debe borrar el registro para poder cambiar su tamaño. <strong>Windows Server 2003 y Windows XP/2000:  </strong> Este valor es el intervalo de tiempo, en segundos, que se protegen los registros de eventos para que no se sobrescriban. Cuando la antigüedad de un evento alcanza o supera este valor, se puede sobrescribir.<br/></td>
</tr>
<tr class="even">
<td><strong>Sources</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:  </strong> Nombres de las aplicaciones, servicios o grupos de aplicaciones que escriben eventos en este registro. Este valor solo se debe leer y no modificar. El servicio registro de eventos mantiene la lista en función de cada programa enumerado en una subclave del registro. Este valor es de tipo REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Este valor es de tipo REG_DWORD y lo utiliza el servicio registro de eventos para determinar si se debe guardar automáticamente un registro de eventos. El valor predeterminado es 0, que deshabilita la copia de seguridad automática. El servicio realizará una copia de seguridad del archivo de registro solo si el valor de retención es-1 (0xFFFFFFFF). Se omitirán otros valores. <strong>Windows Server 2003:  </strong> La retención se puede establecer en-1 (0xFFFFFFFF) o 1 (0x00000001) para que AutoBackupLogFiles funcione. Se omitirán otros valores.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Este valor no se utiliza. <strong>Windows XP/2000:  </strong> Este valor es de tipo REG_DWORD y el valor predeterminado es 1. Cuando el valor se establece en 1, restringe el acceso de la cuenta invitado y anónima al registro de eventos, y cuando este valor es 0, permite el acceso de la cuenta de invitado al registro de eventos.<br/></td>
</tr>
<tr class="odd">
<td><strong>Aislamiento</strong></td>
<td>Define los permisos de acceso predeterminados para el registro. Este valor es de tipo REG_SZ. Puede especificar uno de los siguientes valores:
<ul>
<li><strong>Aplicación</strong></li>
<li><strong>Sistema</strong></li>
<li><strong>Personalizada</strong></li>
</ul>
El aislamiento predeterminado es <strong>aplicación</strong>. Los permisos predeterminados para la <strong>aplicación</strong> se muestran mediante SDDL: <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Los permisos predeterminados para el <strong>sistema</strong> son (se muestran mediante SDDL): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
Los permisos predeterminados para el aislamiento <strong>personalizado</strong> son los mismos que para la aplicación.<br/> <strong>Windows Server 2003 y Windows XP/2000:  </strong> Este valor no está disponible.<br/></td>
</tr>
</tbody>
</table>



 

Cada registro también contiene orígenes de eventos. Para obtener más información, vea [orígenes de eventos](event-sources.md).

