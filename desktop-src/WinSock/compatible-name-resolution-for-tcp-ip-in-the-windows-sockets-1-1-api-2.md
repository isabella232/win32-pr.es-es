---
description: Nota Todas las funciones Windows Sockets 1.1 para la resolución de nombres son específicas de las redes TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322305"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1

> [!Note]  
> Todas las funciones Windows Sockets 1.1 para la resolución de nombres son específicas de las redes TCP/IP IPv4. Se desaconseja encarecidamente a los desarrolladores de aplicaciones seguir utilizando estas funciones específicas del transporte que solo admiten IPv4.

 

Los desarrolladores de aplicaciones deben usar las siguientes funciones independientes del protocolo y admitir la resolución de nombres IPv6 e IPv4.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1.1 definió una serie de rutinas usadas para la resolución de nombres con redes TCP/IP (IP versión 4). A veces se denominan **funciones getXbyY** e incluyen lo siguiente:

<dl>

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

También se definieron versiones asincrónicas de estas funciones.

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

También hay dos funciones, ahora implementadas en la Winsock2.dll, que se usan para convertir la notación de direcciones Ipv4 con puntos a y desde representaciones binarias y de cadena, respectivamente.

<dl>

[**complemento de \_ conjunto de inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Con el fin de conservar la compatibilidad estricta con versiones anteriores con Windows Sockets 1.1, todas las funciones anteriores de solo IPv4 siguen siendo compatibles siempre que al menos un proveedor de espacios de nombres esté presente que admita la familia de direcciones AF INET (estas funciones no son relevantes para la versión 6 de IP, lo que indica \_ AF \_ INET6).

El32.dll Ws2 implementa estas funciones de compatibilidad en términos de las nuevas funciones de resolución de nombres independientes del protocolo mediante una secuencia adecuada de llamadas de función \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End.** A continuación se proporcionan los detalles de cómo se asignan las funciones **getXbyY** a las funciones de resolución de nombres. El32.dll WSs2 controla las diferencias entre las versiones asincrónica y sincrónica de las funciones \_ **getXbyY,** por lo que solo se describe la implementación de las funciones **getXbyY** sincrónicas.

En esta sección se describe la resolución de nombres compatible para TCP/IP en la API Windows Sockets 1.1. En la lista siguiente se describen los temas de esta sección:

-   [Enfoque básico de GetXbyY en la API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Getprotobyname y getprotobynumber Functions en la API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [getservbyname y getservbyport Functions en la API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Gethostbyname (Función) en la API](gethostbyname-function-in-the-api-2.md)
-   [Gethostbyaddr (Función) en la API](gethostbyaddr-function-in-the-api-2.md)
-   [Gethostname (Función) en la API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres independiente del protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
