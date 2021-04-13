---
description: Una vez que el cliente ha finalizado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Desconectar el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360305"
---
# <a name="disconnecting-the-client"></a><span data-ttu-id="4496a-103">Desconectar el cliente</span><span class="sxs-lookup"><span data-stu-id="4496a-103">Disconnecting the Client</span></span>

<span data-ttu-id="4496a-104">Una vez que el cliente ha finalizado el envío y la recepción de datos, el cliente se desconecta del servidor y apaga el socket.</span><span class="sxs-lookup"><span data-stu-id="4496a-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="4496a-105">**Para desconectar y apagar un socket**</span><span class="sxs-lookup"><span data-stu-id="4496a-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="4496a-106">Cuando el cliente ha terminado de enviar datos al servidor, se puede llamar a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) especificando el \_ envío de SD para apagar el lado de envío del socket.</span><span class="sxs-lookup"><span data-stu-id="4496a-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="4496a-107">Esto permite al servidor liberar algunos de los recursos de este socket.</span><span class="sxs-lookup"><span data-stu-id="4496a-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="4496a-108">La aplicación cliente todavía puede recibir datos en el socket.</span><span class="sxs-lookup"><span data-stu-id="4496a-108">The client application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="4496a-109">Cuando la aplicación cliente ha terminado de recibir datos, se llama a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para cerrar el socket.</span><span class="sxs-lookup"><span data-stu-id="4496a-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="4496a-110">Cuando la aplicación cliente se completa mediante el archivo DLL de Windows Sockets, se llama a la función [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="4496a-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="4496a-111">Completar código fuente de cliente</span><span class="sxs-lookup"><span data-stu-id="4496a-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="4496a-112">Completar el código de cliente</span><span class="sxs-lookup"><span data-stu-id="4496a-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="4496a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4496a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4496a-114">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="4496a-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="4496a-115">Aplicación cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="4496a-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="4496a-116">Enviar y recibir datos en el cliente</span><span class="sxs-lookup"><span data-stu-id="4496a-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



