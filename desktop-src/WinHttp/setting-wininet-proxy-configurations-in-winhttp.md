---
description: Es posible que las aplicaciones que se porte desde WinINet a WinHTTP deba usar la misma configuración de proxy automático que pueden recuperar en WinINet o Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Establecimiento de configuraciones de proxy de WinINet en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476128"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Establecimiento de configuraciones de proxy de WinINet en WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Configuración del proxy automático en WinHTTP 5.1

Es posible que las aplicaciones que se porte desde WinINet a WinHTTP deba usar la misma configuración de proxy automático que pueden recuperar en WinINet o Internet Explorer (IE). La API WinHTTP versión 5.1 puede recuperar y usar esta configuración de proxy. En general, WinHTTP especifica los servidores de omisión de proxy y proxy por sesión cuando se crea la sesión. Esta configuración se puede invalidar por solicitud.

Para usar la misma configuración de proxy que WinINet o IE, el cliente WinHTTP debe establecer la configuración de proxy para la sesión. Además, si IE o WinINet están configurados para usar la detección automática de proxy web (WPAD), el cliente WinHTTP que usa esa configuración debe establecer la configuración del proxy por solicitud. En las secciones siguientes se describe cómo especificar la configuración de proxy para una sesión y una solicitud:

-   [Establecer la configuración de proxy en una sesión](#setting-the-proxy-configuration-on-a-session)
-   [Establecer la configuración del proxy en una única solicitud](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Establecer la configuración de proxy en una sesión

## <a name="the-application-is-running-on-a-user-account"></a>La aplicación se ejecuta en una cuenta de usuario

Antes de crear una sesión, la aplicación llama [**a WinHttpGetIEProxyConfigForCurrentUser para**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) obtener la configuración del proxy de IE. La aplicación debe ejecutarse como una cuenta de usuario para obtener esta configuración. El *parámetro pProxyConfig* es un puntero a una estructura DE CONFIGURACIÓN DE PROXY DE [**WINHTTP CURRENT USER \_ \_ \_ IE \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contiene los servidores de nombre de proxy *(lpszProxy)* y de omisión de proxy *(lpszProxyBypass).* A continuación, se usan los valores de nombre de proxy y omisión de proxy de la estructura DE CONFIGURACIÓN DE PROXY DE **WINHTTP \_ CURRENT USER \_ \_ IE \_ \_** para inicializar la sesión WinHTTP. La sesión se inicializa mediante una llamada [**a WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con los parámetros *pwszProxyName* y *pwszProxyBypass* obtenidos de los miembros **lpszProxy** y **lpszProxyBypass** de la estructura DE CONFIGURACIÓN DEL PROXY DE **\_ \_ \_ IE \_ \_** DE USUARIO ACTUAL DE WINHTTP.

## <a name="the-application-is-running-as-a-service"></a>La aplicación se ejecuta como servicio

La aplicación debe asegurarse de que la configuración del Registro de un usuario individual se carga en el registro antes de llamar a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Si esta configuración no se carga en el Registro, **WinHttpGetIEProxyConfigForCurrentUser** no puede obtener la configuración del proxy. La configuración del Registro para un usuario individual se puede cargar en el Registro mediante una llamada a la **función LoadUserProfile.** Si la carga de la configuración del Registro del usuario no es una opción, la aplicación puede llamar a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con el **\_ \_ \_ \_ PROXY** PREDETERMINADO de TIPO DE ACCESO WINHTTP especificado en el *parámetro dwAcessType.* Al especificar el proxy predeterminado en la llamada a **WinHttpOpen,** se indica a la API WinHTTP que recupere la configuración de proxy establecida mediante la utilidadproxycfg.exe [**WinHTTP.**](proxycfg-exe--a-proxy-configuration-tool.md) Una vez cargada la configuración del Registro para un usuario individual, la aplicación sigue los pasos descritos en La aplicación se ejecuta en una cuenta de usuario para establecer el nombre de proxy y los servidores de omisión de proxy. [](#the-application-is-running-on-a-user-account)

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Establecer la configuración del proxy en una única solicitud

Antes de crear la sesión, la aplicación llama a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para determinar si WinINet e IE están configurados para usar WPAD. **WinHttpGetIEProxyConfigForCurrentUser** devuelve la estructura DE CONFIGURACIÓN DEL PROXY DE [**\_ \_ \_ IE \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) DE USUARIO ACTUAL DE WINHTTP que contiene el **miembro fAutoDetect.** Un valor **TRUE para** este miembro indica que se usa WPAD y que el miembro **lpszAutoConfigUrl** contiene la dirección URL de WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>Se usa la configuración automática de proxy

Si se usa WPAD, la aplicación llama [**a WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para recuperar el proxy de la solicitud. El parámetro *lpwszUrl* contiene la dirección URL a la que se envía la solicitud y el parámetro *pAutoProxyOptions* contiene un puntero a la estructura (OPCIONES DE [**WINHTTP \_ AUTOPROXY) \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)que contiene las opciones de proxy automático. La aplicación inicializa la estructura **WINHTTP \_ AUTOPROXY \_ OPTIONS** con la configuración devuelta de la estructura DE CONFIGURACIÓN DEL PROXY DE [**\_ \_ \_ IE \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) DE USUARIO ACTUAL DE WINHTTP en la llamada a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). La marca DE URL de configuración de **WINHTTP \_ \_ \_ AUTOPROXY** se especifica en el miembro **dwFlags** de la estructura OPCIONES DE **WINHTTP \_ \_ AUTOPROXY** y el miembro **lpszAutoconfigUrl** contiene la dirección URL de configuración automática del proxy de la estructura DE CONFIGURACIÓN DEL PROXY DE **\_ \_ \_ IE \_ \_** DE USUARIO ACTUAL DE WINHTTP. La **función WinHttpGetProxyForUrl** devuelve el nombre del proxy y la lista de omisión del proxy en los miembros **lpszProxy** y **lpszProxyBypass** de la estructura INFO del [**\_ \_ proxy WINHTTP.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)

Una vez que el proxy de la solicitud se obtiene de [**WinHttpGetProxyForUrl,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)la aplicación crea la solicitud [**con WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). A continuación, se llama a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer el proxy de la solicitud especificando el identificador de solicitud en el *parámetro hInternet.* El *parámetro dwOption* de la llamada a **WinHttpSetOption** debe establecerse en **WINHTTP OPTION \_ \_ PROXY** y el parámetro *lpBuffer* es un puntero a una estructura INFO de [**\_ PROXY \_ WINHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene el proxy y la omisión del proxy que se usarán para la solicitud.

## <a name="automatic-proxy-configuration-is-not-used"></a>No se usa la configuración automática de proxy

Si la llamada a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indica que no se usa el proxy automático, la aplicación simplemente puede crear la solicitud [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) La configuración del proxy es la misma para toda la sesión y no se necesitan cambios por solicitud.

 

 



