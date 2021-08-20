---
description: En el código siguiente se muestran las funciones recv y send usadas por el servidor.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Recepción y envío de datos en el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f943fe9f1c4045c087b31861bc6db5f1eb394ad800ee0133e0ec8fb668fcbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857855"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Recepción y envío de datos en el servidor

En el código siguiente se muestran las [**funciones recv**](/windows/desktop/api/winsock/nf-winsock-recv) [**y send**](/windows/desktop/api/Winsock2/nf-winsock2-send) usadas por el servidor.

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



Las [**funciones send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error. Cada función también toma los mismos parámetros: el socket activo, un búfer **char,** el número de bytes que se envían o reciben y cualquier marca que se va a usar.

Paso siguiente: [Desconectar el servidor](disconnecting-the-server.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Aplicación de servidor Winsock](winsock-server-application.md)
</dt> <dt>

[Aceptación de una conexión](accepting-a-connection.md)
</dt> </dl>

 

 



