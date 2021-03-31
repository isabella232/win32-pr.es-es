---
description: Después de la inicialización, se debe crear una instancia de un objeto de SOCKET para que lo use el cliente.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Crear un socket para el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907954"
---
# <a name="creating-a-socket-for-the-client"></a>Crear un socket para el cliente

Después de la inicialización, se debe crear una instancia de un objeto de **socket** para que lo use el cliente.

**Para crear un socket**

1.  Declare un objeto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) que contenga una estructura [**sockaddr**](sockaddr-2.md) e inicialice estos valores. Para esta aplicación, la familia de direcciones de Internet no está especificada, por lo que se puede devolver una dirección IPv6 o IPv4. La aplicación solicita que el tipo de socket sea un socket de secuencia para el protocolo TCP.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Llame a la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) solicitando la dirección IP para el nombre de servidor que se ha pasado en la línea de comandos. El puerto TCP del servidor al que se conectará el cliente se define de forma predeterminada \_ como 27015 en este ejemplo. La función **función getaddrinfo** devuelve su valor como un entero en el que se comprueban los errores.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Cree un objeto de **socket** llamado ConnectSocket.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y devuelva su valor a la variable ConnectSocket. Para esta aplicación, use la primera dirección IP devuelta por la llamada a [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que coincida con la familia de direcciones, el tipo de socket y el protocolo especificados en el parámetro *hints* . En este ejemplo, se especificó un socket de flujo TCP con un tipo de socket de \_ flujo Sock y un protocolo de IPPROTO \_ TCP. No se especificó la familia de direcciones (AF \_ unspec), por lo que la dirección IP devuelta podría ser una dirección IPv6 o IPv4 para el servidor.

    Si la aplicación cliente desea conectarse solo con IPv6 o IPv4, la familia de direcciones debe establecerse en AF \_ inet6 para IPv6 o AF \_ inet para IPv4 en el parámetro *hints* .

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Compruebe si hay errores para asegurarse de que el socket es un socket válido.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Los parámetros pasados a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se pueden cambiar para implementaciones diferentes.

La detección de errores es una parte fundamental del correcto código de red. Si se produce un error en la llamada de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , devuelve un socket no válido \_ . La instrucción **If** del código anterior se usa para detectar los errores que se hayan producido al crear el socket. [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve un número de error asociado al último error que se produjo.

> [!Note]  
> En función de la aplicación, es posible que sea necesario realizar una comprobación de errores más extensa.
>
> Por ejemplo, si se establece *hints.ai_family* en **AF_UNSPEC** puede producirse un error en la llamada Connect. Si esto ocurre, utilice en su lugar un valor de IPv4 (**AF_INET**) o IPv6 (**AF_INET6**) específico.

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) se usa para terminar el uso de la \_ dll WS2 32.

Siguiente paso: [conectarse a un socket](connecting-to-a-socket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Inicializando Winsock](initializing-winsock.md)
</dt> <dt>

[Aplicación cliente Winsock](winsock-client-application.md)
</dt> </dl>

 

 
