---
description: Es posible que las aplicaciones que portan desde WinINet a WinHTTP deban usar la misma configuración de AutoProxy que pueden recuperar en WinINet o Internet Explorer (IE).
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Establecer configuraciones de proxy WinINet en WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003012"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Establecer configuraciones de proxy WinINet en WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Configuración de proxy automático en WinHTTP 5,1

Es posible que las aplicaciones que portan desde WinINet a WinHTTP deban usar la misma configuración de AutoProxy que pueden recuperar en WinINet o Internet Explorer (IE). La API de la versión 5,1 de WinHTTP puede recuperar y usar esta configuración de proxy. En general, WinHTTP especifica el proxy y los servidores de derivación de proxy por sesión cuando se crea la sesión. Esta configuración se puede invalidar en función de cada solicitud.

Para usar la misma configuración de proxy que WinINet o IE, el cliente WinHTTP debe establecer la configuración de proxy para la sesión. Además, si IE o WinINet están configurados para usar la detección automática de proxy web (WPAD), el cliente de WinHTTP que utiliza esa configuración debe establecer la configuración de proxy por solicitud. En las secciones siguientes se describe cómo especificar la configuración de proxy para una sesión y una solicitud:

-   [Establecimiento de la configuración de proxy en una sesión](#setting-the-proxy-configuration-on-a-session)
-   [Establecimiento de la configuración de proxy en una única solicitud](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Establecimiento de la configuración de proxy en una sesión

## <a name="the-application-is-running-on-a-user-account"></a>La aplicación se ejecuta en una cuenta de usuario

Antes de crear una sesión, la aplicación llama a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para obtener la configuración del proxy de Internet Explorer. La aplicación debe ejecutarse como una cuenta de usuario para obtener esta configuración. El *parámetro pProxyConfig* es un puntero a una estructura de configuración del [**\_ proxy de \_ IE del usuario \_ \_ \_ actual de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contiene los servidores de nombre de proxy (*lpszProxy*) y de omisión de proxy (*lpszProxyBypass*). El nombre del proxy y los valores de omisión del proxy de la estructura de **configuración del proxy de \_ \_ IE del usuario \_ \_ \_ actual** se utilizan para inicializar la sesión de winhttp. La sesión se inicializa llamando a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con los parámetros *pwszProxyName* y *PwszProxyBypass* obtenidos de los miembros **lpszProxy** y **lpszProxyBypass** de la estructura **de \_ \_ configuración del \_ \_ proxy de \_ IE del usuario actual de WinHTTP** .

## <a name="the-application-is-running-as-a-service"></a>La aplicación se ejecuta como un servicio

La aplicación debe asegurarse de que la configuración del registro para un usuario individual se carga en el registro antes de llamar a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). Si esta configuración no se carga en el registro, **WinHttpGetIEProxyConfigForCurrentUser** no puede obtener la configuración del proxy. La configuración del registro para un usuario individual se puede cargar en el registro mediante una llamada a la función **LoadUserProfile** . Si la carga de la configuración del registro del usuario no es una opción, la aplicación puede llamar a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) con el **\_ \_ \_ \_ proxy predeterminado de tipo de acceso de WinHTTP** especificado en el parámetro *dwAcessType* . Al especificar el proxy predeterminado en la llamada a **WinHttpOpen** se indica a la API de WinHTTP que recupere el conjunto de configuración de proxy mediante la utilidad WinHTTP [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) . Una vez cargados los valores del registro para un usuario individual, la aplicación sigue los pasos descritos en [la aplicación se está ejecutando en una cuenta de usuario](#the-application-is-running-on-a-user-account) para establecer el nombre del proxy y los servidores de omisión del proxy.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Establecimiento de la configuración de proxy en una única solicitud

Antes de crear la sesión, la aplicación llama a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para determinar si WinInet e IE están configurados para usar WPAD. **WinHttpGetIEProxyConfigForCurrentUser** devuelve la estructura de [**configuración del proxy de \_ \_ IE del usuario \_ \_ \_ actual de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) que contiene el miembro **fAutoDetect** . Un valor de **true** para este miembro indica que se utiliza wpad y el miembro **lpszAutoConfigUrl** contiene la dirección URL de WPAD.

## <a name="automatic-proxy-configuration-is-used"></a>Se usa la configuración automática del proxy

Si se usa WPAD, la aplicación llama a [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para recuperar el proxy de la solicitud. El parámetro *lpwszUrl* contiene la dirección URL a la que se envía la solicitud y el parámetro *pAutoProxyOptions* contiene un puntero a la estructura ([**\_ \_ Opciones de AutoProxy de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)) que contiene las opciones de AutoProxy. La aplicación inicializa la estructura **de \_ \_ Opciones de AutoProxy WinHTTP** con la configuración devuelta por la estructura de configuración del [**proxy de \_ \_ IE del usuario \_ \_ \_ actual de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) en la llamada a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). La marca de **\_ \_ \_ dirección URL** de configuración de proxy automático WinHTTP se especifica en el miembro **dwFlags** de la estructura de **Opciones de \_ AUTOPROXY \_ WinHTTP** y el miembro **lpszAutoconfigUrl** contiene la dirección URL de configuración automática de proxy de la estructura de configuración del proxy de **IE del \_ \_ usuario \_ \_ \_ actual** . La función **WinHttpGetProxyForUrl** devuelve el nombre del proxy y la lista de omisión de proxy en los miembros **lpszProxy** y **lpszProxyBypass** de la estructura de [**\_ \_ información del proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) .

Una vez que el proxy de la solicitud se obtiene de [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl), la aplicación crea la solicitud con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). A continuación, se llama a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para establecer el proxy para la solicitud mediante la especificación del identificador de solicitud en el parámetro *hInternet* . El parámetro *dwOption* de la llamada a **WinHttpSetOption** debe establecerse en el proxy de la **\_ opción \_ WinHTTP** y el parámetro *lpBuffer* es un puntero a una estructura de [**\_ \_ información del proxy WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene el proxy y la omisión del proxy que se usará para la solicitud.

## <a name="automatic-proxy-configuration-is-not-used"></a>No se utiliza la configuración automática del proxy

Si la llamada a [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) indica que no se utiliza AutoProxy, la aplicación puede simplemente crear la solicitud con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). La configuración del proxy es la misma para toda la sesión y no se necesitan cambios por solicitud.

 

 



