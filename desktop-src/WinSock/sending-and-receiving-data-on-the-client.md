---
description: El código siguiente muestra las funciones send y recv usadas por el cliente una vez establecida una conexión.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Envío y recepción de datos en el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3150c853f50e8626451cc344179645289058df928600d71bf437dc95d9738986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740566"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Envío y recepción de datos en el cliente

El código siguiente muestra las [**funciones send**](/windows/desktop/api/Winsock2/nf-winsock2-send) [**y recv**](/windows/desktop/api/winsock/nf-winsock-recv) usadas por el cliente una vez establecida una conexión.

## <a name="client"></a>Cliente


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



Las [**funciones send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error. Cada función también toma los mismos parámetros: el socket activo, un búfer **char,** el número de bytes que se envían o reciben y cualquier marca que se va a usar.

Paso siguiente: [Desconectar el cliente](disconnecting-the-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente winsock](winsock-client-application.md)
</dt> <dt>

[Conexión a un socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



