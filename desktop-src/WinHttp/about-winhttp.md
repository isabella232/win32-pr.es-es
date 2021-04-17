---
description: Los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan una interfaz de alto nivel compatible con el servidor para los protocolos de Internet HTTP/2 y 1,1.
ms.assetid: 8337f699-3ec0-4397-acc2-6dc813f7542d
title: Acerca de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150c829410a1601a3ede7f115f4594276af7fead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687886"
---
# <a name="about-winhttp"></a>Acerca de WinHTTP

> [!NOTE]
> En el caso de los contenedores de aplicaciones y los servicios del sistema desde Windows 10, versión 1709, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) está activada de forma predeterminada.

Los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan una interfaz de alto nivel compatible con el servidor para los protocolos de Internet HTTP/2 y 1,1. WinHTTP está diseñado para usarse principalmente en escenarios basados en servidor por aplicaciones de servidor que se comunican con servidores HTTP.

[WinInet](/windows/desktop/WinInet/portal) se diseñó como una plataforma de cliente http para las aplicaciones de escritorio interactivas. WinINet muestra una interfaz de usuario para algunas operaciones, como la recopilación de credenciales de usuario. Sin embargo, WinHTTP controla estas operaciones mediante programación. Las aplicaciones de servidor que requieran servicios de cliente HTTP deben usar WinHTTP en lugar de WinINet. Para obtener más información, vea [migrar aplicaciones WinInet a winhttp](porting-wininet-applications-to-winhttp.md).

WinHTTP también está diseñado para su uso en servicios del sistema y aplicaciones cliente basadas en HTTP. Sin embargo, las aplicaciones de un solo usuario que requieren funcionalidad del protocolo FTP, persistencia de cookies, almacenamiento en caché, control automático de cuadros de diálogo de credenciales, compatibilidad con Internet Explorer o compatibilidad con plataformas de nivel inferior deben considerar el uso de [WinInet](/windows/desktop/WinInet/portal).

Se puede tener acceso a esta interfaz desde C/C++ mediante la interfaz de programación de aplicaciones (API) de WinHTTP o mediante las interfaces [**IWinHttpRequest**](iwinhttprequest-interface.md) y [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) . También se puede tener acceso a WinHTTP desde el script y Microsoft Visual Basic a través del objeto WinHTTP. Para obtener más información y descripciones de las funciones individuales, vea la referencia de funciones WinHTTP para el lenguaje específico.

A partir de Windows 8, WinHTTP proporciona API para habilitar conexiones mediante el [Protocolo WebSocket](https://tools.ietf.org/html/rfc6455)l, como [**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend) y [**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive).

> [!Caution]  
> WinHTTP no es reentrante, excepto durante la devolución de llamada de finalización asincrónica. Es decir, mientras que un subproceso tiene una llamada pendiente a una de las funciones WinHTTP como WinHttpSendRequest, WinHttpReceiveResponse, WinHttpQueryDataAvailable, WinHttpSendData o WinHttpWriteData, nunca debe llamar a WinHTTP una segunda vez hasta que se complete la primera llamada. Un escenario en el que podría producirse una segunda llamada es el siguiente: Si una aplicación pone en cola una llamada a procedimiento asincrónico (APC) al subproceso que llama a WinHTTP y, si WinHTTP realiza una espera de alerta internamente, se puede ejecutar la APC. Si la rutina APC se produce también para llamar a WinHTTP, se reentra en la API WinHTTP y el estado interno de WinHTTP puede estar dañado.

## <a name="winhttp-51-features"></a>Características de WinHTTP 5,1

Se han agregado las siguientes características en la versión 5,1 de WinHTTP:

-   Compatibilidad con IPv6.
-   Capacidades de proxy AutoProxy.
-   Protocolo HTTP/1.0, incluida la compatibilidad con las conexiones persistentes (persistentes) y las cookies de sesión.
-   Compatibilidad con la transferencia fragmentada de HTTP/1.1 para respuestas HTTP.
-   Agrupación persistente de conexiones anónimas entre sesiones.
-   Funcionalidad de Capa de sockets seguros (SSL), incluidos los certificados de cliente. Entre los protocolos SSL admitidos se incluyen los siguientes: SSL 2,0, SSL 3,0 y seguridad de la capa de transporte (TLS) 1,0.
-   Compatibilidad con la autenticación de servidor y proxy, incluida la compatibilidad integrada con Microsoft Passport 1,4 y el paquete Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md) .
-   El control automático de las redirecciones a menos que se suprima.
-   Interfaz que admite scripts además de la API.
-   Utilidad de seguimiento que ayuda a solucionar problemas.

No se admiten varias características de [WinInet](/windows/desktop/WinInet/portal) en WinHTTP, como el almacenamiento en caché de direcciones URL y las cookies persistentes, el proxy automático, el marcado automático, la compatibilidad sin conexión y el protocolo de transferencia de archivos (FTP).

Para obtener más información sobre los cambios introducidos en la versión 5,1, vea [novedades de WinHTTP 5,1](what-s-new-in-winhttp-5-1.md).

## <a name="getting-started-with-winhttp"></a>Introducción con WinHTTP

Para obtener más información acerca de WinHTTP, vea los temas siguientes.

* [WinInet frente a winhttp](/windows/desktop/wininet/wininet-vs-winhttp) compara las dos tecnologías para tener acceso a http.
* [Versiones de WinHTTP](winhttp-versions.md) describe el historial de versiones de winhttp.
* [Novedades de winhttp 5,1](what-s-new-in-winhttp-5-1.md) describe los cambios y las nuevas características de WinHTTP 5,1.
* [Terminología de red](network-terminology.md) describe conceptos y terminología útiles relacionados con las redes en general y el protocolo http en particular.
* Al [elegir una interfaz WinHTTP](choosing-a-winhttp-interface.md) se describe la API de C/C++ y la interfaz com para winhttp.
* Las [consideraciones de seguridad de WinHTTP](winhttp-security-considerations.md) describen los problemas de seguridad que se deben tener en cuenta al usar winhttp.
* [Trasladar aplicaciones WinInet a winhttp](porting-wininet-applications-to-winhttp.md) describe cómo modificar las aplicaciones [WinInet](/windows/desktop/WinInet/portal) existentes para usar la API winhttp.
