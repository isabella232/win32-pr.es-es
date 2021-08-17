---
description: El SPI de transporte de Winsock es similar a winsock API en el que aparecen todas las funciones de socket básicas.
ms.assetid: 37ef8a69-2aa0-4824-8ca9-4b84158086db
title: Asignación de transporte entre funciones DE API y SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf4167353fa05c5656c588a9dff99c96564a5202ffdc4d21edf358c340634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739945"
---
# <a name="transport-mapping-between-api-and-spi-functions"></a>Asignación de transporte entre funciones DE API y SPI

El SPI de transporte de Winsock es similar a winsock API en el que aparecen todas las funciones de socket básicas. Cuando una nueva versión de una función Winsock y la versión original existen en la API, solo se mostrará la nueva versión en el SPI. Esto se muestra en la lista siguiente.

-   [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) y [**WSAConnect se**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) asignan a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))
-   [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) y [**WSAAccept se asignan**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)
-   [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket se**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) asignan a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)

Otras funciones de API que se contraen en las versiones mejoradas de SPI incluyen:

-   [**Enviar**](/windows/desktop/api/Winsock2/nf-winsock2-send)
-   [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)
-   [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)
-   [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)
-   [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)

Las funciones de compatibilidad como [**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl), [**htons,**](/windows/desktop/api/winsock/nf-winsock-htons) [**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)y [**ntmts**](/windows/desktop/api/winsock/nf-winsock-ntohs) se implementan en el32.dll Ws2 y no se pasan a los proveedores \_ de servicios. Lo mismo se aplica a las versiones de WSA de estas funciones.

Windows La enumeración del proveedor de servicios sockets y las funciones relacionadas con el enlace de bloqueo se realizan en el32.dll de Ws2, por lo que \_ [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [WSAIsBlocking,](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) [WSASetBlockingHook y](/windows/desktop/api/winsock2/nf-winsock2-wsasetblockinghook) [WSAUnhookBlockingHook](/windows/desktop/api/winsock2/nf-winsock2-wsaunhookblockinghook) no aparecen como funciones SPI.

Dado que los códigos de error se devuelven junto con las funciones SPI, los equivalentes de [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) y [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) no son necesarios en el SPI.

Las funciones de manipulación y espera de objetos de evento, incluidas [**WSACreateEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) [**WSACloseEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) [**WSASetEvent,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent) [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)y [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) se asignan directamente a los servicios Windows nativos y, por tanto, no están presentes en el SPI.

Todas las funciones de conversión y resolución de nombres específicas de TCP/IP de Windows Sockets 1.1, como **GetXbyY**, **WSAAsyncGetXByY** y [**WSACancelAsyncRequest,**](/windows/desktop/api/winsock/nf-winsock-wsacancelasyncrequest)así como [**gethostname,**](/windows/desktop/api/winsock/nf-winsock-gethostname) se implementan en el32.dll de Ws2 en términos de las nuevas funciones de resolución \_ de nombres. Para obtener más información, [vea Resolución de nombres compatible para TCP/IP en Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md). Las funciones de conversión, [**como inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) e [**inet \_ ntoa,**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) se implementan dentro de la32.dll Ws2. \_

 

 
