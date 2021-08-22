---
description: Windows Sockets 1.1 definió una serie de rutinas que se usaron para la resolución de nombres IPv4 con redes TCP/IP. Estas funciones se denominan habitualmente funciones GetXbyY e incluyen lo siguiente.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Resolución de nombres compatible para TCP/IP en Windows Sockets 1.1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051683"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Resolución de nombres compatible para TCP/IP en Windows Sockets 1.1 SPI

Windows Sockets 1.1 definió una serie de rutinas que se usaron para la resolución de nombres IPv4 con redes TCP/IP. Estas funciones se denominan habitualmente **funciones GetXbyY** e incluyen lo siguiente.

[**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

También se definieron versiones asincrónicas de estas funciones.

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Estas funciones son específicas de las redes TCP/IP; No se recomienda a los desarrolladores de aplicaciones independientes del protocolo seguir utilizando estas funciones específicas del transporte. Sin embargo, para conservar la compatibilidad estricta con versiones anteriores con Windows Sockets 1.1, las funciones anteriores siguen siendo compatibles siempre y cuando al menos esté presente un proveedor de espacios de nombres que admita la familia de direcciones \_ AF INET.

El *32.dll\_ Ws2* implementa estas funciones de compatibilidad en términos de las nuevas funciones de resolución de nombres independientes del protocolo mediante una secuencia adecuada de llamadas de función [**WSALookupServiceBegin,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) A continuación se proporcionan los detalles de cómo se asignan las funciones **GetXbyY** a las funciones de resolución de nombres. El Ws232.dll las diferencias entre las versiones asincrónicas y sincrónicas de las funciones GetXbyY, de modo que solo se analice la implementación de las funciones \_ **getXbyY** sincrónicas. 

 

 
