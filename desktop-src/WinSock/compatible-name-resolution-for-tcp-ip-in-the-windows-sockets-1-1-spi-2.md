---
description: Windows Sockets 1,1 definía un número de rutinas que se usaban para la resolución de nombres IPv4 con redes TCP/IP. Normalmente se denominan funciones GetXbyY e incluyen lo siguiente.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Resolución de nombres compatible para TCP/IP en Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696396"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Resolución de nombres compatible para TCP/IP en Windows Sockets 1,1 SPI

Windows Sockets 1,1 definía un número de rutinas que se usaban para la resolución de nombres IPv4 con redes TCP/IP. Normalmente se denominan funciones **GetXbyY** e incluyen lo siguiente.

[**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname)

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

Estas funciones son específicas de las redes TCP/IP; no se recomienda que los desarrolladores de aplicaciones independientes del Protocolo sigan usando estas funciones específicas del transporte. Sin embargo, para mantener la compatibilidad estricta con las versiones anteriores de Windows Sockets 1,1, las funciones anteriores siguen siendo compatibles, siempre que exista al menos un proveedor de espacios de nombres que admita la familia de direcciones de AF \_ inet.

El *\_32.dllWs2* implementa estas funciones de compatibilidad en cuanto a las nuevas funciones de resolución de nombres independientes del Protocolo mediante una secuencia adecuada de llamadas a funciones [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . A continuación se proporcionan los detalles sobre cómo se asignan las funciones de **GetXbyY** a las funciones de resolución de nombres. El \_32.dll Ws2 controla las diferencias entre las versiones asincrónica y sincrónica de las funciones de **GetXbyY** , de modo que solo se describe la implementación de las funciones sincrónicas de **GetXbyY** .

 

 
