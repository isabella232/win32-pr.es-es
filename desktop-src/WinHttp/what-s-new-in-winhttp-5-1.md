---
description: En este tema se describen las diferencias más importantes entre la versión 5,1 y la versión 5,0 de WinHTTP.
ms.assetid: df3fcf27-3012-4818-b29c-b8a4dc409828
title: Novedades de WinHTTP 5,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909d5ae8fb1d169af01782d21d2ead56b25c940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715165"
---
# <a name="whats-new-in-winhttp-51"></a>Novedades de WinHTTP 5,1

En este tema se describen las diferencias más importantes entre la versión 5,1 y la versión 5,0 de WinHTTP. Muchas de estas diferencias requieren cambios en el código de las aplicaciones que migran de la versión 5,0 a la versión 5,1. Algunas de las características de la versión 5,1 solo están disponibles a partir de Windows Server 2003 y Windows XP con Service Pack 2 (SP2), especialmente las características relacionadas con la mejora de la seguridad del cliente frente a los servidores Web malintencionados.

> [!IMPORTANT]
> Con el lanzamiento de la versión 5,1 de WinHTTP, la descarga de WinHTTP 5,0 ya no está disponible. A partir del 1 de octubre de 2004, Microsoft ha quitado la descarga del SDK de WinHTTP 5,0 de MSDN y ha finalizado el soporte técnico para la versión 5,0.

 

## <a name="dll-name-change"></a>Cambio de nombre de DLL

Se Winhttp.dll el nombre del nuevo archivo DLL de WinHTTP 5,1, mientras que el nombre de la DLL de WinHTTP 5,0 es Winhttp5.dll.

WinHTTP 5,0 y 5,1 pueden coexistir en el mismo sistema. WinHTTP 5,1 no reemplaza ni se instala en WinHTTP 5,0.

## <a name="redistribution"></a>Redistribución

WinHTTP 5,1 solo está disponible con Windows Server 2003, Windows 2000 Professional con Service Pack 3 (SP3), Windows XP con Service Pack 1 (SP1) y sistemas operativos posteriores. Un archivo de módulo de combinación redistribuible (. MSM) no está disponible para WinHTTP 5,1.

## <a name="winhttprequest-progid"></a>WinHttpRequest ProgID

El ProgID del componente WinHttpRequest ha cambiado de "WinHttp. WinHttpRequest. 5" a "WinHttp. WinHttpRequest. 5.1". El CLSID de la clase [**WinHttpRequest**](winhttprequest.md) también ha cambiado.

## <a name="async-callback-behavior-change"></a>Cambio de comportamiento de devolución de llamada asincrónica

Cuando llame a las funciones [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) y [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) en modo asincrónico, no se base en los parámetros de salida *lpdwNumberOfBytesWritten*, *lpdwNumberOfBytesAvailable* y *lpdwNumberOfBytesRead* respectivos que se van a establecer. Si la llamada de función se completa de forma asincrónica, WinHTTP no escribe en estos punteros proporcionados por el código de aplicación. En su lugar, la aplicación debe recuperar estos valores con los parámetros *lpvStatusInformation* y *dwStatusInformationLength* en la función de devolución de llamada.

## <a name="changes-to-default-settings"></a>Cambios en la configuración predeterminada

Los cambios en la configuración predeterminada incluyen:

-   La comprobación de certificados de servidor SSL está habilitada de forma predeterminada en WinHTTP 5,1. WinHTTP 5,0 no controla los errores que se producen al validar el certificado de servidor como errores irrecuperables. se notifican a la aplicación mediante una notificación de devolución de llamada de **\_ error segura** , pero no hace que se anule la solicitud. WinHTTP 5,1, como alternativa, controla los errores de validación de certificados de servidor como errores irrecuperables que anulan la solicitud. La aplicación puede indicar a WinHTTP que omita un pequeño subconjunto de errores de certificado, como una CA desconocida, una fecha de certificado no válida o expirada o un nombre de sujeto de certificado no válido, con la opción WinHTTP opciones de **\_ \_ \_ marcas de seguridad** .
-   La compatibilidad con la autenticación de Passport está deshabilitada de forma predeterminada en WinHTTP 5,1. La compatibilidad con Passport se puede habilitar con la opción **WinHTTP \_ configurar la \_ \_ \_ autenticación de Passport** . La búsqueda automática de credenciales de Passport en el registro de claves también está deshabilitada de forma predeterminada.
-   Cambio de comportamiento de redireccionamiento: los redireccionamientos HTTP a partir de una dirección URL segura **https:** a una dirección URL **http:** , ya no se siguen automáticamente de forma predeterminada por motivos de seguridad. Existe una nueva opción, **\_ \_ \_ Directiva de redirección de la opción WinHTTP**, para invalidar el comportamiento de redireccionamiento predeterminado en WinHTTP 5,1. Con el componente com **WinHttpRequest** , use la opción New **WinHttpRequestOption \_ EnableHttpsToHttpRedirects** para habilitar las redirecciones de https: a http: URL.
-   Cuando se crea un archivo de seguimiento de WinHTTP, el acceso se restringe con una ACL para que solo los administradores puedan leer o escribir el archivo. La cuenta de usuario con la que se creó el objeto de escritura también puede modificar la ACL para conceder acceso a otros usuarios. Esta protección solo está disponible en los sistemas de archivos que admiten la seguridad. es decir, NTFS, no FAT32).
-   A partir de Windows Server 2003 y Windows XP con SP2, el envío de solicitudes a los siguientes puertos conocidos, que no son HTTP, está restringido por razones de seguridad: 21 (FTP), 25 (SMTP), 70 (GOPHER), 110 (POP3), 119 (NNTP), 143 (IMAP).
-   A partir de Windows Server 2003 y Windows XP con SP2, la cantidad máxima de datos de encabezado que WinHTTP acepta en una respuesta HTTP es de 64 KB, de forma predeterminada. Si la respuesta HTTP del servidor contiene más de 64 KB de datos de encabezado totales, WinHTTP no podrá realizar la solicitud con un **error WinHTTP error de \_ \_ \_ \_ respuesta del servidor** . Este límite de 64 k se puede invalidar con la nueva opción de **WinHTTP \_ \_ Max \_ Response \_ \_ size** .

## <a name="ipv6-support"></a>Compatibilidad con IPv6

WinHTTP 5,1 agrega compatibilidad con el protocolo de Internet versión 6 (IPv6). WinHTTP puede enviar solicitudes HTTP a un servidor cuyo nombre DNS se resuelve en una dirección IPv6, y a partir de Windows Server 2003 y Windows XP con SP2, WinHTTP también admite direcciones literales IPv6.

## <a name="new-options-in-the-cc-api-for-winhttp"></a>Nuevas opciones de la API de C/C++ para WinHTTP

WinHTTP 5,1 implementa las siguientes opciones nuevas:

<dl> " \# definir la \_ opción de WinHTTP inicio de sesión de \_ Passport \_ \_ 86"  
" \# definir la \_ opción de WinHTTP \_ \_ dirección URL de retorno de Passport \_ 87"  
" \# definir la \_ Directiva de redirección de la opción de WinHTTP \_ \_ 88"  
</dl>

A partir de Windows Server 2003 y Windows XP con SP2, WinHTTP 5,1 implementa las siguientes opciones nuevas. En Windows 2000 Professional con SP3 o Windows XP con SP1, sin embargo, se produce un error en las llamadas a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) o [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) con estos identificadores de opción:

<dl> " \# definir el tiempo de espera de respuesta de recepción de la opción de WinHTTP \_ \_ \_ \_ 7"  
" \# definir la \_ opción de WinHTTP \_ Max \_ HTTP \_ Automatic \_ redirecciones 89"  
" \# definir la \_ opción WinHTTP \_ Max \_ HTTP \_ status \_ continue 90"  
" \# definir \_ el tamaño máximo del encabezado de respuesta de la opción WinHTTP \_ \_ \_ \_ 91"  
" \# definir la \_ opción de WinHTTP \_ Max \_ response \_ \_ size size 92"  
</dl>

## <a name="new-options-in-the-winhttprequest-51-component"></a>Nuevas opciones en el componente WinHttpRequest 5,1

El componente WinHttpRequest 5,1 implementa las siguientes opciones nuevas:

<dl> "WinHttpRequestOption \_ RevertImpersonationOverSsl"  
"WinHttpRequestOption \_ EnableHttpsToHttpRedirects"  
"WinHttpRequestOption \_ EnablePassportAuthentication"  
</dl>

Las siguientes opciones nuevas de WinHttpRequest 5,1 están disponibles a partir de Windows Server 2003 y Windows XP con SP2:

<dl> "WinHttpRequestOption \_ MaxAutomaticRedirects"  
"WinHttpRequestOption \_ MaxResponseHeaderSize"  
"WinHttpRequestOption \_ MaxResponseDrainSize"  
"WinHttpRequestOptions \_ EnableHttp1 \_ 1"  
</dl>

## <a name="proxies-are-not-trusted-when-auto-logon-security-is-set-to-high"></a>Los servidores proxy no son de confianza cuando la seguridad de inicio de sesión automático está establecida en alta

En WinHTTP 5,0, los servidores proxy siempre son de confianza para el inicio de sesión automático. Esto ya no es válido para WinHTTP 5,1 que se ejecuta en Windows Server 2003 y Windows XP con SP2 cuando se establece la opción de directiva **\_ \_ \_ \_ alta de seguridad de inicio de sesión automático de WinHTTP** .

## <a name="web-proxy-auto-discovery-autoproxy-api"></a>API de detección automática de proxy web (AutoProxy)

Para facilitar la configuración de los valores de proxy para las aplicaciones basadas en WinHTTP, WinHTTP ahora implementa el protocolo de detección automática de proxy web (WPAD), también denominado *AutoProxy*. Es el mismo protocolo que los exploradores Web, como Internet Explorer, implementan para detectar la configuración de proxy automáticamente sin necesidad de que un usuario final especifique un servidor proxy manualmente. Para admitir el AutoProxy, WinHTTP 5,1 implementa una nueva función de C/C++, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), además de dos funciones auxiliares, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

## <a name="known-issues"></a>Problemas conocidos

Se sabe que existen los siguientes problemas en WinHTTP 5,1 en Windows 2000 Professional con SP3 y Windows XP con SP1. Estos problemas se resuelven para WinHTTP a partir de Windows Server 2003 y Windows XP con SP2:

-   Si la aplicación usa la función [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) o el método [**SetTimeouts**](iwinhttprequest-settimeouts.md) en el componente [**WinHttpRequest**](iwinhttprequest-interface.md) para establecer un tiempo de espera de resolución DNS no infinito, como el parámetro *dwResolveTimeout* , se produce una pérdida de identificador de subproceso cada vez que WinHTTP resuelve un nombre DNS. A través de un gran número de solicitudes HTTP, esto provoca una pérdida de memoria considerable. La solución alternativa es dejar sin cambios la configuración de tiempo de espera de resolución infinita predeterminada (un valor de 0 especifica un tiempo de espera infinito). Esto es muy recomendable en cualquier caso, ya que la compatibilidad con los tiempos de espera de las resoluciones de nombres DNS en WinHTTP es costosa en términos de rendimiento. En Windows 2000 y versiones posteriores, el establecimiento de un tiempo de espera de resolución de DNS en WinHTTP no es necesario, ya que el servicio cliente DNS subyacente implementa su propio tiempo de espera de resolución.
-   Al procesar las solicitudes asincrónicas, WinHTTP no controla la suplantación de subprocesos correctamente. Esto hace que se produzca un error en las solicitudes que requieren autenticación NTLM/Negotiate, a menos que se proporcionen explícitamente las credenciales mediante las funciones [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) .

 

 



