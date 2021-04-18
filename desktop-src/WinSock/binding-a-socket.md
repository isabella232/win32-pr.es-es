---
description: Para que un servidor acepte conexiones de cliente, se debe enlazar a una dirección de red dentro del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Enlazar un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715139"
---
# <a name="binding-a-socket"></a>Enlazar un socket

Para que un servidor acepte conexiones de cliente, se debe enlazar a una dirección de red dentro del sistema. En el código siguiente se muestra cómo enlazar un socket que ya se ha creado a una dirección IP y un puerto. Las aplicaciones cliente usan la dirección IP y el puerto para conectarse a la red del host.

## <a name="to-bind-a-socket"></a>Para enlazar un socket

La estructura [**sockaddr**](sockaddr-2.md) contiene información relacionada con la familia de direcciones, la dirección IP y el número de puerto.

Llame a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , pasando el **socket** creado y la estructura [**sockaddr**](sockaddr-2.md) devuelta desde la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como parámetros. Compruebe si hay errores generales.


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



Una vez que se llama a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , ya no se necesita la información de dirección devuelta por la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Se llama a la función [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) para liberar la memoria asignada por la función **función getaddrinfo** para esta información de dirección.


```C++
    freeaddrinfo(result);

```



Siguiente paso: [escuchar en un socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación Winsock Server](winsock-server-application.md)
</dt> <dt>

[Crear un socket para el servidor](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



