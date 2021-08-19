---
description: Microsoft Windows HTTP Services (WinHTTP) proporciona una interfaz de alto nivel compatible con el servidor para los protocolos de Internet HTTP/2 y 1.1.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Acerca de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19df8ac8073cfca4fd74fd5d024712cc3fc59c770c3d9ad0ab1386bc0642d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570295"
---
# <a name="about-winhttp"></a>Acerca de WinHTTP

> [!NOTE]
> En el caso de los contenedores de aplicaciones y los servicios del sistema desde Windows 10, la versión 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) está de forma predeterminada.

Microsoft Windows HTTP Services (WinHTTP) proporciona una interfaz de alto nivel compatible con el servidor para los protocolos de Internet HTTP/2 y 1.1. WinHTTP está diseñado para usarse principalmente en escenarios basados en servidor por aplicaciones de servidor que se comunican con servidores HTTP.

[WinINet se](/windows/desktop/WinInet/portal) diseñó como una plataforma de cliente HTTP para aplicaciones de escritorio interactivas. WinINet muestra una interfaz de usuario para algunas operaciones, como la recopilación de credenciales de usuario. Sin embargo, WinHTTP controla estas operaciones mediante programación. Las aplicaciones de servidor que requieren servicios de cliente HTTP deben usar WinHTTP en lugar de WinINet. Para obtener más información, [vea Porting WinINet Applications to WinHTTP (Porting WinINet Applications to WinHTTP [ Porting WinINet Applications to WinHTTP [Porting WinINet Applications to WinHTTP(Por](porting-wininet-applications-to-winhttp.md)

WinHTTP también está diseñado para su uso en servicios del sistema y aplicaciones cliente basadas en HTTP. Sin embargo, las aplicaciones de usuario único que requieren funcionalidad de protocolo FTP, persistencia de cookies, almacenamiento en caché, control automático de cuadros de diálogo de credenciales, compatibilidad de Internet Explorer o compatibilidad con plataformas de nivel inferior deben considerar el uso de [WinINet.](/windows/desktop/WinInet/portal)

Esta interfaz es accesible desde C/C++ mediante la interfaz de programación de aplicaciones (API) WinHTTP o mediante las interfaces [**IWinHttpRequest**](iwinhttprequest-interface.md) e [**IWinHttpRequestEvents.**](iwinhttprequestevents-interface.md) WinHTTP también es accesible desde el script y Microsoft Visual Basic a través del objeto WinHTTP. Para obtener más información y descripciones de las funciones individuales, consulte la referencia de funciones WinHTTP para el lenguaje específico.

A partir de Windows 8, WinHTTP proporciona API para habilitar las conexiones mediante el protocolo [WebSocket](https://tools.ietf.org/html/rfc6455)l, como [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) y [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> WinHTTP no es reentrante excepto durante la devolución de llamada de finalización asincrónica. Es decir, mientras un subproceso tiene una llamada pendiente a una de las funciones WinHTTP como WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData o WinHttpWriteData, nunca debe llamar a WinHTTP una segunda vez hasta que se haya completado la primera llamada. Un escenario en el que podría producirse una segunda llamada es el siguiente: si una aplicación pone en cola una llamada a procedimiento asincrónico (APC) al subproceso que llama a WinHTTP y WinHTTP realiza una espera de alerta internamente, el APC puede ejecutarse. Si la rutina de APC también llama a WinHTTP, vuelve a escribir la API WinHTTP y el estado interno de WinHTTP puede estar dañado.

## <a name="winhttp-51-features"></a>Características de WinHTTP 5.1

Las siguientes características se agregaron en la versión 5.1 de WinHTTP:

-   Compatibilidad con IPv6.
-   Funcionalidades de AutoProxy.
-   Protocolo HTTP/1.0, incluida la compatibilidad con conexiones persistentes (persistentes) y cookies de sesión.
-   Compatibilidad de transferencia fragmentada de HTTP/1.1 para respuestas HTTP.
-   Agrupación keep-alive de conexiones anónimas entre sesiones.
-   Capa de sockets seguros (SSL), incluidos los certificados de cliente. Entre los protocolos SSL admitidos se incluyen los siguientes: SSL 2.0, SSL 3.0 y Seguridad de la capa de transporte (TLS) 1.0.
-   Compatibilidad con la autenticación de servidor y proxy, incluida la compatibilidad integrada con Microsoft Passport 1.4 y el paquete [Negotiate/Kerberos.](../com/kerberos-v5-protocol.md)
-   Control automático de redireccionamientos a menos que se supriman.
-   Interfaz que admite scripts además de la API.
-   Utilidad de seguimiento para ayudar a solucionar problemas.

No se admiten varias características de [WinINet](/windows/desktop/WinInet/portal) en WinHTTP, como el almacenamiento en caché de direcciones URL y las cookies persistentes, el proxy automático, la autodialing, la compatibilidad sin conexión y protocolo de transferencia de archivos (FTP).

Para obtener más información sobre los cambios introducidos en la versión 5.1, vea Novedades [de WinHTTP 5.1.](what-s-new-in-winhttp-5-1.md)

## <a name="getting-started-with-winhttp"></a>Tareas iniciales con WinHTTP

Para obtener más información sobre WinHTTP, vea los temas siguientes.

* [WinINet frente a WinHTTP](/windows/desktop/wininet/wininet-vs-winhttp) compara las dos tecnologías para acceder a HTTP.
* [Versiones winHTTP](winhttp-versions.md) describe el historial de versiones de WinHTTP.
* [Novedades de WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) describe los cambios y las nuevas características de WinHTTP 5.1.
* [Terminología de red](network-terminology.md) describe conceptos y terminología útiles relacionados con las redes en general y el protocolo HTTP en particular.
* [Al elegir una interfaz WinHTTP](choosing-a-winhttp-interface.md) se describen la API de C/C++ y la interfaz COM para WinHTTP.
* [Consideraciones de seguridad de WinHTTP](winhttp-security-considerations.md) describe los problemas de seguridad que se deben tener en cuenta al usar WinHTTP.
* [En Porting WinINet Applications to WinHTTP (Porting WinINet Applications to WinHTTP)](porting-wininet-applications-to-winhttp.md) se describe cómo modificar las aplicaciones [winINet](/windows/desktop/WinInet/portal) existentes para usar la API WinHTTP.
