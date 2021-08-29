---
title: Novedades (BITS)
description: En la tabla siguiente se identifican las novedades de cada versión de Servicio de transferencia inteligente en segundo plano (BITS).
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- novedades de BITS
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 9d7a27187b0f3ac9cb0bf74c7b57afaacd7498dd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474301"
---
# <a name="whats-new-bits"></a>Novedades (BITS)

Desde su primera versión como parte de Windows XP, Servicio de transferencia inteligente en segundo plano (BITS) se ha mejorado constantemente, lo que agrega controles más eficaces para que el desarrollador y el administrador controlen y administren las descargas. Se ha agregado un amplio conjunto de cmdlets de PowerShell. puede conectarse a más tipos de servidores HTTP; es más cuidadosa que nunca el ancho de banda y los costos de red del usuario. 

En la tabla siguiente se identifican las novedades de cada versión de Servicio de transferencia inteligente en segundo plano (BITS).




| Versión | Descripción de las características | 
|---------|-------------------------|
| Versión 10.3 | Características nuevas:<br /><ul><li>Se ha <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>agregado BackgroundCopyJobHttpOptions3</strong></a> para marcar los encabezados HTTP como de solo escritura y para establecer una devolución de llamada de validación de certificados de servidor.</li><li>BITS conservará su identidad de servicio cuando lo cree otro servicio del sistema.</li><li>BITS seguirá transfiriendo archivos en espera conectado siempre que el dispositivo esté conectado.</li></ul>Bits versión 10.3 se incluye en el Actualización de mayo de 2019 de Windows 10 (10.0; Compilación 18362) y versiones posteriores. | 
| Versión 10.2 | Características nuevas:<br /><ul><li>Se ha <a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>agregado BackgroundCopyJobHttpOptions2 para</strong></a> cambiar el método HTTP para las descargas HTTP.</li><li>BITS ahora usa la ordenación de proxy predeterminada para ser más coherente con el resto del sistema.</li><li>Es más fácil para los programadores establecer la configuración del proxy bits para escenarios empresariales.</li><li>BITS ahora tiene más cuidado con la energía y admite [el modo de espera moderno.](/windows-hardware/design/device-experiences/modern-standby)</li><li>BITS ahora admite directivas de administrador de [dispositivos](/windows/client-management/mdm/policy-configuration-service-provider) móviles (MDM), además de [directivas de grupo.](./group-policies)</li></ul>Bits versión 10.2 se incluye en Actualización de octubre de 2018 de Windows 10(10.0; Compilación 17763) y versiones posteriores. | 
| Versión 10.1 | Características nuevas:<br /><ul><li>Se han agregado <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>e IBackgroundCopyCallback3</strong></a> para habilitar escenarios de acceso aleatorio para descargas HTTP.</li><li>Se han <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> y <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> a la enumeración <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> para ajustar los comportamientos de descarga y notificación, respectivamente.</li></ul>Bits versión 10.1 se incluye en Windows 10 Creator's Update y versiones posteriores. | 
| Versión 5.0 | Características nuevas:<br /><ul><li>Se ha agregado la <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>interfaz IBackgroundCopyJob5</strong></a> que agrega métodos genéricos para obtener y establecer propiedades de trabajo bits a los métodos heredados de la <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>interfaz IBackgroundCopyJob4.</strong></a><br /> Para obtener información sobre el uso de la nueva interfaz <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5,</strong></a> consulte Cómo controlar si un trabajo <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">de BITS</a> puede descargarse a través de una conexión costosa y Cómo obtener el último conjunto de encabezados HTTP recibidos para cada archivo en un trabajo de descarga de <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">BITS.</a><br /></li><li>Se han agregado <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> y las <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>enumeraciones BITS_JOB_PROPERTY_ID</strong></a>, <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>y BITS_JOB_TRANSFER_POLICY</strong></a> enumeraciones. Para obtener ejemplos de uso, vea los temas de cómo.</li><li>Se ha agregado la <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>interfaz IBackgroundCopyFile5,</strong></a> que agrega métodos para obtener y establecer propiedades genéricas en objetos BackgroundCopyFile a los métodos heredados de la <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>interfaz IBackgroundCopyFile4.</strong></a> La adición de propiedades genéricas permitirá mejorar las funcionalidades de BackgroundCopyFile en el futuro sin necesidad de crear una nueva interfaz.</li><li>La primera propiedad genérica expuesta por <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> es <strong>la propiedad HttpResponseHeaders.</strong></li><li>Se han agregado <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>la BITS_FILE_PROPERTY_VALUE</strong></a> y <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>la</strong></a> BITS_FILE_PROPERTY_ID enumeración.</li></ul>Bits versión 5.0 se incluye en los sistemas operativos Windows Server 2012 y Windows 8, donde la versión de %windir%\System32\QMgr.dll es "7.7.xxxx.xxxx".<br /> Las siguientes características se agregaron a BITS en Windows 10<br /><ul><li>En Windows 10, versión 1607, es posible usar las API COM de BITS y los cmdlets de PowerShell bits (si están disponibles) en una sesión remota de PowerShell. Esto es especialmente útil al administrar versiones de Windows Server 2016 que no tienen ninguna funcionalidad de inicio de sesión local. Los trabajos de BITS iniciados a través de sesiones remotas de PowerShell se ejecutan en el contexto de la cuenta de usuario de la sesión y solo avanzarán cuando haya al menos una sesión iniciada o una sesión remota de PowerShell activa asociada con dicha cuenta de usuario. Considere la posibilidad de usar sesiones remotas de PowerShell persistentes <a href="/powershell/module/microsoft.powershell.core/new-pssession">(consulte New-PSSession</a>) para transferencias de larga duración.</li><li>En Windows 10, versión 1607, ahora es posible que un propietario del trabajo bits establezca tokens auxiliares sin ser administrador, siempre y cuando el token auxiliar no tenga funcionalidades de administrador. Esto reduce la superficie de vulnerabilidad de las herramientas de descarga o actualización en segundo plano, ya que permite que se ejecuten con la cuenta NetworkService con menos privilegios, en lugar de con una cuenta con privilegios administrativos.</li></ul>Bits versión 5.0 también se incluye en Windows 10, donde la versión de %windir%\System32\QMgr.dll es "7.8.xxxx.xxxx".<br /> | 
| Versión 4.0 | Características nuevas:<br /><ul><li>El almacenamiento en caché del mismo nivel ahora usa Windows BranchCache. Este nuevo modelo de almacenamiento en caché del mismo nivel reemplaza el modelo usado para BITS versión 3.0. Para obtener más información, vea <a href="peer-caching.md">Almacenamiento en caché del mismo nivel.</a></li><li>Se ha agregado un modelo de acceso a recursos más flexible que permite a las aplicaciones asociar un par de tokens de seguridad a un trabajo de transferencia de BITS. Para obtener más información, vea <a href="helper-tokens-for-bits-transfer-jobs.md">Tokens auxiliares para trabajos de transferencia de BITS.</a></li><li>Se ha agregado <a href="bits-compact-server.md">bits compact server</a>, que es un servidor de archivos HTTP/HTTPS independiente que proporciona la capacidad de transferir un número limitado de archivos de gran tamaño de forma asincrónica entre equipos.</li><li>Se ha agregado una limitación de ancho de banda más granular. Para obtener más información, vea <a href="group-policies.md">Directivas de grupo.</a></li></ul>Bits versión 4.0 se incluye en los sistemas operativos Windows Server 2008 R2 y Windows 7.<br /> También puede descargar BITS 4.0 para Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) y Windows Vista con Service Pack 2 (SP2). Para obtener información sobre cómo descargar BITS 4.0, vea <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br /> La versión de %windir%\System32\QMgr.dll es "7.5.xxxx.xxxx".<br /> | 
| Versión 3.0 | Características nuevas:<br /><ul><li>Se ha agregado <a href="peer-caching.md">el almacenamiento en caché del</a> mismo nivel, que permite descargar contenido de los pares y también servir contenido a los pares de una red de dominio.</li><li>Se ha <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">agregado una</a> notificación para cuando se descarga un archivo.</li><li>Se ha agregado acceso al <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">archivo temporal mientras</a> la descarga está en curso.</li><li>Se ha agregado la capacidad de controlar las <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">redirecciones</a>HTTP .</li><li>Se han agregado más <a href="group-policies.md">directivas de grupo para</a> controlar el almacenamiento en caché del mismo nivel y limitar los tiempos de descarga.</li><li>Se han agregado eventos de diagnóstico y solución de problemas al registro de eventos del sistema.</li><li>Se ha agregado compatibilidad con <a href="user-account-control-and-bits.md">el control de cuentas de</a> usuario (UAC).</li><li>En Windows Vista y versiones posteriores, el tipo de inicio predeterminado de BITS es el inicio automático retrasado.</li></ul><blockquote>[!Note]<br />BITS ahora usa directivas de grupo para limitar el número de trabajos y archivos que puede crear. Esto puede afectar a las aplicaciones que actualmente crean un gran número de trabajos o agregan un gran número de archivos a un trabajo.</blockquote><br /><br /> BITS versión 3.0 se incluye en los sistemas operativos Windows Server 2008 y Windows Vista. <br /> La versión de %windir%\System32\QMgr.dll es "7.0.xxxx.xxxx".<br /> | 
| Versión 2.5 | Se ha agregado compatibilidad con encabezados HTTP personalizados, autenticación de cliente basada en certificados para transportes HTTP seguros e IPv6. También se ha agregado el uso de contadores de dispositivo de puerta de enlace de Internet (IGD) para calcular con más precisión el ancho de banda <a href="network-bandwidth.md">disponible.</a><br /> Las características de BITS 2.5 están disponibles en los sistemas operativos Windows Server 2008, Windows Vista y Windows XP con Service Pack 3 (SP3). <br /> También puede descargar BITS 2.5 para Windows Server 2003 con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) y Windows XP con Service Pack 2 (SP2). Para descargar BITS 2.5, vaya al Centro <a href="https://www.microsoft.com/download/details.aspx?id=4933">de descarga de Microsoft</a> e instale KB923845.<br /> La versión de %windir%\System32\QMgr.dll es "6.7.xxxx.xxxx".<br /> | 
| Versión 2.0 | Se ha agregado compatibilidad para realizar descargas simultáneas en primer plano, usar rutas de acceso de bloque de mensajes del servidor (SMB) para nombres remotos, descargar intervalos de un archivo, cambiar el prefijo o el nombre completo de un nombre remoto y limitar el uso de ancho de banda de cliente. La directiva JobInactivityTimeout ahora se encuentra en Configuración del equipo, Plantillas administrativas, Red, Servicio de transferencia inteligente en segundo plano (BITS).<br /> BITS versión 2.0 se incluye en Windows XP con SP2 y Windows Server 2003 con SP1. También puede descargar BITS 2.0 para Windows Server 2003 y Windows XP. Para descargar BITS 2.0, vaya al Centro de <a href="https://www.microsoft.com/download/details.aspx?id=19031">descarga de Microsoft</a> e instale KB842773.<br /> La versión de %windir%\System32\QMgr.dll es "6.6.xxxx.xxxx".<br /> | 
| Versión 1.5 | Se ha agregado la funcionalidad de carga y carga y respuesta, la ejecución de la línea de comandos para eventos y las credenciales explícitas y las credenciales de proxy.<br /> A partir de BITS 1.5, los usuarios con <a href="/windows/win32/secauthz/restricted-tokens">un token restringido</a> no pueden crear ni modificar trabajos.<br /> Bits versión 1.5 se incluye en Windows Server 2003. Hay disponible un redistribuible para Windows XP desde el <a href="https://www.microsoft.com/download/details.aspx?id=22250">Centro de descarga de Microsoft</a>.<br /> La versión de %windir%\System32\QMgr.dll es "6.5.xxxx.xxxx".<br /> | 
| Versión 1.2 | La misma funcionalidad que la versión 1.0. Contiene actualizaciones y mejoras internas.<br /> Bits versión 1.2 se incluye en Windows XP con Service Pack 1 (SP1).<br /> La versión de %windir%\System32\QMgr.dll es "6.2.xxxx.xxxx".<br /> | 
| Versión 1.0 | Versión inicial. Proporciona descargas prioritarias, limitadas y asincrónicas en segundo plano o en primer plano. Las descargas se reanudan automáticamente después de reiniciar el equipo y desconectar la red.<br /> Bits versión 1.0 se incluye en Windows XP.<br /> La versión de %windir%\System32\QMgr.dll es "6.0.xxxx.xxxx".<br /> | 


Para mejorar las características del programa en función de las funcionalidades de BITS, use QueryInterface en (por ejemplo) el objeto Job para ver si el objeto Job le permite crear la versión que necesita. Como alternativa, vea [Determinar la versión de BITS en un](./determining-the-version-of-bits-on-a-computer.md) equipo para convertir el número de QMgr.dll en la versión de BITS.

## <a name="version-103"></a>Versión 10.3

Se agregaron las interfaces siguientes para esta versión.
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Versión 10.2

Se agregaron las interfaces siguientes para esta versión.
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Versión 10.1

Se agregaron las interfaces siguientes para esta versión.
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Se agregaron las siguientes constantes para usarlas con la [enumeración BITS_JOB_PROPERTY_ID enumeración](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id).

-   **BITS \_ JOB \_ PROPERTY \_ ON \_ DEMAND \_ MODE**
-   **BITS \_ JOB \_ PROPERTY \_ MINIMUM \_ NOTIFICATION \_ INTERVAL \_ MS**


## <a name="version-50"></a>Versión 5.0

Se agregaron las interfaces siguientes para esta versión:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Versión 4.0

Se agregaron las interfaces siguientes para esta versión:

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Versión 3.0

Se agregaron las interfaces siguientes para esta versión:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Se agregaron las siguientes constantes para usarlas con el método [**IBackgroundCopyJobHttpOptions::SetSecurityFlags:**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags)

-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ ALLOW \_ SILENT**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ ALLOW \_ REPORT**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ DISALLOW**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ MASK**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ ALLOW \_ HTTPS \_ TO \_ HTTP**

## <a name="version-25"></a>Versión 2.5

Se agregaron la siguiente interfaz y enumeración para la versión 2.5:

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**UBICACIÓN \_ DEL ALMACÉN DE CERTIFICADOS \_ \_ DE BG**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Versión 2.0

Se agregaron las interfaces, la estructura y los temas siguientes para la versión 2.0:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**INTERVALO \_ DE ARCHIVOS \_ BG**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Directivas de grupo](group-policies.md)

Para obtener información sobre las descargas simultáneas en primer plano, vea la sección Comentarios de [**BG \_ JOB \_ PRIORITY**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Para obtener información sobre el uso del protocolo SMB, vea [**BG \_ FILE \_ INFO**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Versión 1.5

Se agregaron las interfaces y los temas siguientes para la versión 1.5:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Recuperar la respuesta de un trabajo Upload-Reply trabajo](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registro para ejecutar un programa](registering-to-execute-a-program.md)
-   [Bits Server Configuración for Upload Jobs](bits-server-settings-for-upload-jobs.md)
-   [Configuración del servidor para cargas](setting-up-the-server-for-uploads.md)
-   [Uso de encabezados de solicitud/respuesta de notificación de BITS](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Actualización de versiones de BITS
 
Puede descargar BITS 4.0 para Windows Server 2008 con Service Pack 2 (SP2), Windows Vista con Service Pack 1 (SP1) y Windows Vista con Service Pack 2 (SP2). Para obtener información sobre cómo descargar BITS 4.0, vea [KB968929](https://support.microsoft.com/kb/968929).
