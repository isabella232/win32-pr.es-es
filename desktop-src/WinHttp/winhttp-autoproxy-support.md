---
description: Para facilitar la configuración de proxy, WinHTTP 5.1 implementa el protocolo de detección automática de proxy web (WPAD), también conocido como proxy automático.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Compatibilidad con WinHTTP AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f6a07645fd7d8bcd401bf399d2a9f525499c4d3a725e49b9d170c067092f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614085"
---
# <a name="winhttp-autoproxy-support"></a>Compatibilidad con WinHTTP AutoProxy

Para facilitar la configuración de proxy, WinHTTP 5.1 implementa el protocolo de detección automática de proxy web (WPAD), también conocido como proxy automático.

## <a name="overview-of-autoproxy"></a>Introducción a AutoProxy

Las aplicaciones y los componentes que usan WinHTTP para enviar solicitudes HTTP deben asegurarse de que la configuración del proxy está establecida correctamente. A menos que el cliente tenga una conexión directa a Internet, normalmente se debe enviar una solicitud HTTP a través de un servidor proxy web que conecte la red local del cliente a Internet (por ejemplo, esto suele ser el caso de los clientes web en una LAN corporativa). En el caso de las aplicaciones basadas en servidor, la configuración del proxy normalmente la administra el administrador del servidor mediante la utilidad de ProxyCfg.exe WinHTTP. El administrador del servidor conoce el nombre del servidor proxy de antemano y usa ProxyCfg.exe para registrar esta configuración en el registro donde WinHTTP puede buscarlo. Sin embargo, la necesidad de que los usuarios finales del escritorio del cliente configuren manualmente los valores del proxy WinHTTP es problemática. Es posible que el usuario final no conozca el nombre del servidor proxy; requerir al usuario final que ejecute la utilidad ProxyCfg.exe puede ser una carga de soporte técnico para una organización. Para admitir una buena experiencia del usuario, una aplicación cliente habilitada para web debe determinar la configuración del proxy sin intervención del usuario.

Para facilitar la configuración del proxy para aplicaciones basadas en WinHTTP, WinHTTP ahora implementa el protocolo de detección automática de proxy web [(WPAD),](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)que a menudo se conoce como *proxy automático.* Se trata del mismo protocolo que implementan los exploradores web para detectar automáticamente la configuración del proxy sin necesidad de que un usuario final especifique manualmente un servidor proxy. Esta característica está disponible a partir de WinHTTP versión 5.1 en Windows 2000 Service Pack 3, Windows XP Service Pack 1 y Windows Server 2003. Tenga en cuenta que aunque Microsoft Internet Explorer y Microsoft WinHTTP admiten WPAD, la especificación nunca ha progresado más allá de la fase "Internet-Draft" y expiró en mayo de 2001.

El protocolo WPAD funciona de la siguiente manera:

1.  Mediante los protocolos de red DHCP o DNS, se detecta la dirección URL de un archivo de configuración automática (PAC) de proxy. La dirección URL identifica un archivo PAC en la red local del cliente. WinHTTP solo admite direcciones URL de PAC "http:" y "https:"; no admite, por ejemplo, direcciones URL de "archivo:".
2.  El archivo PAC se descarga y, opcionalmente, se almacena en caché en el equipo del cliente. El archivo PAC es un script ejecutable que genera una lista de uno o varios servidores proxy según un nombre de host de destino y una dirección URL. WinHTTP solo admite archivos PAC basados en ECMAScript.
3.  En cada solicitud HTTP, se ejecuta el código de script PAC, con el nombre de host y la dirección URL de la solicitud HTTP pasadas como parámetros. WinHTTP espera que el código de script PAC contenga una función denominada **FindProxyForURL**, con el formato siguiente:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Esta función calcula una lista de uno o varios servidores proxy que puede usar el cliente HTTP para transmitir la solicitud. Si el script PAC determina que el cliente HTTP puede llegar al servidor de destino directamente sin pasar por un servidor proxy, lo indica mediante un valor devuelto especial.

## <a name="autoproxy-topics"></a>Temas de AutoProxy

-   [Funciones de WinHTTP AutoProxy](winhttp-autoproxy-api.md)
-   [Detección sin un archivo de configuración automática](discovery-without-an-auto-config-file.md)
-   [Problemas de AutoProxy en WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Establecimiento de configuraciones de proxy wininet en WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Caché de AutoProxy](autoproxy-cache.md)
-   [Extensiones IPv6 para el formato de archivo de configuración automática del navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



