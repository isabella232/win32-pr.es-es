---
description: En el código siguiente se muestran las funciones SEND y RECV utilizadas por el cliente una vez establecida una conexión.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Enviar y recibir datos en el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697488"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Enviar y recibir datos en el cliente

En el código siguiente se muestran las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) utilizadas por el cliente una vez establecida una conexión.

## <a name="client"></a>Remoto


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



Las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error. Cada función también toma los mismos parámetros: el socket activo, un búfer **Char** , el número de bytes que se van a enviar o recibir y las marcas que se van a utilizar.

Siguiente paso: [desconectar el cliente](disconnecting-the-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación cliente Winsock](winsock-client-application.md)
</dt> <dt>

[Conexión a un socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



