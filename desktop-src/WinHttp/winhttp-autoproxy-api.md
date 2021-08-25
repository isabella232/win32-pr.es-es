---
description: WinHTTP implementa el protocolo WPAD mediante la función WinHttpGetProxyForUrl junto con dos funciones de utilidad auxiliares, WinHttpDetectAutoProxyConfigUrl y WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funciones de WinHTTP AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955715"
---
# <a name="winhttp-autoproxy-functions"></a>Funciones de WinHTTP AutoProxy

WinHTTP implementa el protocolo WPAD mediante la función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) junto con dos funciones de utilidad auxiliares, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) y [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)

La compatibilidad con AutoProxy no está totalmente integrada en la pila HTTP en WinHTTP. Antes de enviar una solicitud, la aplicación debe llamar a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para obtener el nombre de un servidor proxy y, a continuación, llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mediante **WINHTTP \_ OPTION \_ PROXY** para establecer la configuración del proxy en el identificador de solicitud WinHTTP creado [**por WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

La función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) puede ejecutar los tres pasos del protocolo WPAD descritos en la información general anterior: (1) detectar la dirección URL de PAC, (2) descargar el archivo de script PAC, (3) ejecutar el código de script y devolver la configuración del proxy en una estructura DE INFORMACIÓN de **\_ PROXY \_ WINHTTP.** Opcionalmente, si la aplicación conoce de antemano la dirección URL de PAC, puede especificarla en **WinHttpGetProxyForUrl.**

En el código de ejemplo siguiente se usa el proxy automático. Configura una solicitud HTTP GET creando primero la conexión de sesión WinHTTP y los identificadores de solicitud. La [**llamada WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) especifica **WINHTTP ACCESS TYPE NO \_ \_ \_ \_ PROXY** para la configuración de proxy inicial, para indicar que las solicitudes se envían directamente al servidor de destino de forma predeterminada. Con el proxy automático, establece la configuración del proxy directamente en el identificador de solicitud.


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



En el código de ejemplo proporcionado, la llamada a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica a la función que detecte automáticamente el archivo de configuración automática del proxy especificando la marca AUTO DETECT de **WINHTTP \_ AUTOPROXY \_ \_** en la estructura OPCIONES DE [**WINHTTP \_ AUTOPROXY. \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) El uso de la marca DETECCIÓN AUTOMÁTICA DE **WINHTTP \_ AUTOPROXY \_ \_** requiere que el código especifique una o ambas marcas de detección automática **(WINHTTP \_ AUTO DETECT TYPE \_ \_ \_ DHCP**, **WINHTTP AUTO DETECT TYPE DNS \_ \_ \_ \_ \_ A**). El código de ejemplo usa la característica de detección automática **de WinHttpGetProxyForUrl** porque la dirección URL de PAC no se conoce de antemano. Si no se puede encontrar una dirección URL de PAC en la red en este escenario, se produce un error **en WinHttpGetProxyForUrl** ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve **ERROR \_ WINHTTP \_ AUTODETECTION \_ FAILED**).

## <a name="if-the-pac-url-is-known-in-advance"></a>Si la dirección URL de PAC se conoce de antemano

Si la aplicación conoce la dirección URL de PAC, puede especificarla en la estructura WINHTTP AUTOPROXY OPTIONS y configurar \_ \_ [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para omitir la fase de detección automática.

Por ejemplo, si hay un archivo PAC disponible en la red local en la dirección URL, "", la llamada a https://InternalSite/proxy-config.pac [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tendría el siguiente aspecto.


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



Si la estructura OPCIONES DE [**WINHTTP \_ \_ AUTOPROXY**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) especifica las marcas **WINHTTP \_ AUTOPROXY \_ AUTO \_ DETECT** y **WINHTTP \_ AUTOPROXY CONFIG \_ \_ URL** (y especifica marcas de auto-detction y una dirección URL de configuración automática), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) intenta primero la detección automática y, a continuación, si la detección automática no encuentra una dirección URL de PAC, "vuelve" a la dirección URL de configuración automática proporcionada por la aplicación.

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>Función WinHttpDetectAutoProxyConfigUrl

La función [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subconjunto del protocolo WPAD: intenta detectar automáticamente la dirección URL del archivo de configuración automática del proxy, sin descargar ni ejecutar el archivo PAC. Esta función es útil en situaciones especiales en las que una aplicación cliente web debe controlar la descarga y ejecución del propio archivo PAC.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>Función WinHttpGetIEProxyConfigForCurrentUser

La [**función WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) devuelve la configuración actual del proxy Internet Explorer usuario para la conexión de red activa actual, sin llamar a "WinInet.dll". Esta función solo es útil cuando se llama dentro de un proceso que se ejecuta bajo una identidad de cuenta de usuario interactiva, porque es probable que no haya ninguna configuración de proxy Internet Explorer disponible de lo contrario. Por ejemplo, no sería útil llamar a esta función desde un archivo DLL de ISAPI que se ejecuta en el proceso del servicio IIS. Para obtener más información y un escenario en el que una aplicación basada en WinHTTP usaría **WinHttpGetIEProxyConfigForCurrentUser,** vea [Detección](discovery-without-an-auto-config-file.md)sin un archivo de configuración automática .

 

 
