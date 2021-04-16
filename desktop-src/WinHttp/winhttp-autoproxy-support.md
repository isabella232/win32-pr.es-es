---
description: Para facilitar la configuración de la configuración de proxy, WinHTTP 5,1 implementa el protocolo de detección automática de proxy web (WPAD), también conocido como AutoProxy.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Compatibilidad con el AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705675"
---
# <a name="winhttp-autoproxy-support"></a>Compatibilidad con el AutoProxy WinHTTP

Para facilitar la configuración de la configuración de proxy, WinHTTP 5,1 implementa el protocolo de detección automática de proxy web (WPAD), también conocido como AutoProxy.

## <a name="overview-of-autoproxy"></a>Información general de AutoProxy

Las aplicaciones y los componentes que usan WinHTTP para enviar solicitudes HTTP deben asegurarse de que la configuración del proxy esté establecida correctamente. A menos que el cliente tenga una conexión directa a Internet, normalmente se debe enviar una solicitud HTTP a través de un servidor proxy web que conecta la red local del cliente a Internet (por ejemplo, suele ser el caso de los clientes Web en una LAN corporativa). En el caso de las aplicaciones basadas en servidor, la configuración del proxy se administra normalmente mediante el administrador del servidor mediante la utilidad WinHTTP ProxyCfg.exe. El administrador del servidor conoce el nombre del servidor proxy de antemano y usa ProxyCfg.exe para registrar esta configuración en el registro donde WinHTTP puede buscarla. Sin embargo, requerir que los usuarios finales del escritorio de cliente configuren manualmente la configuración del proxy WinHTTP es problemático. Es posible que el usuario final no conozca el nombre del servidor proxy. solicitar al usuario final que ejecute la utilidad de ProxyCfg.exe puede suponer una carga de soporte técnico para una organización. Para admitir una buena experiencia del usuario, una aplicación cliente habilitada para Web debe determinar la configuración del proxy sin la intervención del usuario.

Para facilitar la configuración del proxy para las aplicaciones basadas en WinHTTP, WinHTTP ahora implementa el [Protocolo de detección automática de proxy web (WPAD)](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), que a menudo se conoce como *AutoProxy*. Este es el mismo protocolo que los exploradores Web implementan para detectar automáticamente la configuración de proxy sin necesidad de que un usuario final especifique un servidor proxy manualmente. Esta característica está disponible a partir de la versión 5,1 de WinHTTP en Windows 2000 Service Pack 3, Windows XP Service Pack 1 y Windows Server 2003. Tenga en cuenta que, aunque Microsoft Internet Explorer y Microsoft WinHTTP admiten WPAD, la especificación nunca progresó después de la fase "Internet-Draft" y expiró el 2001 de mayo.

El protocolo WPAD funciona de la siguiente manera:

1.  Mediante el uso de los protocolos de red DHCP o DNS, se detecta la dirección URL de un archivo de configuración automática de proxy (PAC). La dirección URL identifica un archivo PAC en la red local del cliente. WinHTTP solo admite las direcciones URL "http:" y "https:" PAC; por ejemplo, no admite las direcciones URL "File:".
2.  El archivo PAC se descarga y, opcionalmente, se almacena en caché en el equipo del cliente. El archivo PAC es un script ejecutable que genera una lista de uno o varios servidores proxy, dados un nombre de host y una dirección URL de destino. WinHTTP solo admite archivos PAC basados en ECMAScript.
3.  En cada solicitud HTTP se ejecuta el código del script PAC, con el nombre de host y la dirección URL de la solicitud HTTP pasados como parámetros. WinHTTP espera que el código del script PAC contenga una función llamada **FindProxyForURL**, en el formato:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Esta función calcula una lista de uno o más servidores proxy que puede usar el cliente HTTP para transmitir la solicitud. Si el script de PAC determina que el cliente HTTP puede tener acceso al servidor de destino directamente sin pasar por un servidor proxy, lo indica mediante un valor devuelto especial.

## <a name="autoproxy-topics"></a>Temas de AutoProxy

-   [Funciones de AutoProxy de WinHTTP](winhttp-autoproxy-api.md)
-   [Detección sin un archivo de configuración automática](discovery-without-an-auto-config-file.md)
-   [Problemas de AutoProxy en WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Establecer configuraciones de proxy WinInet en WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Caché de AutoProxy](autoproxy-cache.md)
-   [Extensiones IPv6 para el formato de archivo de configuración automática de navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



