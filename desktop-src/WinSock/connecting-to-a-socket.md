---
description: Para que un cliente se comunique en una red, debe conectarse a un servidor.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Conexión a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705645"
---
# <a name="connecting-to-a-socket"></a>Conexión a un socket

Para que un cliente se comunique en una red, debe conectarse a un servidor.

## <a name="to-connect-to-a-socket"></a>Para conectarse a un socket

Llame a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , pasando el socket creado y la estructura [**sockaddr**](sockaddr-2.md) como parámetros. Compruebe si hay errores generales.


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la estructura [**sockaddr**](sockaddr-2.md) . En este ejemplo, la primera dirección IP devuelta por la función **función getaddrinfo** se usa para especificar la estructura **sockaddr** que se pasa a [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Si se produce un error en la llamada de **conexión** a la primera dirección IP, intente la siguiente estructura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) en la lista vinculada devuelta por la función **función getaddrinfo** .

La información especificada en la estructura [**sockaddr**](sockaddr-2.md) incluye:

-   la dirección IP del servidor al que el cliente intentará conectarse.
-   número de puerto del servidor al que se conectará el cliente. Este puerto se especificó como el puerto 27015 cuando el cliente llamó a la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

Siguiente paso: [enviar y recibir datos en el cliente](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Crear un socket para el cliente](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
