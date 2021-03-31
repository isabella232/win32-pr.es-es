---
description: Una vez que el servidor finaliza la recepción de datos del cliente y el envío de datos al cliente, el servidor se desconecta del cliente y apaga el socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Desconectar el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907952"
---
# <a name="disconnecting-the-server"></a><span data-ttu-id="2d9f2-103">Desconectar el servidor</span><span class="sxs-lookup"><span data-stu-id="2d9f2-103">Disconnecting the Server</span></span>

<span data-ttu-id="2d9f2-104">Una vez que el servidor finaliza la recepción de datos del cliente y el envío de datos al cliente, el servidor se desconecta del cliente y apaga el socket.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="2d9f2-105">**Para desconectar y apagar un socket**</span><span class="sxs-lookup"><span data-stu-id="2d9f2-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="2d9f2-106">Cuando el servidor ha terminado de enviar datos al cliente, se puede llamar a la función [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) especificando el \_ envío de SD para apagar el lado de envío del socket.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="2d9f2-107">Esto permite al cliente liberar algunos de los recursos de este socket.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="2d9f2-108">La aplicación de servidor todavía puede recibir datos en el socket.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-108">The server application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="2d9f2-109">Cuando la aplicación cliente ha terminado de recibir datos, se llama a la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) para cerrar el socket.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="2d9f2-110">Cuando la aplicación cliente se completa mediante el archivo DLL de Windows Sockets, se llama a la función [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="2d9f2-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="2d9f2-111">Código fuente completo del servidor</span><span class="sxs-lookup"><span data-stu-id="2d9f2-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="2d9f2-112">Código de servidor completo</span><span class="sxs-lookup"><span data-stu-id="2d9f2-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="2d9f2-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d9f2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9f2-114">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="2d9f2-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="2d9f2-115">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="2d9f2-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="2d9f2-116">Recibir y enviar datos en el servidor</span><span class="sxs-lookup"><span data-stu-id="2d9f2-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="2d9f2-117">Ejecución del ejemplo de código de servidor y cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="2d9f2-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



