---
description: Después de la inicialización, se debe crear una instancia de un objeto de SOCKET para que lo use el servidor.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Crear un socket para el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154290"
---
# <a name="creating-a-socket-for-the-server"></a>Crear un socket para el servidor

Después de la inicialización, se debe crear una instancia de un objeto de **socket** para que lo use el servidor.

**Para crear un socket para el servidor**

1.  La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la estructura [**sockaddr**](sockaddr-2.md) :

    -   **AF \_ INET** se usa para especificar la familia de direcciones IPv4.
    -   **Sock \_ STREAM** se usa para especificar un socket de flujo.
    -   **IPPROTO \_ TCP** se utiliza para especificar el protocolo TCP.
    -   **AI \_** La marca pasiva indica que el autor de la llamada pretende utilizar la estructura de la dirección de socket devuelta en una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) . Cuando se establece la marca de **inteligencia artificial de AI \_** y el parámetro *nodename* en la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) es un puntero **nulo** , la parte de la dirección IP de la estructura de la dirección de socket se establece en **inaddress \_ any** para direcciones IPv4 o en **IN6ADDR \_ cualquier \_ init** para direcciones IPv6.
    -   27015 es el número de puerto asociado al servidor al que se conectará el cliente.

    La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) usa la estructura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) .

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

    

2.  Cree un objeto de **socket** denominado ListenSocket para que el servidor escuche las conexiones de cliente.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y devuelva su valor a la variable ListenSocket. Para esta aplicación de servidor, use la primera dirección IP devuelta por la llamada a [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que coincida con la familia de direcciones, el tipo de socket y el protocolo especificados en el parámetro *hints* . En este ejemplo, se solicitó un socket de flujo TCP para IPv4 con una familia de direcciones IPv4, un tipo de socket de SOCK \_ Stream y un protocolo de IPPROTO \_ TCP. Por lo tanto, se solicita una dirección IPv4 para el ListenSocket.

    Si la aplicación de servidor desea escuchar en IPv6, la familia de direcciones debe establecerse en AF \_ inet6 en el parámetro *hints* . Si un servidor desea escuchar en IPv6 e IPv4, deben crearse dos sockets de escucha, uno para IPv6 y otro para IPv4. La aplicación debe controlar estos dos sockets por separado.

    Windows Vista y versiones posteriores ofrecen la posibilidad de crear un socket IPv6 único que se pone en modo de pila doble para escuchar en IPv6 e IPv4. Para obtener más información sobre esta característica, consulte [sockets de dos pilas](dual-stack-sockets.md).

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

    

Siguiente paso: [enlazar un socket](binding-a-socket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inicializando Winsock](initializing-winsock.md)
</dt> <dt>

[Aplicación Winsock Server](winsock-server-application.md)
</dt> </dl>

 

 
