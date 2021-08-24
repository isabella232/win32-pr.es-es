---
title: Procedimientos recomendados al usar BITS
description: Esta sección contiene información que debe tener en cuenta al diseñar una aplicación que usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: cbc11365cde74e092ae179c8b41562a16de9a6c36f0d85e51787a979c9332863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702095"
---
# <a name="best-practices-when-using-bits"></a>Procedimientos recomendados al usar BITS

Esta sección contiene información que debe tener en cuenta al diseñar una aplicación que usa BITS.

## <a name="user-context-or-service-context"></a>Contexto de usuario o contexto de servicio

BITS transfiere archivos solo cuando el propietario del trabajo ha iniciado sesión en el equipo (el usuario debe haber iniciado sesión de forma interactiva). BITS no admite el **comando RunAs.** Para más información, consulte [Usuarios y conexiones de red.](users-and-network-connections.md)

Si no necesita el contexto de un usuario para la aplicación, considere la posibilidad de escribir un servicio que se ejecute como LocalSystem, LocalService o NetworkService en su lugar. Estas cuentas del sistema siempre inician sesión, por lo que la transferencia no está sujeta a un registro de usuario. Sin embargo, si suplanta a un usuario al crear el trabajo, se aplican las reglas de inicio de sesión interactivo. Para más información, consulte [Cuentas de servicio y BITS.](service-accounts-and-bits.md)

## <a name="jobs-are-persistent"></a>Los trabajos son persistentes

Los trabajos permanecen en la cola hasta que se llama al [**método IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o [**IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) Los archivos del trabajo no están disponibles para el usuario hasta que se llama a **Complete**. Normalmente, se llama a **Complete** cuando el estado del trabajo es **BG JOB STATE \_ \_ \_ TRANSFERRED** y se llama a **Cancel** cuando el trabajo está en el estado BG JOB STATE **TRANSIENT \_ \_ \_ \_ ERROR** o **BG JOB STATE \_ \_ \_ ERROR** y ya no puede avanzar.

Si no llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) en un plazo de 90 días (el valor predeterminado [directiva de grupo JobInactivityTimeout),](group-policies.md) el servicio cancela el trabajo. Siempre debe llamar al método **Complete** o **Cancel** y no confiar en la directiva JobInactivityTimeout para limpiar los trabajos. Los trabajos que quedan en la cola pueden impedir que los usuarios creen otros trabajos si se alcanza el límite de directivas MaxJobsPerUser o MaxJobsPerMachine.

## <a name="when-to-use-foreground-or-background-priority"></a>Cuándo usar prioridad en primer plano o en segundo plano

A menos que el trabajo sea crítico para el tiempo o que el usuario esté esperando activamente, siempre debe usar una prioridad en segundo plano. Sin embargo, hay ocasiones en las que es posible que quiera cambiar de prioridad en segundo plano a prioridad en primer plano, por ejemplo, cuando el proxy o el servidor no admiten el encabezado Content-Range, o cuando el software antivirus del cliente quita la solicitud de encabezado de intervalo. Cambiar a prioridad en primer plano solo funciona para los archivos cuyo tamaño de archivo es inferior a 2 GB. Para obtener un ejemplo, vea la implementación del [**método IBackgroundCopyCallback::JobError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) Tenga en cuenta también que si el trabajo en primer plano se interrumpe debido a una desconexión de red o al inicio de sesión del usuario, se producirá un error en el trabajo porque BITS enviará una solicitud de intervalo para intentar reiniciar la transferencia desde donde la dejó.

A partir Windows 8, debe configurar los trabajos de descarga con **BITS JOB PROPERTY DYNAMIC \_ \_ \_ \_ CONTENT** y **BG JOB PRIORITY \_ \_ \_ FOREGROUND** al establecer como destino servidores que no cumplan los requisitos HTTP para las descargas [de BITS.](http-requirements-for-bits-downloads.md) Tenga en cuenta que esto dará lugar a que BITS tenga que reiniciar la descarga desde el principio si alguna vez se interrumpe (por ejemplo, debido a problemas de conectividad o reinicio del sistema).

Para obtener información sobre las prioridades disponibles y cómo BITS usa el nivel de prioridad para programar trabajos, vea [**BG \_ JOB \_ PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Errores transitorios y irreales

Algunos errores son recuperables y otros no. Por ejemplo, el error "El servidor no está disponible" es un error recuperable y el error "Acceso denegado" es un error irrecuperable. BITS coloca los errores recuperables en un estado de error transitorio e intenta de nuevo el trabajo después de un intervalo especificado. Si el trabajo no puede avanzar, BITS mueve el trabajo a un estado de error grave. Use los [**métodos IBackgroundCopyJob::SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) [**e IBackgroundCopyJob::SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar cómo bits procesa los errores transitorios.

Para los trabajos en primer plano, debe limitar la cantidad de tiempo que deja que un trabajo permanezca en estado de error transitorio e intente recuperarse. Use el [**método SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para limitar la cantidad de tiempo que un trabajo permanece en estado de error transitorio o para forzar el trabajo al estado de error grave. Si deja que el trabajo intente recuperarse, debe usar el método [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) para establecer el retraso de reintento mínimo en 60 segundos o llamar al método [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para volver a activar el trabajo.

Para obtener más información, vea [**BG \_ JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [Life Cycle of a BITS Job y](life-cycle-of-a-bits-job.md)Handling [Errors](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Medición del uso del ancho de banda de red

BITS puede usar el adaptador de red del cliente para calcular el ancho de banda de red disponible. Dado que BITS no puede medir el ancho de banda más allá del cliente, BITS puede ingerir el vínculo WAN. Para reducir la congestión en el vínculo WAN, puede usar la directiva de grupo **MaxInternetBandwidth** para limitar la cantidad de ancho de banda que usa el cliente. Para obtener más información, vea [Ancho de banda de red](network-bandwidth.md) y directivas de [grupo.](group-policies.md)

Si está escribiendo una aplicación que muchos clientes usarán para descargar archivos de un servidor determinado, debe considerar un esquema que escalona las solicitudes de descarga para no sobrecargar el servidor con solicitudes.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Establecimiento de credenciales para la autenticación de servidor y proxy

Si espera que el servidor proxy o el servidor requieran credenciales de usuario, debe proporcionar las credenciales a BITS. Para especificar las credenciales, llame al [**método IBackgroundCopyJob2::SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) BITS admite los esquemas de autenticación Basic, Digest, Negotiate, NTLM y Passport.

Para más información sobre la autenticación, consulte [Autenticación](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Especificación de la configuración de proxy para cuentas de usuario y cuentas de servicio

De forma predeterminada, BITS usa la configuración del proxy Internet Explorer usuario. Para invalidar la configuración del proxy Internet Explorer usuario, llame al [**método IBackgroundCopyJob::SetProxySettings.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)

La configuración del proxy Internet Explorer no se aplica a las cuentas del sistema, por lo que el comportamiento predeterminado del proxy **(BG \_ JOB PROXY \_ USAGE \_ \_ PRECONFIG)** solo funcionará correctamente en las implementaciones del Protocolo de detección automática de proxy web (WPAD), a menos que se realicen pasos de configuración adicionales. Si la aplicación es un servicio que se ejecuta como LocalSystem, LocalService o NetworkService, considere la posibilidad de configurar un token auxiliar en los trabajos de BITS o establecer explícitamente la configuración de proxy correcta mediante una llamada a [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG JOB PROXY USAGE \_ \_ \_ \_ OVERRIDE**. Como alternativa, puede usar los modificadores **/Util /SetIEProxy** de BitsAdmin.exe Internet Explorer para establecer una configuración de proxy para la cuenta del sistema LocalSystem, LocalService o NetworkService. Para obtener más información, [vea BitsAdmin Tool](bitsadmin-tool.md).

BITS no reconoce la configuración de proxy que se establece mediante Proxycfg.exe archivo.

A partir del Actualización de octubre de 2018 de Windows 10 (10.0; Compilación 17763), BITS usa el mismo orden de proxy que WinHttp con AUTOMATIC_PROXY. BITS usa esta ordenación más compatible cuando BG_JOB_PROXY_USAGE_PRECONFIG especifica. BG_JOB_PROXY_USAGE_PRECONFIG es el valor predeterminado para especificar el proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Especificación de la configuración específica del usuario para autenticar servidores proxy

Si usa BITS en un entorno que requiere autenticación de proxy mientras se ejecuta como una cuenta sin credenciales NTLM o Kerberos utilizables en el dominio de red del equipo, debe realizar pasos adicionales para autenticarse correctamente mediante las credenciales de otra cuenta de usuario que tenga credenciales en el dominio. Este es un escenario típico cuando el código BITS se ejecuta como un servicio del sistema como LocalService, NetworkService o LocalSystem, ya que esas cuentas no tienen credenciales NTLM o Kerberos utilizables.

Para más información sobre cómo funciona la autenticación en este escenario, consulte [Autenticación.](authentication.md)

## <a name="scalability"></a>Escalabilidad

Si hay más de 100 trabajos en la cola, el rendimiento puede empezar a disminuir en función de la composición del trabajo. BITS usa la [configuración de directiva MaxJobsPerMachine](group-policies.md) para imponer un límite máximo en el número de trabajos de la cola. Las aplicaciones deben limitar el número de sus trabajos a unos 10, de modo que varias aplicaciones tengan menos posibilidades de superar la guía de 100 trabajos. Normalmente, una aplicación con un gran número de trabajos para enviar primero enviaría 10 trabajos y, a continuación, enviaría uno a la vez a medida que finaliza cada trabajo.

El número de archivos del trabajo también debe limitarse a un máximo de 10 archivos. Si desea transferir un gran número de archivos para un trabajo, considere la posibilidad de crear un archivo CAB que contenga todos los archivos en su lugar.

## <a name="http-headers-can-be-in-any-case"></a>Los encabezados HTTP pueden ser en cualquier caso

Los estándares HTTP siempre han dicho que los encabezados HTTP deben tratarse como sin mayúsculas de minúsculas (sección 3.2 de RFC 7230). El estándar HTTP más reciente, RFC 7540, va más allá y dice que el tráfico HTTP/2 debe comparar los encabezados como sin mayúsculas de minúsculas y debe presentar encabezados en minúsculas (RFC 6540, sección 8.1.2). Incluso cuando el tráfico se envía con encabezados que no están en minúsculas, los servidores proxy pueden optar por forzar los encabezados a minúsculas.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitar información de identificación personal (PII)

Los trabajos de BITS, incluidos el nombre para mostrar del trabajo y la descripción y los nombres de archivo, son visibles para todos los usuarios con privilegios de administrador. También se pueden agregar a Windows telemetría. Debe evitar colocar datos confidenciales (como el nombre del usuario) en los detalles del trabajo.
