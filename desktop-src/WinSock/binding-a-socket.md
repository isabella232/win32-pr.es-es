---
description: Para que un servidor acepte conexiones de cliente, debe enlazarse a una dirección de red dentro del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Enlazar un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9e745395209228584ea5535864cca57e30494b2e30bfff02fe2abc527ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996925"
---
# <a name="binding-a-socket"></a>Enlazar un socket

Para que un servidor acepte conexiones de cliente, debe enlazarse a una dirección de red dentro del sistema. El código siguiente muestra cómo enlazar un socket que ya se ha creado a una dirección IP y un puerto. Las aplicaciones cliente usan la dirección IP y el puerto para conectarse a la red host.

## <a name="to-bind-a-socket"></a>Para enlazar un socket

La [**estructura sockaddr**](sockaddr-2.md) contiene información sobre la familia de direcciones, la dirección IP y el número de puerto.

Llame a [**la función bind**](/windows/desktop/api/winsock/nf-winsock-bind) y pase el **socket** y la estructura [**sockaddr creados**](sockaddr-2.md) devueltos desde la [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como parámetros. Compruebe si hay errores generales.


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



Una vez [**que se**](/windows/desktop/api/winsock/nf-winsock-bind) llama a la función bind, ya no se necesita la información de dirección devuelta por la función [**getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Se [**llama a la función freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) para liberar la memoria asignada por la función **getaddrinfo** para esta información de dirección.


```C++
    freeaddrinfo(result);

```



Paso siguiente: [Escuchar en un socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Crear un socket para el servidor](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



