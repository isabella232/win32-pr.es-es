---
description: Para que un servidor acepte conexiones de cliente, se debe enlazar a una dirección de red dentro del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Enlazar un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715139"
---
# <a name="binding-a-socket"></a><span data-ttu-id="5d7f6-103">Enlazar un socket</span><span class="sxs-lookup"><span data-stu-id="5d7f6-103">Binding a Socket</span></span>

<span data-ttu-id="5d7f6-104">Para que un servidor acepte conexiones de cliente, se debe enlazar a una dirección de red dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="5d7f6-105">En el código siguiente se muestra cómo enlazar un socket que ya se ha creado a una dirección IP y un puerto.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="5d7f6-106">Las aplicaciones cliente usan la dirección IP y el puerto para conectarse a la red del host.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="5d7f6-107">Para enlazar un socket</span><span class="sxs-lookup"><span data-stu-id="5d7f6-107">To bind a socket</span></span>

<span data-ttu-id="5d7f6-108">La estructura [**sockaddr**](sockaddr-2.md) contiene información relacionada con la familia de direcciones, la dirección IP y el número de puerto.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="5d7f6-109">Llame a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , pasando el **socket** creado y la estructura [**sockaddr**](sockaddr-2.md) devuelta desde la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) como parámetros.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="5d7f6-110">Compruebe si hay errores generales.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="5d7f6-111">Una vez que se llama a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) , ya no se necesita la información de dirección devuelta por la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="5d7f6-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="5d7f6-112">Se llama a la función [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) para liberar la memoria asignada por la función **función getaddrinfo** para esta información de dirección.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="5d7f6-113">Siguiente paso: [escuchar en un socket](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="5d7f6-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d7f6-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d7f6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7f6-115">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="5d7f6-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="5d7f6-116">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="5d7f6-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="5d7f6-117">Crear un socket para el servidor</span><span class="sxs-lookup"><span data-stu-id="5d7f6-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



