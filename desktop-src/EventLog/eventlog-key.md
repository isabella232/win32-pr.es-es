---
description: 'El registro de eventos contiene los siguientes registros estándar, así como registros personalizados:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Clave del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eed1e64d3084d6b952693957c65766b257cb552a861c9989ea0550111e9b224
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383775"
---
# <a name="eventlog-key"></a>Clave del registro de eventos

El registro de eventos contiene los siguientes registros estándar, así como registros personalizados:



| Log             | Descripción                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aplicación** | Contiene eventos registrados por las aplicaciones. Por ejemplo, una aplicación de base de datos podría registrar un error de archivo. El desarrollador de la aplicación decide qué eventos registrar.                                                                             |
| **Seguridad**    | Contiene eventos como intentos de inicio de sesión válidos o no válidos, así como eventos relacionados con el uso de recursos, como la creación, apertura o eliminación de archivos u otros objetos. Un administrador puede iniciar la auditoría para registrar eventos en el registro de seguridad. |
| **Sistema**      | Contiene eventos registrados por componentes del sistema, como el error de un controlador u otro componente del sistema para cargar durante el inicio.                                                                                                               |
| *CustomLog*     | Contiene eventos registrados por aplicaciones que crean un registro personalizado. El uso de un registro personalizado permite que una aplicación controle el tamaño del registro o adjunte acl por motivos de seguridad sin afectar a otras aplicaciones.                         |



 

El servicio de registro de eventos usa la información almacenada en la clave del Registro **eventlog.** La **clave eventlog** contiene varias subclaves, *denominadas registros*. Cada registro contiene información que el servicio de registro de eventos usa para buscar recursos cuando una aplicación escribe en el registro de eventos y lo lee.

La estructura de la **clave eventlog** es la siguiente:

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

Tenga en cuenta que los controladores  de dominio registran eventos en el servicio **de directorio** y los registros del servicio de replicación de archivos y los servidores DNS registran eventos en el **servidor DNS.**

Cada registro puede contener los siguientes valores del Registro.



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
<td><strong>CustomSD</strong></td>
<td>Restringe el acceso al registro de eventos. Este valor es de tipo REG_SZ. El formato utilizado es <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Lenguaje de definición de descriptores de seguridad</a> (SDDL). Construya una ACL que conceda uno o varios de los derechos siguientes:<dl> Borrar (0x0004)<br />
Lectura (0x0001)<br />
Escritura (0x0002)<br />
</dl> Para ser un SDDL sintácticamente válido, el valor CustomSD debe especificar un propietario y un propietario del grupo (por ejemplo, O:BAG:SY), pero no se usan el propietario ni el propietario del grupo. Si CustomSD se establece en un valor incorrecto, se desencadena un evento en el registro de eventos del sistema cuando se inicia el servicio de registro de eventos y el registro de eventos obtiene un descriptor de seguridad predeterminado que es idéntico al valor customSD original para el registro de aplicaciones. Las SACL no se admiten.<br/> Para obtener más información, vea <a href="event-logging-security.md">Event Logging Security</a>.<br/> <strong>Windows Server 2003:</strong> Se admiten las SACL.<br/> <strong>Windows XP/2000:</strong> Este valor no se admite.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:</strong> Nombre del archivo que almacena el nombre localizado del registro de eventos. El nombre almacenado en este archivo aparece como el nombre del registro en Visor de eventos. Si esta entrada no aparece en el Registro para un registro de eventos, Visor de eventos muestra el nombre de la subclave del Registro como nombre del registro. Este valor es de tipo REG_EXPAND_SZ. El valor predeterminado es %SystemRoot%\system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:</strong> Número de identificación del mensaje de la cadena de nombre de registro. Este número indica el mensaje en el que aparece el nombre para mostrar localizado. El mensaje se almacena en el archivo especificado por el <strong>valor DisplayNameFile.</strong> Este valor es de tipo REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>Archivo</strong></td>
<td>Ruta de acceso completa al archivo donde se almacena cada registro de eventos. Esto permite que Visor de eventos y otras aplicaciones busquen los archivos de registro. Este valor es de tipo REG_SZ o REG_EXPAND_SZ. Este valor es opcional. Si no se especifica el valor, el valor predeterminado es %SystemRoot%\system32\winevt\logs\ seguido de un nombre de archivo basado en el nombre de la clave del Registro de registros de eventos. La ruta de acceso del archivo de registro de eventos específica debe establecerse mediante la utilidad de línea de comandos wevtutil.exe o mediante la función <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> con EvtChannelLoggingConfigLogFilePath pasado al <em>parámetro PropertyId.</em><br/> Si se establece un archivo específico, asegúrese de que el servicio de registro de eventos tiene permisos completos en el archivo.<br/> Este valor debe ser un nombre de archivo válido para un archivo que se encuentra en un directorio local (no un equipo remoto, no un dispositivo DOS, no un disquete y no una canalización). Si la configuración del archivo es incorrecta, se desencadena un evento en el registro de eventos del sistema cuando se inicia el servicio de registro de eventos.<br/> No use variables de entorno, en la ruta de acceso al archivo, que no se puedan expandir en el contexto del servicio de registro de eventos.<br/> <strong>Windows Server 2003 y Windows XP/2000:</strong> Este valor tiene como valor predeterminado %SystemRoot%\system32\config\ seguido de un nombre de archivo basado en el nombre de clave del Registro de registros de eventos. Si la opción Archivo se establece en un valor no válido, el registro no se inicializará correctamente o todas las solicitudes irán en modo silencioso al registro predeterminado (Aplicación).<br/></td>
</tr>
<tr class="odd">
<td><strong>Maxsize</strong></td>
<td>Tamaño máximo, en bytes, del archivo de registro. Este valor es de tipo REG_DWORD. El valor debe establecerse en un múltiplo de 64 000 para un registro de sistema, aplicación o seguridad. El valor predeterminado es 1 MB. <strong>Windows Server 2003 y Windows XP/2000:</strong> El valor se limita a 0xFFFFFFFF y el valor predeterminado es 512 000.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Este valor no se usa. <strong>Windows Server 2003 y Windows XP/2000:</strong> Este valor es el nombre de la subclave que contiene los valores predeterminados de las entradas de la subclave para el origen del evento. Este valor es de tipo REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Retención</strong></td>
<td>Este valor es de tipo REG_DWORD. El valor predeterminado es 0. Si este valor es 0, los registros de eventos siempre se sobrescriben. Si este valor es 0xFFFFFFFF o cualquier valor distinto de cero, los registros nunca se sobrescriben. Cuando el archivo de registro alcanza su tamaño máximo, debe borrar el registro manualmente; De lo contrario, se descartan los nuevos eventos. También debe borrar el registro para poder cambiar su tamaño. <strong>Windows Server 2003 y Windows XP/2000:</strong> Este valor es el intervalo de tiempo, en segundos, que protegen los registros de eventos para que no se sobrescriban. Cuando la antigüedad de un evento alcanza o supera este valor, se puede sobrescribir.<br/></td>
</tr>
<tr class="even">
<td><strong>Sources</strong></td>
<td>Este valor no se utiliza. <strong>Windows Server 2003 y Windows XP/2000:</strong> Nombres de las aplicaciones, servicios o grupos de aplicaciones que escriben eventos en este registro. Este valor solo debe leerse y no modificarse. El servicio de registro de eventos mantiene la lista en función de cada programa enumerado en una subclave bajo el registro. Este valor es de tipo REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Este valor es de tipo REG_DWORD y lo usa el servicio de registro de eventos para determinar si se debe guardar automáticamente un registro de eventos. El valor predeterminado es 0, lo que deshabilita la copia de seguridad automática. El servicio realizará una copia de seguridad del archivo de registro solo si el valor de retención es -1 (0xFFFFFFFF). Se omitirán otros valores. <strong>Windows Server 2003:</strong> La retención se puede establecer en -1 (0xFFFFFFFF) o 1 (0x00000001) para que AutoBackupLogFiles funcione. Se omitirán otros valores.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Este valor no se utiliza. <strong>Windows XP/2000:</strong> Este valor es de tipo REG_DWORD y el valor predeterminado es 1. Cuando el valor se establece en 1, restringe el acceso de la cuenta de invitado y anónimo al registro de eventos y, cuando este valor es 0, permite el acceso de la cuenta de invitado al registro de eventos.<br/></td>
</tr>
<tr class="odd">
<td><strong>Aislamiento</strong></td>
<td>Define los permisos de acceso predeterminados para el registro. Este valor es de tipo REG_SZ. Puede especificar uno de los siguientes valores:
<ul>
<li><strong>Aplicación</strong></li>
<li><strong>Sistema</strong></li>
<li><strong>Personalizada</strong></li>
</ul>
El aislamiento predeterminado es <strong>Application</strong>. Los permisos predeterminados para <strong>la aplicación</strong> son (se muestran mediante SDDL): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Los permisos predeterminados para <strong>System son</strong> (se muestran mediante SDDL): <br/>
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
Los permisos predeterminados para el <strong>aislamiento</strong> personalizado son los mismos que los de la aplicación.<br/> <strong>Windows Server 2003 y Windows XP/2000:</strong> Este valor no está disponible.<br/></td>
</tr>
</tbody>
</table>



 

Cada registro también contiene orígenes de eventos. Para obtener más información, vea [Orígenes de eventos](event-sources.md).

