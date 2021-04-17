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
# <a name="sending-and-receiving-data-on-the-client"></a><span data-ttu-id="0099e-103">Enviar y recibir datos en el cliente</span><span class="sxs-lookup"><span data-stu-id="0099e-103">Sending and Receiving Data on the Client</span></span>

<span data-ttu-id="0099e-104">En el código siguiente se muestran las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) utilizadas por el cliente una vez establecida una conexión.</span><span class="sxs-lookup"><span data-stu-id="0099e-104">The following code demonstrates the [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions used by the client once a connection is established.</span></span>

## <a name="client"></a><span data-ttu-id="0099e-105">Remoto</span><span class="sxs-lookup"><span data-stu-id="0099e-105">Client</span></span>


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



<span data-ttu-id="0099e-106">Las funciones [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) y [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) devuelven un valor entero del número de bytes enviados o recibidos, respectivamente, o un error.</span><span class="sxs-lookup"><span data-stu-id="0099e-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="0099e-107">Cada función también toma los mismos parámetros: el socket activo, un búfer **Char** , el número de bytes que se van a enviar o recibir y las marcas que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="0099e-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="0099e-108">Siguiente paso: [desconectar el cliente](disconnecting-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="0099e-108">Next Step: [Disconnecting the Client](disconnecting-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0099e-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0099e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0099e-110">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="0099e-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="0099e-111">Aplicación cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="0099e-111">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="0099e-112">Conexión a un socket</span><span class="sxs-lookup"><span data-stu-id="0099e-112">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
</dt> </dl>

 

 



