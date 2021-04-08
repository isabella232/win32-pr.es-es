---
title: Novedades (BITS)
description: En la tabla siguiente se identifican las novedades de cada versión de Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- Novedades de los BITS
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078685"
---
# <a name="whats-new-bits"></a>Novedades (BITS)

Desde su primera versión como parte de Windows XP, el Servicio de transferencia inteligente en segundo plano (BITS) se ha mejorado constantemente, agregando controles más eficaces para que el desarrollador y el administrador controlen y administren las descargas. Se ha agregado un amplio conjunto de cmdlets de PowerShell. puede conectarse a más tipos de servidores HTTP; el ancho de banda y los costos de red del usuario son más cuidados que nunca. 

En la tabla siguiente se identifican las novedades de cada versión de Servicio de transferencia inteligente en segundo plano (BITS).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versión</th>
<th>Descripción de las características</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versión 10,3</td>
<td>Características nuevas:<br/>
<ul>
<li>Se ha agregado <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> para marcar los encabezados HTTP como de solo escritura y para establecer una devolución de llamada de validación de certificado de servidor.</li>
<li>BITS conservará su identidad de servicio cuando lo cree otro servicio de sistema.</li>
<li>BITS seguirá transfiriendo archivos en modo de espera conectado siempre que el dispositivo esté conectado.</li>
</ul>
La versión 10,3 de BITS se incluye en la actualización de Windows 10 mayo de 2019 (10,0; Compilación 18362) y versiones posteriores.
</td>
</tr>
<tr class="even">
<td>Versión 10,2</td>
<td>Características nuevas:<br/>
<ul>
<li>Se ha agregado <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> para cambiar el método http para descargas http.</li>
<li>BITS ahora usa la ordenación de proxy predeterminada para que sea más coherente con el resto del sistema.</li>
<li>Es más fácil para los programadores establecer la configuración del proxy de BITS para escenarios empresariales.</li>
<li>BITS es ahora más cuidadoso y admite el [modo de espera moderno](/windows-hardware/design/device-experiences/modern-standby).</li>
<li>Los BITS ahora admiten [las directivas](/windows/client-management/mdm/policy-configuration-service-provider) del administrador de dispositivos móviles (MDM) además de [las directivas de grupo](./group-policies).</li>
</ul>
La versión 10,2 de BITS se incluye en la actualización de Windows 10 de octubre de 2018 (10.0). Compilación 17763) y versiones posteriores.
</td>
</tr>
<tr class="odd">
<td>Versión 10,1</td>
<td>Características nuevas:<br/>
<ul>
<li>Se han agregado <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> y <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> para habilitar escenarios de acceso aleatorio para descargas http.</li>
<li>Se han agregado <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> y <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> a la enumeración <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> para modificar los comportamientos de descarga y notificación, respectivamente.</li>
</ul>
La versión 10,1 de BITS se incluye en la actualización de Windows 10 Creator y versiones posteriores.
</td>
</tr>
<tr class="even">
<td>Versión 5.0</td>
<td>Características nuevas:<br/>
<ul>
<li>Se ha agregado la interfaz <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> que agrega métodos genéricos para obtener y establecer las propiedades del trabajo de bits en los métodos heredados de la interfaz <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> .<br/> Para obtener información sobre el uso de la nueva interfaz <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> , consulte <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">Cómo controlar si un trabajo de bits puede descargarse a través de una conexión costosa</a> y <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">Cómo obtener el último conjunto de encabezados HTTP recibidos para cada archivo en un trabajo de descarga de bits</a>.<br/></li>
<li>Se han agregado los <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> Unión y las enumeraciones <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>y <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> . Para obtener ejemplos de uso, vea los temas de procedimientos anteriores.</li>
<li>Se ha agregado la interfaz <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> , que agrega métodos para obtener y establecer propiedades genéricas en objetos BackgroundCopyFile en los métodos heredados de la interfaz <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> . La adición de propiedades genéricas permitirá mejorar las capacidades de BackgroundCopyFile en el futuro sin necesidad de crear una nueva interfaz.</li>
<li>La primera propiedad genérica expuesta por <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> es la propiedad <strong>HttpResponseHeaders</strong> .</li>
<li>Se han agregado los <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> Unión y la enumeración <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> .</li>
</ul>
La versión 5,0 de BITS se incluye en los sistemas operativos Windows Server 2012 y Windows 8, donde la versión de% WINDIR% \System32\QMgr.dll es &quot; 7.7. xxxx. xxxx &quot; .<br/> Las siguientes características se han agregado a BITS en Windows 10<br/>
<ul>
<li>En la versión 1607 de Windows 10, es posible usar las API COM de BITS y los cmdlets de PowerShell de BITS (si están disponibles) en una sesión remota de PowerShell. Esto es especialmente útil cuando se administran versiones de Windows Server 2016 que no tienen ninguna funcionalidad de inicio de sesión local. Los trabajos de BITS iniciados a través de sesiones remotas de PowerShell se ejecutan en el contexto de la cuenta de usuario de la sesión y solo avanzarán cuando haya al menos una sesión iniciada o una sesión remota de PowerShell activa asociada con dicha cuenta de usuario. Considere la posibilidad de usar sesiones remotas de PowerShell persistentes (consulte <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) para las transferencias de ejecución prolongada.</li>
<li>En Windows 10, versión 1607, ahora es posible que un propietario del trabajo de BITS establezca tokens auxiliares sin ser un administrador, siempre que el token auxiliar no tenga funciones de administrador. Esto reduce la superficie de vulnerabilidad de las herramientas de descarga o actualización en segundo plano, ya que permite que se ejecuten con la cuenta NetworkService con menos privilegios, en lugar de con una cuenta con privilegios administrativos.</li>
</ul>
La versión 5,0 de BITS también se incluye en Windows 10, donde la versión de% WINDIR% \System32\QMgr.dll es &quot; 7.8. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versión 4.0</td>
<td>Características nuevas:<br/>
<ul>
<li>El almacenamiento en caché del mismo nivel usa ahora Windows BranchCache. Este nuevo modelo de almacenamiento en caché del mismo nivel reemplaza el modelo usado para la versión de BITS 3,0. Para obtener más información, consulte <a href="peer-caching.md">almacenamiento en caché del mismo nivel</a>.</li>
<li>Se ha agregado un modelo de acceso a recursos más flexible que permite a las aplicaciones asociar un par de tokens de seguridad a un trabajo de transferencia de BITS. Para obtener más información, consulte <a href="helper-tokens-for-bits-transfer-jobs.md">tokens de aplicación auxiliar para trabajos de transferencia de bits</a>.</li>
<li>Se ha agregado el <a href="bits-compact-server.md">servidor bits compacto</a>, que es un servidor de archivos http/https independiente que proporciona la capacidad de transferir un número limitado de archivos grandes de forma asincrónica entre equipos.</li>
<li>Se ha agregado más limitación de ancho de banda granular. Para obtener más información, consulte <a href="group-policies.md">directivas de grupo</a>.</li>
</ul>
La versión 4,0 de BITS se incluye en los sistemas operativos Windows Server 2008 R2 y Windows 7.<br/> También puede descargar BITS 4,0 para Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) y Windows Vista con Service Pack 2 (SP2). Para obtener información sobre cómo descargar BITS 4,0, vea <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 7,5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versión 3.0</td>
<td>Características nuevas:<br/>
<ul>
<li>Se ha agregado <a href="peer-caching.md">almacenamiento en caché del mismo nivel</a> que permite descargar contenido de equipos del mismo nivel y también servir contenido a equipos del mismo nivel en una red de dominio.</li>
<li>Se ha agregado una <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">notificación</a> para cuando se descarga un archivo.</li>
<li>Se ha agregado acceso al <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">archivo temporal</a> mientras la descarga está en curso.</li>
<li>Se ha agregado la capacidad de controlar las <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">redirecciones</a>http.</li>
<li>Se agregaron más <a href="group-policies.md">directivas de grupo</a> para controlar el almacenamiento en caché del mismo nivel y limitar los tiempos de descarga.</li>
<li>Se han agregado eventos de diagnóstico y solución de problemas al registro de eventos del sistema.</li>
<li>Compatibilidad agregada para el <a href="user-account-control-and-bits.md">control de cuentas de usuario</a> (UAC).</li>
<li>En Windows Vista y versiones posteriores, el tipo de inicio de BITS predeterminado es el inicio automático retrasado.</li>
</ul>
<blockquote>
[!Note]<br />
BITS ahora usa directivas de grupo para limitar el número de trabajos y archivos que se pueden crear. Esto podría afectar a las aplicaciones que actualmente crean un gran número de trabajos o que agregan un gran número de archivos a un trabajo.
</blockquote>
<br/> <br/> La versión 3,0 de BITS se incluye en los sistemas operativos Windows Server 2008 y Windows Vista. <br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versión 2.5</td>
<td>Se ha agregado compatibilidad con los encabezados HTTP personalizados, la autenticación de cliente basada en certificados para transportes HTTP seguros y IPv6. También se ha agregado el uso de contadores de dispositivo de puerta de enlace a Internet (IGD) para calcular de forma más precisa el <a href="network-bandwidth.md">ancho de banda</a>disponible.<br/> Las características de BITS 2,5 están disponibles en los sistemas operativos Windows Server 2008, Windows Vista y Windows XP con Service Pack 3 (SP3). <br/> También puede descargar BITS 2,5 para Windows Server 2003 con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) y Windows XP con Service Pack 2 (SP2). Para descargar BITS 2,5, vaya al <a href="https://www.microsoft.com/download/details.aspx?id=4933">centro de descarga de Microsoft</a> e instale KB923845.<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versión 2.0</td>
<td>Se ha agregado compatibilidad con la realización de descargas de primer plano simultáneas, mediante rutas de acceso de bloque de mensajes del servidor (SMB) para nombres remotos, la descarga de intervalos de un archivo, el cambio de prefijo o el nombre completo de un nombre remoto y la limitación del uso del ancho de banda del cliente La Directiva valor jobinactivitytimeout se encuentra ahora en configuración del equipo, Plantillas administrativas, red, Servicio de transferencia inteligente en segundo plano (BITS).<br/> La versión 2,0 de BITS se incluye en Windows XP con SP2 y Windows Server 2003 con SP1. También puede descargar BITS 2,0 para Windows Server 2003 y Windows XP. Para descargar BITS 2,0, vaya al <a href="https://www.microsoft.com/download/details.aspx?id=19031">centro de descarga de Microsoft</a> e instale KB842773.<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 6.6. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versión 1.5</td>
<td>Se han agregado funciones de carga y de carga y respuesta, ejecución de línea de comandos para eventos, credenciales explícitas y credenciales de proxy.<br/> A partir de los BITS 1,5, los usuarios con un <a href="/windows/win32/secauthz/restricted-tokens">token restringido</a> no pueden crear ni modificar trabajos.<br/> La versión 1,5 de BITS se incluye en Windows Server 2003. Un paquete redistribuible está disponible para Windows XP desde el <a href="https://www.microsoft.com/download/details.aspx?id=22250">centro de descarga de Microsoft</a>.<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 6.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Versión 1.2</td>
<td>La misma funcionalidad que la versión 1,0. Contiene las actualizaciones y mejoras internas.<br/> La versión 1,2 de BITS se incluye en Windows XP con Service Pack 1 (SP1).<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 6.2. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Versión 1.0</td>
<td>Versión inicial. Proporciona descargas prioritarias, limitadas y asincrónicas en segundo plano o en primer plano. Las descargas se reanudan automáticamente después de que el equipo se reinicie y se desconecte la red.<br/> La versión 1,0 de BITS se incluye en Windows XP.<br/> La versión de% WINDIR% \System32\QMgr.dll es &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Para aclarar las características del programa en función de las capacidades de BITS, use QueryInterface en (por ejemplo) el objeto de trabajo para ver si el objeto de trabajo le permite crear la versión que necesita. También puede ver la [determinación de la versión de bits en un equipo](./determining-the-version-of-bits-on-a-computer.md) para convertir el número de versión QMgr.dll en la versión de bits.

## <a name="version-103"></a>Versión 10,3

Se han agregado las siguientes interfaces para esta versión
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Versión 10,2

Se han agregado las siguientes interfaces para esta versión
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Versión 10,1

Se han agregado las siguientes interfaces para esta versión
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Se han agregado las siguientes constantes para usar con la [enumeración BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **\_ \_ propiedad de trabajo \_ de bits en \_ modo de petición \_**
-   **\_intervalo de \_ notificación mínimo de la propiedad de trabajo de bits \_ \_ \_ \_ MS**


## <a name="version-50"></a>Versión 5.0

Se han agregado las siguientes interfaces para esta versión:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Versión 4.0

Se han agregado las siguientes interfaces para esta versión:

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Versión 3.0

Se han agregado las siguientes interfaces para esta versión:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Se han agregado las siguientes constantes para usarlas con el método [**IBackgroundCopyJobHttpOptions:: SetSecurityFlags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) :

-   **la \_ Directiva de redirección http de BG \_ \_ permite el \_ \_ modo silencioso**
-   **la \_ Directiva de redirección http de BG \_ \_ permite el \_ \_ Informe**
-   **\_Directiva de redirección http de BG no \_ \_ \_ permitida**
-   **\_máscara de \_ Directiva de redirección http \_ de BG \_**
-   **la \_ \_ Directiva de redirección http \_ de BG \_ permite \_ https \_ a \_ http**

## <a name="version-25"></a>Versión 2.5

Se han agregado la siguiente interfaz y enumeración para la versión 2,5:

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**\_Ubicación del \_ almacén de certificados de BG \_**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Versión 2.0

Se han agregado las siguientes interfaces, estructuras y temas para la versión 2,0:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_intervalo del archivo BG \_**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Directivas de grupo](group-policies.md)

Para obtener información acerca de las descargas de primer plano simultáneas, consulte la sección Comentarios para la [**\_ \_ prioridad del trabajo de BG**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Para obtener información sobre el uso del protocolo SMB, consulte [**\_ \_ información del archivo BG**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Versión 1.5

Se han agregado las siguientes interfaces y temas para la versión 1,5:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Recuperación de la respuesta de un trabajo Upload-Reply](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registro para ejecutar un programa](registering-to-execute-a-program.md)
-   [Configuración del servidor BITS para trabajos de carga](bits-server-settings-for-upload-jobs.md)
-   [Configuración del servidor para cargas](setting-up-the-server-for-uploads.md)
-   [Usar encabezados de solicitud/respuesta de notificación BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Actualizar versiones de BITS
 
Puede descargar BITS 4,0 para Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) y Windows Vista con Service Pack 2 (SP2). Para obtener información sobre cómo descargar BITS 4,0, vea [KB968929](https://support.microsoft.com/kb/968929).
