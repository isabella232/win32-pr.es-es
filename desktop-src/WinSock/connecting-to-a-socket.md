---
description: Para que un cliente se comunique en una red, debe conectarse a un servidor.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Conexión a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132678"
---
# <a name="connecting-to-a-socket"></a>Conexión a un socket

Para que un cliente se comunique en una red, debe conectarse a un servidor.

## <a name="to-connect-to-a-socket"></a>Para conectarse a un socket

Llame a [**la función connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) y pase el socket creado y la estructura [**sockaddr**](sockaddr-2.md) como parámetros. Compruebe si hay errores generales.


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



La [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la [**estructura sockaddr.**](sockaddr-2.md) En este ejemplo, la primera dirección IP devuelta por la función **getaddrinfo** se usa para especificar la **estructura sockaddr** pasada a [**la conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Si se **produce un** error en la llamada de conexión a la primera dirección IP, pruebe la siguiente estructura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) en la lista vinculada devuelta desde la **función getaddrinfo.**

La información especificada en la [**estructura sockaddr**](sockaddr-2.md) incluye:

-   la dirección IP del servidor al que el cliente intentará conectarse.
-   número de puerto en el servidor al que se conectará el cliente. Este puerto se especificó como puerto 27015 cuando el cliente llamó a la [**función getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)

Paso siguiente: [Envío y recepción de datos en el cliente](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente winsock](winsock-client-application.md)
</dt> <dt>

[Crear un socket para el cliente](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
