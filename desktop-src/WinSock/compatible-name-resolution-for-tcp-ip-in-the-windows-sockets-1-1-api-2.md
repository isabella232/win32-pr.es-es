---
description: Tenga en cuenta que todas las funciones de Windows Sockets 1,1 para la resolución de nombres son específicas de las redes TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696397"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1

> [!Note]  
> Todas las funciones de Windows Sockets 1,1 para la resolución de nombres son específicas de las redes TCP/IP IPv4. No se recomienda a los desarrolladores de aplicaciones seguir usando estas funciones específicas del transporte que solo admiten IPv4.

 

Los desarrolladores de aplicaciones deben usar las siguientes funciones que son independientes del protocolo y admiten la resolución de nombres IPv6 e IPv4.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Sockets 1,1 definía un número de rutinas que se usan para la resolución de nombres con redes TCP/IP (IP versión 4). A veces se denominan funciones **getXbyY** e incluyen lo siguiente:

<dl>

[**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
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

También hay dos funciones, implementadas ahora en el Winsock2.dll, que se usan para convertir la notación de dirección IPv4 con puntos en y desde representaciones binarias y de cadena, respectivamente.

<dl>

[**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

Con el fin de mantener la compatibilidad estricta con las versiones anteriores de Windows Sockets 1,1, todas las funciones anteriores solo de IPv4 siguen siendo compatibles, siempre que haya al menos un proveedor de espacios de nombres presente que admita la familia de direcciones de AF \_ inet (estas funciones no son relevantes para la versión 6 de IP, que se indica mediante AF \_ inet6).

El \_32.dll Ws2 implementa estas funciones de compatibilidad en cuanto a las nuevas funciones de resolución de nombres independientes del Protocolo mediante una secuencia adecuada [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)de /  / llamadas a funciones de siguiente **fin** de WSALookupServiceBegin. A continuación se proporcionan los detalles sobre cómo se asignan las funciones de **getXbyY** a las funciones de resolución de nombres. El \_32.dll WSs2 controla las diferencias entre las versiones asincrónica y sincrónica de las funciones de **getXbyY** , por lo que solo se describe la implementación de las funciones sincrónicas de **getXbyY** .

En esta sección se describe la resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1. En la lista siguiente se describen los temas de esta sección:

-   [Enfoque básico para GetXbyY en la API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Funciones getprotobyname y getprotobynumber en la API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Funciones getservbyname y getservbyport en la API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Función gethostbyname en la API](gethostbyname-function-in-the-api-2.md)
-   [Función gethostbyaddr en la API](gethostbyaddr-function-in-the-api-2.md)
-   [Función GetHostName (en la API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resolución de nombres independiente del Protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro y resolución de nombres](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
