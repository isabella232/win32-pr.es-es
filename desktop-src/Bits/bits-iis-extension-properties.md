---
title: Propiedades de extensión IIS de BITS
description: Servicio de transferencia inteligente en segundo plano (BITS) utiliza una ISAPI para extender IIS para admitir trabajos de carga.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS de las propiedades de extensión de IIS de BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09412f6aa0be1ab76e6e45ea0920e1caf1054d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533357"
---
# <a name="bits-iis-extension-properties"></a>Propiedades de extensión IIS de BITS

Servicio de transferencia inteligente en segundo plano (BITS) utiliza una ISAPI para extender IIS para admitir [**trabajos de carga**](/windows/win32/api/bits/ne-bits-bg_job_type). En la tabla siguiente se enumeran las propiedades que BITS agrega a la metabase de IIS para el componente de directorio virtual. BITS usa estas propiedades para determinar cómo se cargan los archivos. Las propiedades de extensión de IIS de BITS se pueden heredar, excepto **BITSUploadEnabled**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>BITSUploadEnabled</strong> Tipo de datos: <strong>booleano</strong><br/></td>
<td>Indica si las cargas de BITS están habilitadas en el directorio virtual. Si el valor no está presente o es 0, las cargas de BITS están deshabilitadas.<br/> Se trata de una propiedad de solo lectura. Para establecer esta propiedad, llame al método <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads</strong></a> o <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads</strong></a> de la interfaz <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>BITSSessionTimeout</strong> Tipo de datos: <strong>DWORD</strong><br/></td>
<td>Número de segundos que se mantiene la conexión si no se realiza ningún progreso al cargar el archivo; el temporizador se restablece cuando se realiza el progreso. BITS cierra la conexión si se alcanza el tiempo de espera y limpia los datos asociados a la sesión.<br/> Establecer un tiempo de espera de sesión corto puede ser un problema para los trabajos de carga y respuesta porque la respuesta solo se descarga cuando el usuario inicia sesión y se conecta a la red. Es posible que se agote el tiempo de espera de la sesión antes de que se descargue la respuesta, en cuyo caso se cancela la sesión y se elimina el archivo de respuesta.<br/> Tenga en cuenta que BITS cancela el trabajo si se alcanza el valor de directiva de grupo <a href="/windows/win32/bits/group-policies">valor jobinactivitytimeout</a> (el valor predeterminado es 90 días), independientemente de esta configuración.<br/> El valor predeterminado es 1.209.600 (14 días).<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSMaximumUploadSize</strong> Tipo de datos: <strong>cadena</strong><br/></td>
<td>Número máximo de bytes que se pueden cargar por trabajo. Especifique el número máximo de bytes como una cadena decimal; el valor de cadena debe ser menor o igual que &quot; 1844674407370955 &quot; . Una cadena vacía equivale a especificar &quot; 1844674407370955 &quot; .<br/> El valor predeterminado es una cadena vacía.<br/>
<blockquote>
[!Note]<br />
En IIS 7, el límite de carga predeterminado es de 30 millones bytes. El valor de la propiedad <strong>BITSMaximumUploadSize</strong> no puede superar el límite de IIS. Para obtener detalles e información sobre cómo cambiar el valor predeterminado de IIS, vea <a href="https://support.microsoft.com//kb/942074">KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSServerNotificationType</strong> Tipo de datos: <strong>DWORD</strong><br/></td>
<td>Especifica cómo enviar el archivo de carga a la aplicación de servidor. Los valores posibles son: 0, 1 y 2.<br/> Un valor de 0 significa que el archivo no se envía a la aplicación de servidor. BITS coloca el archivo de carga en el directorio especificado en el nombre remoto (el nombre remoto especificado al <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">Agregar el archivo</a> al trabajo) sin notificar a la aplicación de servidor. Si el archivo existe actualmente en el directorio de destino, se sustituye por el archivo de carga.<br/> Un valor de 1 significa que BITS pasa la ubicación del archivo de carga a la aplicación de servidor especificada en la propiedad <strong>BITSServerNotificationURL</strong> . La aplicación de servidor procesa el archivo y genera un archivo de respuesta, si es necesario. De forma predeterminada, BITS quita los archivos de carga y respuesta del servidor una vez que recibe la respuesta de la aplicación de servidor. Para que BITS copie el archivo de carga en la ubicación especificada por el nombre de archivo remoto en el trabajo, incluya el encabezado <a href="/windows/win32/bits/notification-protocol-for-server-applications">bits-copiar-archivo a destino</a> en la respuesta. Si no incluye el encabezado y desea guardar los archivos de carga y de respuesta, debe copiar los archivos de carga y de respuesta en una nueva ubicación antes de responder.<br/> Un valor de 2 significa que BITS pasa el archivo de carga en el cuerpo de la solicitud a la aplicación de servidor especificada en la propiedad <strong>BITSServerNotificationURL</strong> . La aplicación de servidor procesa el archivo y devuelve la respuesta en el cuerpo de la respuesta, si es necesario.<br/> Para obtener más información sobre los encabezados de solicitud y respuesta, vea <a href="/windows/win32/bits/notification-protocol-for-server-applications">Protocolo de notificación para aplicaciones de servidor</a>.<br/> La aplicación de servidor debe proporcionar una respuesta en un plazo de cinco minutos. Si la aplicación de servidor no responde en un plazo de cinco minutos, el trabajo entra en el estado de error transitorio. Cuando expire el <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>intervalo entre reintentos</strong></a> , el servidor bits enviará otra notificación a la aplicación de servidor (se debe escribir la aplicación de servidor para que controle las notificaciones duplicadas). <strong>BITS 1,5:</strong> El tiempo de espera de notificación es de 30 segundos.<br/> <br/> El valor predeterminado es 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>BITSServerNotificationURL</strong> Tipo de datos: <strong>cadena</strong><br/></td>
<td>Opcional. Contiene la dirección URL de la aplicación de servidor a la que BITS envía el archivo de carga. Debe especificar una dirección URL si el valor de la propiedad <strong>BITSServerNotificationType</strong> es 1 o 2. La dirección URL está limitada a 2.200 caracteres, sin incluir el terminador null. La dirección URL debe ser una dirección URL HTTP; BITS no admite direcciones URL de notificación HTTPS.<br/> Si la dirección URL no está disponible en el momento de la carga, BITS volverá a intentar la carga hasta que la dirección URL de notificación exista o hasta que expire el período de reintento.<br/> Tenga en cuenta que si el nombre remoto especificado en el trabajo contiene una cadena de consulta, la cadena de consulta se anexará a la dirección URL que especifique. Por ejemplo, si el nombre remoto contiene https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 y especifica el valor de <strong>BITSServerNotificationURL</strong> como https://otherserver/myvdir2/bag.asp , la dirección URL a la que se publican los bits https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Si la dirección URL original es https://myserver/myvdir/file.txt y la dirección URL de notificación es myasp. asp, bits USA http//myvdir/myasp. asp como dirección URL de notificación.<br/> Si la parte de la ruta de acceso y el nombre de archivo de la dirección URL contiene caracteres Unicode que no son comunes a la página de códigos en el cliente y en el servidor, se producirá un error en la conversión de la dirección URL en el servidor y el trabajo de BITS se colocará en el estado de error. Si la parte del servidor de la dirección URL contiene caracteres Unicode, debe codificar la parte del servidor mediante el uso de <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">nombres de dominio internacionalizados</a> (IDN).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSHostId</strong> Tipo de datos: <strong>cadena</strong><br/></td>
<td>Establezca esta propiedad si la instalación del servidor es una granja de servidores web que no usa el almacenamiento compartido.<br/> Especifique el nombre del servidor o la dirección IP del servidor al que se va a volver a conectar después de que se interrumpa el proceso de carga. Normalmente, se especifica el nombre del servidor que se está configurando. La dirección URL está limitada a 300 caracteres, sin incluir el terminador null.<br/> Si no especifica esta propiedad y se interrumpe el proceso de carga, es posible que BITS reanude el trabajo en otro servidor de la granja. Sin embargo, el servidor anterior todavía contiene el archivo de carga parcial de antes de la interrupción. BITS quita el archivo parcial después de que expire el <strong>BITSSessionTimeout</strong> .<br/>
<blockquote>
[!Note]<br />
No use la propiedad <strong>BITSHostId</strong> si se usa SSL en una granja de servidores web que use el equilibrio de carga de red (NLB) o nombres DNS con varias direcciones IP, a menos que incluya el nombre del clúster y los nombres de servidor individuales en el certificado. (Si el nombre del servidor especificado en <strong>BITSHostId</strong> no coincide con el nombre común del certificado, se producirá un error en el trabajo.) En su lugar, para NLB, establezca el parámetro <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">affinity</a> en <strong>Single</strong> para asegurarse de que el cliente se comunica con el mismo servidor en el futuro.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSHostIdFallbackTimeout</strong> Tipo de datos: <strong>DWORD</strong><br/></td>
<td>Número de segundos que el cliente de BITS intenta volver a conectarse al nombre del servidor de <strong>BITSHostId</strong> antes de revertir al nombre de host especificado en el nombre de archivo remoto del trabajo. El temporizador se inicia cuando BITS no puede conectarse al servidor de <strong>BITSHostId</strong> . El temporizador se restablece cuando el cliente se conecta correctamente al servidor.<br/> Tenga en cuenta que el valor de tiempo de espera sin progreso del trabajo (vea <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>IBackgroundCopyJob:: SetNoProgressTimeout</strong></a>) debe ser mayor que este valor de tiempo de espera. En caso contrario, se producirá un error en el trabajo antes de que expire el valor de tiempo de espera de reserva.<br/> Establezca esta propiedad solo si establece la propiedad <strong>BITSHostId</strong> .<br/> El valor predeterminado es 86.400 (1 día).<br/></td>
</tr>
<tr class="even">
<td><strong>BITSAllowOverwrites</strong> Tipo de datos: <strong>entero</strong><br/></td>
<td>Indica si un archivo de carga puede sobrescribir un archivo existente con el mismo nombre. El archivo de carga sobrescribe el archivo existente si <strong>BITSAllowOverwrites</strong> es 1.<br/> El valor predeterminado es 0.<br/> <strong>IIS 6,0:</strong> Esta propiedad solo se puede establecer desde un script, no se puede establecer mediante la página de propiedades de la extensión BITS de la interfaz de usuario de IIS.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUseDefault</strong> Tipo de datos: <strong>booleano</strong><br/></td>
<td>Indica si la tarea de limpieza utiliza las programaciones predeterminadas. De forma predeterminada, la tarea de limpieza se ejecuta cada 12 horas.<br/> Establézcalo en 1 para usar la programación predeterminada; de lo contrario, 0 para especificar una programación.<br/> Para especificar una programación, use las propiedades <strong>BITSCleanupCount</strong> y <strong>BITSCleanupUnits</strong> .<br/> La tarea de limpieza limpia el directorio virtual eliminando los trabajos que no se han modificado en el período de tiempo de espera de la sesión (vea <strong>BITSSessionTimeout</strong>).<br/> El valor predeterminado es 1 usar la programación predeterminada.<br/> <strong>IIS 6,0:</strong> No compatible.<br/></td>
</tr>
<tr class="even">
<td><strong>BITSCleanupCount</strong> Tipo de datos: <strong>entero</strong><br/></td>
<td>Especifica el intervalo de espera entre la ejecución de la tarea de limpieza. El intervalo que se puede especificar depende de las unidades. Para ver los valores de intervalo posibles, vea la propiedad <strong>BITSCleanupUnits</strong> .<br/> Esta propiedad se omite si <strong>BITSCleanupUseDefault</strong> es 0.<br/> <strong>IIS 6,0:</strong> No compatible.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSCleanupUnits</strong> Tipo de datos: <strong>entero</strong><br/></td>
<td>Especifica las unidades del intervalo de limpieza especificado en la propiedad <strong>BITSCleanupCount</strong> . Esta propiedad se omite si <strong>BITSCleanupUseDefault</strong> es 0.<br/> Los valores posibles son:<dl> 0: las unidades son minutos. Los valores posibles son de 1 a 60.<br />
1: las unidades son horas. Este es el valor predeterminado. Los valores posibles son de 1 a 24.<br />
2: las unidades son días. Los valores posibles son de 1 a 360.<br />
</dl> <br/> <strong>IIS 6,0:</strong> No compatible.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>BITSNumberOfSessionsLimit</strong> Tipo de datos: <strong>entero</strong><br/></td>
<td>Limita el número de sesiones de carga que pueden existir simultáneamente para un usuario. Si el número de sesiones para un usuario supera este límite, cuando se ejecute la tarea de limpieza, se eliminarán las sesiones más recientes hasta que el número de sesiones del usuario esté por debajo del límite.<br/> El valor predeterminado es 50 sesiones.<br/> <strong>IIS 6,0:</strong> No compatible.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>BITSSessionLimitEnable</strong> Tipo de datos: <strong>booleano</strong><br/></td>
<td>Indica si BITS limita el número de sesiones de carga por usuario. Si el valor no está presente o es 0, se deshabilita el límite.<br/> Para especificar el límite, establezca la propiedad <strong>BITSNumberOfSessionsLimit</strong> .<br/> El valor predeterminado es 1.<br/> <strong>IIS 6,0:</strong> No compatible.<br/> <br/></td>
</tr>
</tbody>
</table>



 

En el ejemplo siguiente se muestra cómo establecer las propiedades de extensión de IIS de BITS mediante Windows Script Host. Si el directorio virtual apunta a un recurso compartido remoto, establezca también las propiedades de IIS **UNCUserName** y **UNCPassword** .


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



 

