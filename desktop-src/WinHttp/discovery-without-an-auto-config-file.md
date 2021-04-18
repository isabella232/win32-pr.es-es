---
description: Si no se ha implementado un archivo de configuración automática de proxy en la red local, WinHttpGetProxyForUrl no puede encontrar un servidor proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Detección sin un archivo de configuración automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5ec281c2ef74e2a377cecbd30f16cbc49bd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717296"
---
# <a name="discovery-without-an-auto-config-file"></a>Detección sin un archivo de configuración automática

Si no se ha implementado un archivo de configuración automática de proxy en la red local, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) no puede encontrar un servidor proxy. Si se produce un error en **WinHttpGetProxyForUrl** , hay varias estrategias de reversión posibles para obtener una configuración de proxy viable, en función de su entorno de tiempo de ejecución. Se incluye la solicitud de la configuración de proxy a través de una interfaz de usuario, que requiere que alguien almacene la configuración del proxy en el registro mediante la utilidad WinHTTP "ProxyCfg.exe" o el uso de [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para comprobar si un servidor proxy aparece en la configuración de Internet Explorer.

Es posible que no haya ningún archivo de configuración automática de proxy porque el cliente tiene una conexión directa a Internet, como a través de un ISP, y no necesita un servidor proxy.

Por otro lado, es posible que se requiera un servidor proxy, pero es posible que la red local no admita WPAD. En este caso, la configuración de proxy debe obtenerse del usuario o encontrarse en algún lugar del equipo cliente.

Una aplicación basada en WinHTTP que se ejecuta en un entorno de servidor de nivel intermedio, como una aplicación COM+ o ASP, debe depender de que un administrador del servidor establezca una configuración de proxy predeterminada en el registro mediante la utilidad "ProxyCfg.exe". Esta información de configuración predeterminada se puede recuperar mediante la función [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) o simplemente especificando la marca de **\_ \_ \_ preconfiguración de tipo de acceso de WinHTTP** en la llamada a [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) .

Por otro lado, una aplicación WinHTTP que se ejecuta en un equipo de escritorio cliente puede intentar examinar la configuración de proxy de Internet Explorer. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) rellena una estructura de configuración del proxy de [**\_ IE del \_ usuario \_ \_ \_ actual de WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) proporcionada por el llamador con la configuración de proxy de Internet Explorer del usuario actual para la conexión activa actual (acceso telefónico, VPN o LAN). Esta configuración puede indicar que se usa la detección automática, o puede especificar una dirección URL para un archivo de configuración automática de proxy, o puede especificar un servidor proxy real para su uso, o puede especificar una combinación de los tres. Si esta información incluye una dirección URL de PAC o un servidor proxy, la aplicación WinHTTP puede intentar utilizarlos.

Un ejemplo que usa las funciones [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) se puede encontrar en los ejemplos de WinHTTP del kit de desarrollo de software (SDK) de la plataforma.

 

 



