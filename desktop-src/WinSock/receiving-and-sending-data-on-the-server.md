---
description: En el código siguiente se muestran las funciones RECV y Send utilizadas por el servidor.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Recibir y enviar datos en el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706196"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Recibir y enviar datos en el servidor

En el código siguiente se muestran las funciones [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) y [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilizadas por el servidor.

### <a name="to-receive-and-send-data-on-a-socket"></a>Para recibir y enviar datos en un socket


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



Las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error. Cada función también toma los mismos parámetros: el socket activo, un búfer **Char** , el número de bytes que se van a enviar o recibir y las marcas que se van a utilizar.

Siguiente paso: [desconectar el servidor](disconnecting-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación Winsock Server](winsock-server-application.md)
</dt> <dt>

[Aceptación de una conexión](accepting-a-connection.md)
</dt> </dl>

 

 



