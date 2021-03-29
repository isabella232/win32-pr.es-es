---
title: Prácticas recomendadas al usar BITS
description: Esta sección contiene información que debe tener en cuenta al diseñar una aplicación que usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993997"
---
# <a name="best-practices-when-using-bits"></a>Prácticas recomendadas al usar BITS

Esta sección contiene información que debe tener en cuenta al diseñar una aplicación que usa BITS.

## <a name="user-context-or-service-context"></a>Contexto de usuario o de servicio

BITS transfiere archivos solo cuando el propietario del trabajo inicia sesión en el equipo (el usuario debe haber iniciado sesión de forma interactiva). BITS no admite el comando **runas** . Para obtener más información, consulte [usuarios y conexiones de red](users-and-network-connections.md).

Si no necesita el contexto de un usuario para su aplicación, considere la posibilidad de escribir en su lugar un servicio que se ejecute como LocalSystem, LocalService o NetworkService. Estas cuentas del sistema siempre inician sesión, por lo que la transferencia no está sujeta a un cierre de sesión del usuario. Sin embargo, si suplanta a un usuario al crear el trabajo, se aplican las reglas de inicio de sesión interactivo. Para obtener más información, consulte [cuentas de servicio y bits](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>Los trabajos son persistentes

Los trabajos permanecen en la cola hasta que se llama al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o [**IBackgroundCopyJob:: CANCEL**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . Los archivos del trabajo no están disponibles para el usuario hasta que se llama a **Complete**. Normalmente, se llama a **Complete** cuando el estado del trabajo es **\_ \_ \_ transferencia de estado del trabajo de BG** y se llama a **Cancel** cuando el trabajo se encuentra en estado de **trabajo de BG \_ \_ \_ \_ error transitorio** o estado de **\_ \_ \_ error de estado de trabajo de BG** y ya no puede progresar.

Si no llama al método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) o al método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) en 90 días (el valor predeterminado [valor jobinactivitytimeout](group-policies.md) Directiva de grupo), el servicio cancela el trabajo. Siempre debe llamar al método **Complete** o **Cancel** y no confiar en la Directiva valor jobinactivitytimeout para limpiar los trabajos. Los trabajos que quedan en la cola pueden impedir que los usuarios creen otros trabajos si se alcanza el límite de la Directiva MaxJobsPerUser o MaxJobsPerMachine.

## <a name="when-to-use-foreground-or-background-priority"></a>Cuándo usar la prioridad de primer o segundo plano

A menos que el trabajo sea crítico para el tiempo o el usuario esté esperando de forma activa, siempre debe usar una prioridad de fondo. Sin embargo, hay ocasiones en las que puede que desee cambiar de la prioridad de fondo a la prioridad de primer plano, por ejemplo, cuando el proxy o el servidor no admiten el encabezado Content-Range, o el software antivirus en el cliente quita la solicitud de encabezado de intervalo. Cambiar a la prioridad de primer plano solo funciona con los archivos cuyo tamaño de archivo sea inferior a 2 GB. Para obtener un ejemplo, vea la implementación de para el método [**IBackgroundCopyCallback:: JobError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . Tenga en cuenta también que si el trabajo en primer plano se interrumpe debido a una desconexión de la red o el usuario cierra la sesión, el trabajo producirá un error porque BITS enviará una solicitud de intervalo para intentar reiniciar la transferencia desde donde se quedó.

A partir de Windows 8, debe configurar los trabajos de descarga con el **\_ \_ \_ \_ contenido dinámico** de la propiedad de trabajo de bits y la prioridad del trabajo de BG en **\_ \_ \_ primer plano** cuando los servidores de destino no cumplen los [requisitos de http para las descargas de bits](http-requirements-for-bits-downloads.md). Tenga en cuenta que esto hará que BITS tenga que reiniciar la descarga desde el principio si alguna vez se interrumpe (por ejemplo, debido a problemas de conectividad o al reinicio del sistema).

Para obtener información sobre las prioridades disponibles y el modo en que BITS usa el nivel de prioridad para programar trabajos, vea [**BG \_ Job \_ Priority**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Errores transitorios y graves

Algunos errores son recuperables y otros no. Por ejemplo, el error "el servidor no está disponible" es un error recuperable y el error "acceso denegado" es un error irrecuperable. BITS coloca errores recuperables en un estado de error transitorio y vuelve a intentar el trabajo después de un intervalo especificado. Si el trabajo no puede realizar el progreso, BITS mueve el trabajo a un estado de error irrecuperable. Use los métodos [**IBackgroundCopyJob:: SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) y [**IBackgroundCopyJob:: SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar el modo en que bits procesa los errores transitorios.

En el caso de los trabajos en primer plano, debe limitar la cantidad de tiempo que deja que un trabajo permanezca en el estado de error transitorio e intente realizar la recuperación. Use el método [**SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para limitar la cantidad de tiempo que un trabajo permanece en el estado de error transitorio o para forzar el trabajo en el estado de error irrecuperable. Si permite que el trabajo intente la recuperación, debe usar el método [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) para establecer el intervalo mínimo de reintentos en 60 segundos o llamar al método [**IBackgroundCopyJob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para activar el trabajo de nuevo.

Para obtener más información, [**consulte \_ \_ Estado del trabajo de BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [ciclo de vida de un trabajo de bits](life-cycle-of-a-bits-job.md)y [control de errores](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Medición del uso del ancho de banda de red

BITS podría usar el adaptador de red del cliente para estimar el ancho de banda de red disponible. Dado que BITS no puede medir el ancho de banda más allá del cliente, BITS puede congestionar el vínculo WAN. Para reducir la congestión en el vínculo WAN, puede usar la Directiva de grupo **MaxInternetBandwidth** para limitar la cantidad de ancho de banda que usa el cliente. Para obtener más información, vea [ancho de banda de red](network-bandwidth.md) y directivas de [Grupo](group-policies.md).

Si está escribiendo una aplicación que muchos clientes usarán para descargar archivos de un servidor determinado, debe considerar un esquema que escalona las solicitudes de descarga para no sobrecargar el servidor con las solicitudes.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Establecimiento de credenciales para la autenticación de servidor y proxy

Si espera que el proxy o el servidor requieran credenciales de usuario, debe proporcionar las credenciales a BITS. Para especificar las credenciales, llame al método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . BITS admite esquemas de autenticación Basic, Digest, Negotiate, NTLM y Passport.

Para obtener más información sobre la autenticación, vea [autenticación](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Especificación de la configuración de proxy para cuentas de usuario y cuentas de servicio

De forma predeterminada, BITS usa la configuración de proxy de Internet Explorer del usuario. Para invalidar la configuración de proxy de Internet Explorer del usuario, llame al método [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) .

La configuración de proxy de Internet Explorer no se aplica a las cuentas del sistema, por lo que el comportamiento del proxy predeterminado (**\_ \_ \_ \_ preconfiguración de uso del proxy de trabajo de BG**) solo funcionará correctamente en las implementaciones del Protocolo de detección automática de proxy web (WPAD), a menos que se lleven a cabo pasos de configuración adicionales. Si la aplicación es un servicio que se ejecuta como LocalSystem, LocalService o NetworkService, considere la posibilidad de configurar un token auxiliar en los trabajos de BITS o establecer explícitamente la configuración de proxy correcta mediante una llamada a [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con la **\_ \_ \_ \_ invalidación del uso del proxy del trabajo de BG**. Como alternativa, puede usar los modificadores de **/util/SetIEProxy** de BitsAdmin.exe para establecer la configuración de proxy de Internet Explorer para la cuenta de sistema LocalSystem, LocalService o NetworkService. Para obtener más información, consulte la [herramienta BitsAdmin](bitsadmin-tool.md).

BITS no reconoce la configuración de proxy que se establece mediante el archivo de Proxycfg.exe.

A partir de la actualización 2018 de octubre de Windows 10 (10,0; Compilación 17763), BITS usa el mismo orden de proxy que usa WinHttp con AUTOMATIC_PROXY. BITS usa este orden más compatible cuando se especifica BG_JOB_PROXY_USAGE_PRECONFIG. BG_JOB_PROXY_USAGE_PRECONFIG es el valor predeterminado para especificar el proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Especificar la configuración específica del usuario para autenticar servidores proxy

Si usa BITS en un entorno que requiere autenticación de proxy mientras se ejecuta como una cuenta sin credenciales NTLM o Kerberos que se pueden usar en el dominio de red del equipo, debe realizar pasos adicionales para autenticarse correctamente mediante el uso de las credenciales de otra cuenta de usuario que tenga credenciales en el dominio. Se trata de un escenario típico en el que el código BITS se ejecuta como un servicio del sistema como LocalService, NetworkService o LocalSystem, ya que esas cuentas no tienen credenciales NTLM o Kerberos que se puedan usar.

Para obtener más información sobre cómo funciona la autenticación en este escenario, vea [autenticación.](authentication.md)

## <a name="scalability"></a>Escalabilidad

Si hay más de 100 trabajos en la cola, el rendimiento puede empezar a disminuir en función de la composición del trabajo. BITS usa la configuración de directiva [MaxJobsPerMachine](group-policies.md) para imponer un límite máximo en el número de trabajos de la cola. Las aplicaciones deben limitar el número de trabajos a aproximadamente 10, de modo que varias aplicaciones tengan menos posibilidades de superar la directriz 100-Job. Normalmente, una aplicación con un gran número de trabajos que se van a enviar enviará primero 10 trabajos y, a continuación, enviará uno cada vez a medida que cada trabajo finalice.

El número de archivos del trabajo también debe estar limitado a un máximo de 10 archivos. Si desea transferir un gran número de archivos para un trabajo, considere la posibilidad de crear en su lugar un archivo. CAB que contenga todos los archivos.

## <a name="http-headers-can-be-in-any-case"></a>Los encabezados HTTP pueden estar en cualquier caso

Los estándares HTTP siempre han explicado que los encabezados HTTP deben tratarse sin distinción de mayúsculas y minúsculas (sección 3,2 de RFC 7230). El estándar HTTP más reciente, RFC 7540, va más allá y indica que el tráfico HTTP/2 debe comparar los encabezados sin distinguir entre mayúsculas y minúsculas, y debe presentar los encabezados en minúsculas (RFC 6540, sección 8.1.2). Incluso cuando el tráfico se envía con encabezados que no están en minúsculas, los proxies pueden optar por forzar los encabezados a minúsculas.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitar la información de identificación personal (PII)

Los trabajos de BITS que incluyen el nombre para mostrar del trabajo y la descripción y los nombres de archivo son visibles para todos los usuarios con privilegios de administrador. También se pueden agregar a la telemetría de Windows. Debe evitar incluir datos confidenciales (como el nombre del usuario) en los detalles del trabajo.
