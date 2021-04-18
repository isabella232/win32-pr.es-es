---
description: El SPI de transporte Winsock es similar a la API de Winsock en que aparecen todas las funciones básicas de socket.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Asignación de transporte entre las funciones de API y SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f11b950c48d0887f1e593c65f9d77e27c33917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706823"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Asignación de transporte entre las funciones de API y SPI

El SPI de transporte Winsock es similar a la API de Winsock en que aparecen todas las funciones básicas de socket. Cuando hay una nueva versión de una función de Winsock y la versión original en la API, solo se mostrará la nueva versión en el SPI. Esto se muestra en la lista siguiente.

-   [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) y [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) se asignan a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) y [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) se asignan a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) se asignan a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Otras funciones de la API que están contraídas en las versiones mejoradas en SPI incluyen:

-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Las funciones de soporte como [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons**](/windows/desktop/api/winsock/nf-winsock-htons), [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)y [**NTOHS**](/windows/desktop/api/winsock/nf-winsock-ntohs) se implementan en el \_32.dll Ws2 y no se pasan a los proveedores de servicios. Lo mismo se aplica a las versiones WSA de estas funciones.

La enumeración de proveedores de servicios de Windows Sockets y las funciones relacionadas con el enlace de bloqueo se realizan en el \_32.dll Ws2, por lo que [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking), [WSASetBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook)y [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) no aparecen como funciones SPI.

Dado que los códigos de error se devuelven junto con las funciones SPI, no se requieren equivalentes de [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) y [**WSASETLASTERROR**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) en el SPI.

Las funciones de manipulación y espera de objetos de eventos, incluidas [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)y [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , se asignan directamente a los servicios nativos de Windows y, por tanto, no están presentes en el SPI.

Todas las funciones de conversión y resolución de nombres específicos de TCP/IP en Windows Sockets 1,1 como **GetXbyY**, **WSAAsyncGetXByY** y [**WSACancelAsyncRequest**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest), así como [**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname) se implementan dentro del \_32.dll de Ws2 en cuanto a las nuevas funciones de resolución de nombres. Para obtener más información, vea [resolución de nombres compatible para TCP/IP en Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Las funciones de conversión como [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) y [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) se implementan dentro del32.dll de Ws2 \_ .

 

 
