---
title: Propiedades de extensión IIS de BITS
description: Servicio de transferencia inteligente en segundo plano (BITS) usa una ISAPI para extender IIS para admitir trabajos de carga.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS BITS de propiedades de extensión IIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1afb18e324419834d5a1445d1a1b9e5390f5d932
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480951"
---
# <a name="bits-iis-extension-properties"></a>Propiedades de extensión IIS de BITS

Servicio de transferencia inteligente en segundo plano (BITS) usa una ISAPI para extender IIS para admitir trabajos [**de carga.**](/windows/win32/api/bits/ne-bits-bg_job_type) En la tabla siguiente se enumeran las propiedades que BITS agrega a la metabase de IIS para el componente de directorio virtual. BITS usa estas propiedades para determinar cómo cargar los archivos. Las propiedades de extensión IIS de BITS son heredables, excepto **BITSUploadEnabled.**




| Propiedad | Descripción | 
|----------|-------------|
| <strong>BITSUploadEnabled</strong> Tipo de datos: <strong>booleano</strong><br /> | Indica si las cargas de BITS están habilitadas en el directorio virtual. Si la configuración no está presente o es 0, se deshabilitan las cargas de BITS.<br /> Se trata de una propiedad de solo lectura. Para establecer esta propiedad, llame al <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>método EnableBITSUploads</strong></a> o <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> de la <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>interfaz IBITSExtensionSetup.</strong></a><br /> | 
| <strong>BITSSessionTimeout</strong> Tipo de datos: <strong>DWORD</strong><br /> | Número de segundos que se mantiene la conexión si no se realiza ningún progreso al cargar el archivo; el temporizador se restablece cuando se realiza el progreso. BITS cierra la conexión si se alcanza el tiempo de espera y limpia los datos asociados a la sesión.<br /> Establecer un tiempo de espera de sesión breve puede ser un problema para los trabajos de carga y respuesta porque la respuesta solo se descarga cuando el usuario ha iniciado sesión y está conectado a la red. Es posible que la sesión se resalte antes de que se descargue la respuesta, en cuyo caso la sesión se cancela y se elimina el archivo de respuesta.<br /> Tenga en cuenta que BITS cancela el trabajo si se alcanza el valor directiva de grupo <a href="/windows/win32/bits/group-policies">JobInactivityTimeout</a> (el valor predeterminado es 90 días), independientemente de esta configuración.<br /> El valor predeterminado es 1209 600 (14 días).<br /> | 
| <strong>BITSMaximumUploadSize</strong> Tipo de datos: <strong>Cadena</strong><br /> | Número máximo de bytes que se pueden cargar por trabajo. Especifique el número máximo de bytes como una cadena decimal; El valor de cadena debe ser menor o igual que "1844674407370955". Una cadena vacía es igual que especificar "1844674407370955".<br /> El valor predeterminado es una cadena vacía.<br /><blockquote>[!Note]<br />En IIS 7, el límite de carga predeterminado es de 30 millones de bytes. El valor de la <strong>propiedad BITSMaximumUploadSize</strong> no puede superar el límite de IIS. Para obtener más información sobre cómo cambiar el valor predeterminado de IIS, vea <a href="https://support.microsoft.com//kb/942074">KB942074</a>.</blockquote><br /><br /> | 
| <strong>BITSServerNotificationType</strong> Tipo de datos: <strong>DWORD</strong><br /> | Especifica cómo enviar el archivo de carga a la aplicación de servidor. Los valores posibles son: 0, 1 y 2.<br /> Un valor de 0 significa que el archivo no se envía a la aplicación de servidor. BITS coloca el archivo de carga en el directorio especificado en <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile"></a> el nombre remoto (el nombre remoto especificado al agregar el archivo al trabajo) sin notificar a la aplicación de servidor. Si el archivo existe actualmente en el directorio de destino, se reemplaza por el archivo de carga.<br /> Un valor de 1 significa que BITS pasa la ubicación del archivo de carga a la aplicación de servidor especificada en la <strong>propiedad BITSServerNotificationURL.</strong> La aplicación de servidor procesa el archivo y genera un archivo de respuesta, si es necesario. De forma predeterminada, BITS quita los archivos de carga y respuesta del servidor después de recibir la respuesta de la aplicación de servidor. Para que BITS copie el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo, incluya el encabezado <a href="/windows/win32/bits/notification-protocol-for-server-applications">BITS-Copy-File-To-Destination</a> en la respuesta. Si no incluye el encabezado y desea guardar los archivos de carga y respuesta, debe copiar los archivos de carga y respuesta en una nueva ubicación antes de responder.<br /> Un valor de 2 significa que BITS pasa el archivo de carga en el cuerpo de la solicitud a la aplicación de servidor especificada en la <strong>propiedad BITSServerNotificationURL.</strong> La aplicación de servidor procesa el archivo y pasa la respuesta en el cuerpo de la respuesta, si es necesario.<br /> Para obtener más información sobre los encabezados de solicitud y respuesta, vea <a href="/windows/win32/bits/notification-protocol-for-server-applications">Protocolo de notificación para aplicaciones de servidor</a>.<br /> La aplicación de servidor debe proporcionar una respuesta en un plazo de cinco minutos. Si la aplicación de servidor no responde en un plazo de cinco minutos, el trabajo entra en el estado de error transitorio. Cuando expire <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>el retraso de</strong></a> reintento, el servidor BITS enviará otra notificación a la aplicación de servidor (la aplicación de servidor debe escribirse para controlar las notificaciones duplicadas). <strong>BITS 1.5:</strong> El tiempo de espera de notificación es de 30 segundos.<br /><br /> El valor predeterminado es 0.<br /> | 
| <strong>BITSServerNotificationURL</strong> Tipo de datos: <strong>Cadena</strong><br /> | Opcional. Contiene la dirección URL de la aplicación de servidor en la que BITS publica el archivo de carga. Debe especificar una dirección URL si el valor de la <strong>propiedad BITSServerNotificationType</strong> es 1 o 2. La dirección URL está limitada a 2200 caracteres, sin incluir el terminador nulo. La dirección URL debe ser una dirección URL HTTP; BITS no admite direcciones URL de notificación HTTPS.<br /> Si la dirección URL no está disponible en el momento de la carga, BITS volverá a intentar la carga hasta que exista la dirección URL de notificación o hasta que expire el período de reintento.<br /> Tenga en cuenta que si el nombre remoto especificado en el trabajo contiene una cadena de consulta, la cadena de consulta se anexa a la dirección URL que especifique. Por ejemplo, si el nombre remoto contiene y especifica el valor https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 <strong>BITSServerNotificationURL</strong> como , la dirección URL en la que https://otherserver/myvdir2/bag.asp BITS publica es https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br /> Si la dirección URL original es y la dirección URL de notificación es https://myserver/myvdir/file.txt myasp.asp, BITS usa http//myserver/myvdir/myasp.asp como dirección URL de notificación.<br /> Si la ruta de acceso y la parte del nombre de archivo de la dirección URL contienen caracteres Unicode que no son comunes a la página de códigos en el cliente y el servidor, se producirá un error en la traducción de direcciones URL en el servidor y el trabajo de BITS se colocará en el estado de error. Si la parte del servidor de la dirección URL contiene caracteres Unicode, debe codificar la parte del servidor mediante <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">nombres</a> de dominio internacionalizados (IDN).<br /> | 
| <strong>BITSHostId</strong> Tipo de datos: <strong>Cadena</strong><br /> | Establezca esta propiedad si la instalación del servidor es una granja de servidores web que no usa almacenamiento compartido.<br /> Especifique el nombre del servidor o la dirección IP del servidor al que volver a conectarse después de interrumpir el proceso de carga. Normalmente, se especifica el nombre del servidor que se va a configurar. La dirección URL está limitada a 300 caracteres, sin incluir el terminador null.<br /> Si no especifica esta propiedad y se interrumpe el proceso de carga, es posible que BITS reanude el trabajo en otro servidor de la granja. Sin embargo, el servidor anterior todavía contiene el archivo de carga parcial de antes de la interrupción. BITS quita el archivo parcial después de que <strong>expire BITSSessionTimeout.</strong><br /><blockquote>[!Note]<br />No use la propiedad <strong>BITSHostId</strong> si se usa SSL en una granja de servidores web que usa equilibrio de carga de red (NLB) o nombres DNS con varias direcciones IP, a menos que incluya el nombre del clúster y los nombres de servidor individuales en el certificado. (Si el nombre de servidor especificado en <strong>BITSHostId</strong> no coincide con el nombre común del certificado, se producirá un error en el trabajo). En su lugar, para NLB, establezca el parámetro <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">Affinity</a> en <strong>Single</strong> para asegurarse de que el cliente se comunica con el mismo servidor en el futuro.</blockquote><br /><br /> | 
| <strong>BITSHostIdFallbackTimeout</strong> Tipo de datos: <strong>DWORD</strong><br /> | Número de segundos que el cliente bits intenta volver a conectarse al nombre de servidor <strong>BITSHostId</strong> antes de revertir al nombre de host especificado en el nombre de archivo remoto del trabajo. El temporizador comienza cuando BITS no puede conectarse al <strong>servidor BITSHostId.</strong> El temporizador se restablece cuando el cliente se conecta correctamente al servidor.<br /> Tenga en cuenta que el valor de tiempo de espera sin progreso del trabajo (consulte <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>IBackgroundCopyJob::SetNoProgressTimeout</strong></a>) debe ser mayor que este valor de tiempo de espera. Si no es así, se producirá un error en el trabajo antes de que expire el valor de tiempo de espera de reserva.<br /> Establezca esta propiedad solo si establece la <strong>propiedad BITSHostId.</strong><br /> El valor predeterminado es 86 400 (1 día).<br /> | 
| <strong>BITSAllowOverwrites</strong> Tipo de datos: <strong>Entero</strong><br /> | Indica si un archivo de carga puede sobrescribir un archivo existente con el mismo nombre. El archivo de carga sobrescribe el archivo existente si <strong>BITSAllowOverwrites</strong> es 1.<br /> El valor predeterminado es 0.<br /><strong>IIS 6.0:</strong> Esta propiedad solo se puede establecer desde un script, no se puede establecer mediante la página de propiedades de la extensión BITS en la interfaz de usuario de IIS.<br /><br /> | 
| <strong>BITSCleanupUseDefault</strong> Tipo de datos: <strong>booleano</strong><br /> | Indica si la tarea de limpieza usa las programaciones predeterminadas. De forma predeterminada, la tarea de limpieza se ejecuta cada 12 horas.<br /> Establezca en 1 para usar la programación predeterminada; de lo contrario, 0 para especificar una programación.<br /> Para especificar una programación, use las <strong>propiedades BITSCleanupCount</strong> <strong>y BITSCleanupUnits.</strong><br /> La tarea de limpieza limpia el directorio virtual mediante la eliminación de trabajos que no se han modificado dentro del período de tiempo de espera de la sesión (vea <strong>BITSSessionTimeout</strong>).<br /> El valor predeterminado es 1. Use la programación predeterminada.<br /><strong>IIS 6.0:</strong> No se admite.<br /> | 
| <strong>BITSCleanupCount</strong> Tipo de datos: <strong>Entero</strong><br /> | Especifica el intervalo de espera entre la ejecución de la tarea de limpieza. El intervalo que puede especificar depende de las unidades. Para ver los posibles valores de intervalo, <strong>vea la propiedad BITSCleanupUnits.</strong><br /> Esta propiedad se omite si <strong>BITSCleanupUseDefault</strong> es 0.<br /><strong>IIS 6.0:</strong> No se admite.<br /><br /> | 
| <strong>BITSCleanupUnits</strong> Tipo de datos: <strong>Entero</strong><br /> | Especifica las unidades para el intervalo de limpieza especificado en la <strong>propiedad BITSCleanupCount.</strong> Esta propiedad se omite si <strong>BITSCleanupUseDefault</strong> es 0.<br /> Los valores posibles son:<dl> 0: las unidades son minutos. Los valores posibles son de 1 a 60.<br />1: las unidades son horas. Este es el valor predeterminado. Los valores posibles son de 1 a 24.<br />2: Las unidades son días. Los valores posibles son de 1 a 360.<br /></dl><br /><strong>IIS 6.0:</strong> No se admite.<br /><br /> | 
| <strong>BITSNumberOfSessionsLimit</strong> Tipo de datos: <strong>Entero</strong><br /> | Limita el número de sesiones de carga que pueden existir simultáneamente para un usuario. Si el número de sesiones de un usuario es superior a este límite, cuando se ejecute la tarea de limpieza, eliminará las sesiones más recientes hasta que el número de sesiones del usuario esté por debajo del límite.<br /> El valor predeterminado es 50 sesiones.<br /><strong>IIS 6.0:</strong> No se admite.<br /><br /> | 
| <strong>BITSSessionLimitEnable</strong> Tipo de datos: <strong>booleano</strong><br /> | Indica si BITS limita el número de sesiones de carga por usuario. Si la configuración no está presente o es 0, el límite está deshabilitado.<br /> Para especificar el límite, establezca la <strong>propiedad BITSNumberOfSessionsLimit.</strong><br /> El valor predeterminado es 1.<br /><strong>IIS 6.0:</strong> No se admite.<br /><br /> | 




 

En el ejemplo siguiente se muestra cómo establecer las propiedades de la extensión IIS de BITS Windows host de script. Si el directorio virtual apunta a un recurso compartido remoto, establezca también las propiedades **UNCUserName** y **UNCPassword** de IIS.


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

