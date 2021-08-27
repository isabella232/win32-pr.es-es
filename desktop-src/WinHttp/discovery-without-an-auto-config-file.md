---
description: Si no se ha implementado un archivo de configuración automática de proxy en la red local, WinHttpGetProxyForUrl no puede encontrar un servidor proxy.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Detección sin un archivo de configuración automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553f4f798a821ff219b587c494d5dccfbba8c4b22efd0d1692ca2069f53041de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097945"
---
# <a name="discovery-without-an-auto-config-file"></a>Detección sin un archivo de configuración automática

Si no se ha implementado un archivo de configuración automática de proxy en la red local, [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) no puede encontrar un servidor proxy. Si se produce un error en **WinHttpGetProxyForUrl,** hay varias estrategias de resalte posibles para obtener una configuración de proxy viable, en función de su entorno de tiempo de ejecución. Estos incluyen solicitar la configuración de proxy a través de una interfaz de usuario, requerir que alguien almacene la configuración de proxy en el Registro mediante la utilidad "ProxyCfg.exe" de WinHTTP o usar [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) para comprobar si un servidor proxy aparece en la configuración de Internet Explorer.

Es posible que no haya ningún archivo de configuración automática de proxy porque el cliente tiene una conexión directa a Internet, como a través de un ISP, y no necesita un servidor proxy.

Por otro lado, puede ser necesario un servidor proxy, pero es posible que la red local no admita WPAD. En este caso, la configuración del proxy debe obtenerse del usuario o encontrarse en algún lugar del equipo cliente.

Una aplicación basada en WinHTTP que se ejecuta en un entorno de servidor de nivel intermedio, como una aplicación COM+ o ASP, debe basarse en un administrador del servidor que establece una configuración de proxy predeterminada en el Registro mediante la utilidad "ProxyCfg.exe". Esta información de configuración predeterminada se puede recuperar mediante la función [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) o simplemente especificando la marca **\_ \_ \_ PRECONFIG** DE TIPO DE ACCESO WINHTTP en la [**llamada WinHttpOpen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)

Por otro lado, una aplicación WinHTTP que se ejecuta en un equipo de escritorio cliente puede intentar examinar la configuración Internet Explorer proxy del cliente. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) rellena una estructura de CONFIGURACIÓN DE PROXY DE [**\_ \_ \_ IE \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) DE USUARIO ACTUAL de WINHTTP proporcionada por el autor de la llamada con la configuración de proxy de Internet Explorer del usuario actual para la conexión activa actual (acceso telefónico, VPN o LAN). Esta configuración puede indicar que se usa la detección automática, o puede especificar una dirección URL para un archivo de configuración automática de proxy, o puede especificar un servidor proxy real que se va a usar, o bien puede especificar una combinación de los tres. Si esta información incluye una dirección URL de PAC o un servidor proxy, la aplicación WinHTTP puede intentar usarlos.

Puede encontrar un ejemplo que usa las funciones [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) en los ejemplos de WinHTTP del Kit de desarrollo de software de plataforma (SDK).

 

 



