---
description: WinHTTP implementa el protocolo WPAD mediante la función WinHttpGetProxyForUrl junto con dos funciones de utilidad auxiliares, WinHttpDetectAutoProxyConfigUrl y WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funciones de AutoProxy de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001153"
---
# <a name="winhttp-autoproxy-functions"></a>Funciones de AutoProxy de WinHTTP

WinHTTP implementa el protocolo WPAD mediante la función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) junto con dos funciones de utilidad auxiliares, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

La compatibilidad con AutoProxy no se integra totalmente en la pila HTTP en WinHTTP. Antes de enviar una solicitud, la aplicación debe llamar a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para obtener el nombre de un servidor proxy y, a continuación, llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con el proxy de la **\_ opción \_ WinHTTP** para establecer la configuración del proxy en el identificador de solicitud de WinHTTP creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

La función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) puede ejecutar los tres pasos del protocolo WPAD descritos en la información general anterior: (1) detectar la dirección URL de PAC, (2) Descargar el archivo de script PAC, (3) ejecutar el código de script y devolver la configuración del proxy en una estructura de **\_ \_ información del proxy WinHTTP** . Opcionalmente, si la aplicación conoce la dirección URL de PAC de antemano, puede especificarlo en **WinHttpGetProxyForUrl**.

En el siguiente código de ejemplo se usa el proxy de AutoProxy. Configura una solicitud HTTP GET creando primero los identificadores de solicitud y conexión de la sesión de WinHTTP. La llamada a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) especifica el **tipo de acceso de WinHTTP \_ \_ \_ sin \_ proxy** para la configuración de proxy inicial, para indicar que las solicitudes se envían directamente al servidor de destino de forma predeterminada. Mediante el uso de AutoProxy, establece la configuración del proxy directamente en el identificador de solicitud.


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



En el código de ejemplo proporcionado, la llamada a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica a la función que detecte el archivo de configuración automática de proxy automáticamente especificando la marca de **\_ \_ \_ detección automática de AutoProxy WinHTTP** en la estructura de [**\_ \_ Opciones de AutoProxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) . El uso de la marca detección **\_ automática de AutoProxy WinHTTP \_ \_** requiere que el código especifique una o ambas marcas de detección automática (**WinHTTP \_ auto \_ detect \_ Type \_ DHCP**, **WinHTTP \_ auto \_ detect \_ Type \_ DNS \_ A**). En el código de ejemplo se usa la característica de detección automática de **WinHttpGetProxyForUrl** porque la dirección URL de PAC no se conoce de antemano. Si no se puede ubicar una dirección URL de PAC en la red en este escenario, se produce un error en **WinHttpGetProxyForUrl** ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error Error de \_ \_ detección automática \_ de WinHTTP**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Si la dirección URL de PAC se conoce por adelantado

Si la aplicación conoce la dirección URL de PAC, puede especificarla en la \_ estructura de opciones de AUTOPROXY WinHTTP \_ y configurar [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para omitir la fase de detección automática.

Por ejemplo, si un archivo PAC está disponible en la red local en la dirección URL, " https://InternalSite/proxy-config.pac ", la llamada a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tendría el siguiente aspecto.


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



Si la estructura de [**\_ \_ Opciones de AutoProxy de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) especifica tanto la detección **\_ \_ automática \_** de WinHTTP AutoProxy como las marcas **\_ \_ \_ URL de configuración** de WinHTTP AutoProxy (y especifica marcas de detction automática y una dirección URL de configuración automática), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) primero intenta la detección automática y, a continuación, si la detección automática no encuentra una dirección URL de PAC, "recurre a la dirección URL de configuración automática proporcionada por

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>La función WinHttpDetectAutoProxyConfigUrl

La función [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subconjunto del protocolo WPAD: intenta detectar automáticamente la dirección URL del archivo de configuración automática del proxy, sin descargar o ejecutar el archivo PAC. Esta función es útil en situaciones especiales en las que una aplicación cliente web debe controlar la descarga y ejecución del archivo PAC.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>La función WinHttpGetIEProxyConfigForCurrentUser

La función [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) devuelve la configuración de proxy de Internet Explorer del usuario actual para la conexión de red activa actual, sin llamar a "WinInet.dll". Esta función solo es útil cuando se llama dentro de un proceso que se ejecuta bajo una identidad de cuenta de usuario interactiva, ya que es probable que no haya disponible ninguna configuración de proxy de Internet Explorer en caso contrario. Por ejemplo, no sería útil llamar a esta función desde una DLL ISAPI que se ejecuta en el proceso del servicio IIS. Para obtener más información y un escenario en el que una aplicación basada en WinHTTP usaría **WinHttpGetIEProxyConfigForCurrentUser**, consulte [detección sin un archivo de configuración automática](discovery-without-an-auto-config-file.md).

 

 
