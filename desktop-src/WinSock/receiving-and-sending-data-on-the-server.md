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
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="3b0d9-103">Recibir y enviar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="3b0d9-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="3b0d9-104">En el código siguiente se muestran las funciones [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) y [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilizadas por el servidor.</span><span class="sxs-lookup"><span data-stu-id="3b0d9-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="3b0d9-105">Para recibir y enviar datos en un socket</span><span class="sxs-lookup"><span data-stu-id="3b0d9-105">To receive and send data on a socket</span></span>


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



<span data-ttu-id="3b0d9-106">Las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error.</span><span class="sxs-lookup"><span data-stu-id="3b0d9-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="3b0d9-107">Cada función también toma los mismos parámetros: el socket activo, un búfer **Char** , el número de bytes que se van a enviar o recibir y las marcas que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="3b0d9-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="3b0d9-108">Siguiente paso: [desconectar el servidor](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="3b0d9-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b0d9-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b0d9-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0d9-110">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="3b0d9-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="3b0d9-111">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="3b0d9-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="3b0d9-112">Aceptación de una conexión</span><span class="sxs-lookup"><span data-stu-id="3b0d9-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



