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
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="81858-103">Funciones de AutoProxy de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="81858-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="81858-104">WinHTTP implementa el protocolo WPAD mediante la función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) junto con dos funciones de utilidad auxiliares, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="81858-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="81858-105">La compatibilidad con AutoProxy no se integra totalmente en la pila HTTP en WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="81858-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="81858-106">Antes de enviar una solicitud, la aplicación debe llamar a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para obtener el nombre de un servidor proxy y, a continuación, llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con el proxy de la **\_ opción \_ WinHTTP** para establecer la configuración del proxy en el identificador de solicitud de WinHTTP creado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="81858-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="81858-107">La función [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) puede ejecutar los tres pasos del protocolo WPAD descritos en la información general anterior: (1) detectar la dirección URL de PAC, (2) Descargar el archivo de script PAC, (3) ejecutar el código de script y devolver la configuración del proxy en una estructura de **\_ \_ información del proxy WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="81858-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="81858-108">Opcionalmente, si la aplicación conoce la dirección URL de PAC de antemano, puede especificarlo en **WinHttpGetProxyForUrl**.</span><span class="sxs-lookup"><span data-stu-id="81858-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="81858-109">En el siguiente código de ejemplo se usa el proxy de AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="81858-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="81858-110">Configura una solicitud HTTP GET creando primero los identificadores de solicitud y conexión de la sesión de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="81858-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="81858-111">La llamada a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) especifica el **tipo de acceso de WinHTTP \_ \_ \_ sin \_ proxy** para la configuración de proxy inicial, para indicar que las solicitudes se envían directamente al servidor de destino de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81858-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="81858-112">Mediante el uso de AutoProxy, establece la configuración del proxy directamente en el identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="81858-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


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



<span data-ttu-id="81858-113">En el código de ejemplo proporcionado, la llamada a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) indica a la función que detecte el archivo de configuración automática de proxy automáticamente especificando la marca de **\_ \_ \_ detección automática de AutoProxy WinHTTP** en la estructura de [**\_ \_ Opciones de AutoProxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) .</span><span class="sxs-lookup"><span data-stu-id="81858-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="81858-114">El uso de la marca detección **\_ automática de AutoProxy WinHTTP \_ \_** requiere que el código especifique una o ambas marcas de detección automática (**WinHTTP \_ auto \_ detect \_ Type \_ DHCP**, **WinHTTP \_ auto \_ detect \_ Type \_ DNS \_ A**).</span><span class="sxs-lookup"><span data-stu-id="81858-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="81858-115">En el código de ejemplo se usa la característica de detección automática de **WinHttpGetProxyForUrl** porque la dirección URL de PAC no se conoce de antemano.</span><span class="sxs-lookup"><span data-stu-id="81858-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="81858-116">Si no se puede ubicar una dirección URL de PAC en la red en este escenario, se produce un error en **WinHttpGetProxyForUrl** ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error Error de \_ \_ detección automática \_ de WinHTTP**).</span><span class="sxs-lookup"><span data-stu-id="81858-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="81858-117">Si la dirección URL de PAC se conoce por adelantado</span><span class="sxs-lookup"><span data-stu-id="81858-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="81858-118">Si la aplicación conoce la dirección URL de PAC, puede especificarla en la \_ estructura de opciones de AUTOPROXY WinHTTP \_ y configurar [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para omitir la fase de detección automática.</span><span class="sxs-lookup"><span data-stu-id="81858-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="81858-119">Por ejemplo, si un archivo PAC está disponible en la red local en la dirección URL, " https://InternalSite/proxy-config.pac ", la llamada a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) tendría el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="81858-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


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



<span data-ttu-id="81858-120">Si la estructura de [**\_ \_ Opciones de AutoProxy de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) especifica tanto la detección **\_ \_ automática \_** de WinHTTP AutoProxy como las marcas **\_ \_ \_ URL de configuración** de WinHTTP AutoProxy (y especifica marcas de detction automática y una dirección URL de configuración automática), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) primero intenta la detección automática y, a continuación, si la detección automática no encuentra una dirección URL de PAC, "recurre a la dirección URL de configuración automática proporcionada por</span><span class="sxs-lookup"><span data-stu-id="81858-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="81858-121">La función WinHttpDetectAutoProxyConfigUrl</span><span class="sxs-lookup"><span data-stu-id="81858-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="81858-122">La función [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa un subconjunto del protocolo WPAD: intenta detectar automáticamente la dirección URL del archivo de configuración automática del proxy, sin descargar o ejecutar el archivo PAC.</span><span class="sxs-lookup"><span data-stu-id="81858-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="81858-123">Esta función es útil en situaciones especiales en las que una aplicación cliente web debe controlar la descarga y ejecución del archivo PAC.</span><span class="sxs-lookup"><span data-stu-id="81858-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="81858-124">La función WinHttpGetIEProxyConfigForCurrentUser</span><span class="sxs-lookup"><span data-stu-id="81858-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="81858-125">La función [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) devuelve la configuración de proxy de Internet Explorer del usuario actual para la conexión de red activa actual, sin llamar a "WinInet.dll".</span><span class="sxs-lookup"><span data-stu-id="81858-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="81858-126">Esta función solo es útil cuando se llama dentro de un proceso que se ejecuta bajo una identidad de cuenta de usuario interactiva, ya que es probable que no haya disponible ninguna configuración de proxy de Internet Explorer en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="81858-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="81858-127">Por ejemplo, no sería útil llamar a esta función desde una DLL ISAPI que se ejecuta en el proceso del servicio IIS.</span><span class="sxs-lookup"><span data-stu-id="81858-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="81858-128">Para obtener más información y un escenario en el que una aplicación basada en WinHTTP usaría **WinHttpGetIEProxyConfigForCurrentUser**, consulte [detección sin un archivo de configuración automática](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="81858-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
