---
description: En este tema se describen las diferencias más importantes entre la versión 5.1 de WinHTTP y la versión 5.0.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Novedades de WinHTTP 5.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d63be0990b26d45cccb9677afdc8fd9b50154eb7bb2b19c47c85d7374303efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955735"
---
# <a name="whats-new-in-winhttp-51"></a>Novedades de WinHTTP 5.1

En este tema se describen las diferencias más importantes entre la versión 5.1 de WinHTTP y la versión 5.0. Muchas de estas diferencias requieren cambios de código en las aplicaciones que migran de la versión 5.0 a la versión 5.1. Algunas de las características de la versión 5.1 solo están disponibles a partir de Windows Server 2003 y Windows XP con Service Pack 2 (SP2), especialmente características relacionadas con la mejora de la seguridad del cliente frente a servidores web malintencionados.

> [!IMPORTANT]
> Con la versión 5.1 de WinHTTP, la descarga de WinHTTP 5.0 ya no está disponible. A partir del 1 de octubre de 2004, Microsoft quitó la descarga del SDK de WinHTTP 5.0 de MSDN y finalizó el soporte técnico del producto para la versión 5.0.

 

## <a name="dll-name-change"></a>Cambio de nombre de DLL

El nombre del nuevo archivo DLL winHTTP 5.1 es Winhttp.dll, mientras que el nombre del archivo DLL WinHTTP 5.0 es Winhttp5.dll.

WinHTTP 5.0 y 5.1 pueden coexistir en el mismo sistema; WinHTTP 5.1 no reemplaza ni instala WinHTTP 5.0.

## <a name="redistribution"></a>Redistribución

WinHTTP 5.1 solo está disponible con Windows Server 2003, Windows 2000 Professional con Service Pack 3 (SP3), Windows XP con Service Pack 1 (SP1) y sistemas operativos posteriores. Un archivo de módulo de combinación redistribuible (.msm) no está disponible para WinHTTP 5.1.

## <a name="winhttprequest-progid"></a>WinHttpRequest ProgID

El ProgID del componente WinHttpRequest ha cambiado de "WinHttp.WinHttpRequest.5" a "WinHttp.WinHttpRequest.5.1". También ha cambiado el CLSID de la clase [**WinHttpRequest.**](winhttprequest.md)

## <a name="async-callback-behavior-change"></a>Cambio de comportamiento de devolución de llamada asincrónica

Al llamar a las funciones [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) y [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) en modo asincrónico, no se base en los parámetros *lpdwNumberOfBytesWritten*, *lpdwNumberOfBytesAvailable* y *lpdwNumberOfBytesRead* OUT que se establecerán. Si la llamada a la función se completa de forma asincrónica, WinHTTP no escribe en estos punteros proporcionados por el código de aplicación. En su lugar, la aplicación debe recuperar estos valores mediante los parámetros *lpvStatusInformation* y *dwStatusInformationLength* para la función de devolución de llamada.

## <a name="changes-to-default-settings"></a>Cambios en el valor predeterminado Configuración

Los cambios en la configuración predeterminada incluyen:

-   La comprobación del certificado de servidor SSL está habilitada de forma predeterminada en WinHTTP 5.1. WinHTTP 5.0 no controla los errores detectados al validar el certificado de servidor como errores irreales; Se notifican a la aplicación mediante una notificación de devolución de llamada **SECURE \_ FAILURE,** pero no hace que se anule la solicitud. WinHTTP 5.1, como alternativa, controla los errores de validación de certificados de servidor como errores irreales que anulan la solicitud. La aplicación puede indicar a WinHTTP que ignore un pequeño subconjunto de errores de certificado, como una entidad de certificación desconocida, una fecha de certificado no válida o expirada o un nombre de sujeto de certificado no válido, mediante la opción **WINHTTP \_ OPTION SECURITY \_ \_ FLAGS.**
-   La compatibilidad con la autenticación de Passport está deshabilitada de forma predeterminada en WinHTTP 5.1. La compatibilidad con Passport se puede habilitar con la opción WINHTTP OPTION CONFIGURE PASSPORT AUTH (CONFIGURAR **\_ \_ \_ \_ AUTENTICACIÓN DE PASSPORT).** La búsqueda automática de credenciales de Passport en keyring también está deshabilitada de forma predeterminada.
-   Cambio de comportamiento de redireccionamiento: las redirecciones HTTP desde una dirección URL **https:** segura a una dirección **URL http:** normal ya no se siguen automáticamente de forma predeterminada por motivos de seguridad. Hay una nueva opción, **WINHTTP \_ OPTION REDIRECT \_ \_ POLICY**, para invalidar el comportamiento de redireccionamiento predeterminado en WinHTTP 5.1. Con el componente COM **WinHttpRequest,** use la nueva **opción \_ EnableHttpsToHttpRedirects de WinHttpRequestOption** para habilitar las redirecciones de https: a http: DIRECCIONES URL.
-   Cuando se crea un archivo de seguimiento WinHTTP, el acceso está restringido con una ACL, de modo que solo los administradores puedan leer o escribir el archivo. La cuenta de usuario con la que se creó el archivo de seguimiento también puede modificar la ACL para conceder acceso a otros usuarios. Esta protección solo está disponible en sistemas de archivos que admiten seguridad; es decir, NTFS, no FAT32).
-   A partir de Windows Server 2003 y Windows XP con SP2, el envío de solicitudes a los siguientes puertos conocidos y no HTTP está restringido por motivos de seguridad: 21 (FTP), 25 (SMTP), 70 (GOPHER), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   A partir de Windows Server 2003 y Windows XP con SP2, la cantidad máxima de datos de encabezado que WinHTTP acepta en una respuesta HTTP es de 64 000, de forma predeterminada. Si la respuesta HTTP del servidor contiene más de 64 000 datos de encabezado total, WinHTTP produce un error DE RESPUESTA DEL SERVIDOR **\_ WINHTTP \_ \_ \_** NO VÁLIDO en la solicitud. Este límite de 64 000 se puede invalidar mediante la nueva opción **WINHTTP \_ OPTION MAX RESPONSE HEADER \_ \_ \_ \_ SIZE.**

## <a name="ipv6-support"></a>Compatibilidad con IPv6

WinHTTP 5.1 agrega compatibilidad con el protocolo de Internet versión 6 (IPv6). WinHTTP puede enviar solicitudes HTTP a un servidor cuyo nombre DNS se resuelve en una dirección IPv6 y, a partir de Windows Server 2003 y Windows XP con SP2, WinHTTP también admite direcciones literales IPv6.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Nuevas opciones en la API de C/C++ para WinHTTP

WinHTTP 5.1 implementa las siguientes opciones nuevas:

<dl> " \# define WINHTTP \_ OPTION PASSPORT SIGN OUT \_ \_ \_ 86"  
" \# define WINHTTP \_ OPTION PASSPORT RETURN URL \_ \_ \_ 87"  
" \# define WINHTTP \_ OPTION REDIRECT \_ POLICY \_ 88"  
</dl>

A partir de Windows Server 2003 y Windows XP con SP2, WinHTTP 5.1 implementa las siguientes opciones nuevas. En Windows 2000 Professional con SP3 o Windows XP con SP1, sin embargo, las llamadas a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) o [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con estos iDs de opción producirán un error:

<dl> " \# define WINHTTP \_ OPTION RECEIVE RESPONSE TIMEOUT \_ \_ \_ 7"  
" \# define WINHTTP \_ OPTION MAX HTTP AUTOMATIC \_ \_ \_ \_ REDIRECTS 89"  
" \# define WINHTTP \_ OPTION MAX HTTP STATUS CONTINUE \_ \_ \_ \_ 90"  
" \# define WINHTTP \_ OPTION MAX RESPONSE HEADER SIZE \_ \_ \_ \_ 91"  
" \# define WINHTTP \_ OPTION MAX RESPONSE DRAIN SIZE \_ \_ \_ \_ 92"  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Nuevas opciones en el componente WinHttpRequest 5.1

El componente WinHttpRequest 5.1 implementa las siguientes opciones nuevas:

<dl> "WinHttpRequestOption \_ RevertImpersonationOverSsl"  
"WinHttpRequestOption \_ EnableHttpsToHttpRedirects"  
"WinHttpRequestOption \_ EnablePassportAuthentication"  
</dl>

Las siguientes opciones nuevas de WinHttpRequest 5.1 están disponibles a partir de Windows Server 2003 y Windows XP con SP2:

<dl> "WinHttpRequestOption \_ MaxAutomaticRedirects"  
"WinHttpRequestOption \_ MaxResponseHeaderSize"  
"WinHttpRequestOption \_ MaxResponseDrainSize"  
"WinHttpRequestOptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>Los servidores proxy no son de confianza cuando la seguridad de inicio de sesión automático está establecida en Alta

En WinHTTP 5.0, los servidores proxy siempre son de confianza para el inicio de sesión automático. Esto ya no es válido para WinHTTP 5.1 que se ejecuta en Windows Server 2003 y Windows XP con SP2 cuando se establece la opción de directiva NIVEL DE SEGURIDAD ALTO de **WINHTTP \_ \_ \_ \_ AUTOLOGON.**

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API de detección automática de proxy web (AutoProxy)

Para facilitar la configuración de proxy para aplicaciones basadas en WinHTTP, WinHTTP implementa ahora el protocolo de detección automática de proxy web (WPAD), también conocido como *proxy automático.* Se trata del mismo protocolo que implementan los exploradores web, como Internet Explorer, para detectar automáticamente la configuración de proxy sin necesidad de que un usuario final especifique manualmente un servidor proxy. Para admitir el proxy automático, WinHTTP 5.1 implementa una nueva función de C/C++, [**WinHttpGetProxyForUrl,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)además de dos funciones auxiliares, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Problemas conocidos

Se sabe que existen los siguientes problemas en WinHTTP 5.1 en Windows 2000 Professional con SP3 y Windows XP con SP1. Estos problemas se resuelven para WinHTTP a partir de Windows Server 2003 y Windows XP con SP2:

-   Si la aplicación usa la función [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) o el método [**SetTimeouts**](iwinhttprequest-settimeouts.md) en el componente [**WinHttpRequest**](iwinhttprequest-interface.md) para establecer un tiempo de espera de resolución dns no infinito, como el parámetro *dwResolveTimeout,* se produce una pérdida de identificador de subproceso cada vez que WinHTTP resuelve un nombre DNS. A lo largo de un gran número de solicitudes HTTP, esto provoca una pérdida de memoria significativa. La solución alternativa es dejar sin modificar la configuración predeterminada de tiempo de espera de resolución infinita (un valor de 0 especifica un tiempo de espera infinito). Esto se recomienda encarecidamente en cualquier caso, ya que los tiempos de espera de compatibilidad en las resoluciones de nombres DNS en WinHTTP son caros en términos de rendimiento. Para Windows 2000 y versiones posteriores, no es necesario establecer un tiempo de espera de resolución dns en WinHTTP, ya que el servicio cliente DNS subyacente implementa su propio tiempo de espera de resolución.
-   Al procesar solicitudes asincrónicas, WinHTTP no controla correctamente la suplantación de subprocesos. Esto hace que se produce un error en las solicitudes que requieren la autenticación NTLM/Negotiate, a menos que las credenciales se indiquen explícitamente mediante las funciones [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)

 

 



