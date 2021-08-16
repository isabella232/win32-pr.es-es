---
description: Después de la inicialización, se debe crear una instancia de un objeto SOCKET para que lo use el servidor.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Crear un socket para el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e71d6ee0117153b00a9ab77c53bd7555aa031b3fa9d1f7a425ea9aaf0e358f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322205"
---
# <a name="creating-a-socket-for-the-server"></a>Crear un socket para el servidor

Después de la inicialización, se debe crear una instancia de un objeto **SOCKET** para que lo use el servidor.

**Para crear un socket para el servidor**

1.  La [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la [**estructura sockaddr:**](sockaddr-2.md)

    -   **AF \_ INET** se usa para especificar la familia de direcciones IPv4.
    -   **SOCK \_ STREAM** se usa para especificar un socket de secuencia.
    -   **IPPROTO \_ TCP** se usa para especificar el protocolo TCP .
    -   **IA \_ La** marca PASSIVE indica que el autor de la llamada pretende usar la estructura de direcciones de socket devuelta en una llamada a la [**función bind.**](/windows/desktop/api/winsock/nf-winsock-bind) Cuando se establece la marca **AI \_ PASSIVE** y el parámetro *nodename* en la función [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) es un puntero **NULL,** la parte de la dirección IP de la estructura de direcciones de socket se establece en **INADDR \_ ANY** para direcciones IPv4 o **IN6ADDR \_ ANY \_ INIT** para direcciones IPv6.
    -   27015 es el número de puerto asociado al servidor al que se conectará el cliente.

    La [**función getaddrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) usa la estructura [**addrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Cree un **objeto SOCKET** denominado ListenSocket para que el servidor escuche las conexiones de cliente.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Llame a [**la función socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y devuelva su valor a la variable ListenSocket. Para esta aplicación de servidor, use la primera dirección IP devuelta por la llamada a [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que coincida con la familia de direcciones, el tipo de socket y el protocolo especificados en el *parámetro hints.* En este ejemplo, se solicitó un socket de secuencia TCP para IPv4 con una familia de direcciones de IPv4, un tipo de socket de SOCK STREAM y un protocolo \_ IPPROTO \_ TCP. Por lo tanto, se solicita una dirección IPv4 para ListenSocket.

    Si la aplicación de servidor quiere escuchar en IPv6, la familia de direcciones debe establecerse en AF \_ INET6 en el *parámetro hints.* Si un servidor quiere escuchar en IPv6 e IPv4, se deben crear dos sockets de escucha, uno para IPv6 y otro para IPv4. La aplicación debe controlar estos dos sockets por separado.

    Windows Vista y versiones posteriores ofrecen la capacidad de crear un único socket IPv6 que se pone en modo de pila dual para escuchar en IPv6 e IPv4. Para obtener más información sobre esta característica, [vea Sockets de doble pila.](dual-stack-sockets.md)

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Compruebe si hay errores para asegurarse de que el socket es un socket válido.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Paso siguiente: [Enlazar un socket](binding-a-socket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inicialización de Winsock](initializing-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> </dl>

 

 
