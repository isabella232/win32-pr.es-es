---
description: Después de la inicialización, se debe crear una instancia de un objeto de SOCKET para que lo use el servidor.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Crear un socket para el servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154290"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="57ada-103">Crear un socket para el servidor</span><span class="sxs-lookup"><span data-stu-id="57ada-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="57ada-104">Después de la inicialización, se debe crear una instancia de un objeto de **socket** para que lo use el servidor.</span><span class="sxs-lookup"><span data-stu-id="57ada-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="57ada-105">**Para crear un socket para el servidor**</span><span class="sxs-lookup"><span data-stu-id="57ada-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="57ada-106">La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la estructura [**sockaddr**](sockaddr-2.md) :</span><span class="sxs-lookup"><span data-stu-id="57ada-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="57ada-107">**AF \_ INET** se usa para especificar la familia de direcciones IPv4.</span><span class="sxs-lookup"><span data-stu-id="57ada-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="57ada-108">**Sock \_ STREAM** se usa para especificar un socket de flujo.</span><span class="sxs-lookup"><span data-stu-id="57ada-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="57ada-109">**IPPROTO \_ TCP** se utiliza para especificar el protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="57ada-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="57ada-110">**AI \_** La marca pasiva indica que el autor de la llamada pretende utilizar la estructura de la dirección de socket devuelta en una llamada a la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="57ada-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="57ada-111">Cuando se establece la marca de **inteligencia artificial de AI \_** y el parámetro *nodename* en la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) es un puntero **nulo** , la parte de la dirección IP de la estructura de la dirección de socket se establece en **inaddress \_ any** para direcciones IPv4 o en **IN6ADDR \_ cualquier \_ init** para direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="57ada-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="57ada-112">27015 es el número de puerto asociado al servidor al que se conectará el cliente.</span><span class="sxs-lookup"><span data-stu-id="57ada-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="57ada-113">La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) usa la estructura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) .</span><span class="sxs-lookup"><span data-stu-id="57ada-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="57ada-114">Cree un objeto de **socket** denominado ListenSocket para que el servidor escuche las conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="57ada-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="57ada-115">Llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y devuelva su valor a la variable ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="57ada-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="57ada-116">Para esta aplicación de servidor, use la primera dirección IP devuelta por la llamada a [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que coincida con la familia de direcciones, el tipo de socket y el protocolo especificados en el parámetro *hints* .</span><span class="sxs-lookup"><span data-stu-id="57ada-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="57ada-117">En este ejemplo, se solicitó un socket de flujo TCP para IPv4 con una familia de direcciones IPv4, un tipo de socket de SOCK \_ Stream y un protocolo de IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="57ada-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="57ada-118">Por lo tanto, se solicita una dirección IPv4 para el ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="57ada-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="57ada-119">Si la aplicación de servidor desea escuchar en IPv6, la familia de direcciones debe establecerse en AF \_ inet6 en el parámetro *hints* .</span><span class="sxs-lookup"><span data-stu-id="57ada-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="57ada-120">Si un servidor desea escuchar en IPv6 e IPv4, deben crearse dos sockets de escucha, uno para IPv6 y otro para IPv4.</span><span class="sxs-lookup"><span data-stu-id="57ada-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="57ada-121">La aplicación debe controlar estos dos sockets por separado.</span><span class="sxs-lookup"><span data-stu-id="57ada-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="57ada-122">Windows Vista y versiones posteriores ofrecen la posibilidad de crear un socket IPv6 único que se pone en modo de pila doble para escuchar en IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="57ada-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="57ada-123">Para obtener más información sobre esta característica, consulte [sockets de dos pilas](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="57ada-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="57ada-124">Compruebe si hay errores para asegurarse de que el socket es un socket válido.</span><span class="sxs-lookup"><span data-stu-id="57ada-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="57ada-125">Siguiente paso: [enlazar un socket](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="57ada-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="57ada-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57ada-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ada-127">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="57ada-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="57ada-128">Inicializando Winsock</span><span class="sxs-lookup"><span data-stu-id="57ada-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="57ada-129">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="57ada-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
