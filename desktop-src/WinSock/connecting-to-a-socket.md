---
description: Para que un cliente se comunique en una red, debe conectarse a un servidor.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Conexión a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705645"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="60269-103">Conexión a un socket</span><span class="sxs-lookup"><span data-stu-id="60269-103">Connecting to a Socket</span></span>

<span data-ttu-id="60269-104">Para que un cliente se comunique en una red, debe conectarse a un servidor.</span><span class="sxs-lookup"><span data-stu-id="60269-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="60269-105">Para conectarse a un socket</span><span class="sxs-lookup"><span data-stu-id="60269-105">To connect to a socket</span></span>

<span data-ttu-id="60269-106">Llame a la función [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , pasando el socket creado y la estructura [**sockaddr**](sockaddr-2.md) como parámetros.</span><span class="sxs-lookup"><span data-stu-id="60269-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="60269-107">Compruebe si hay errores generales.</span><span class="sxs-lookup"><span data-stu-id="60269-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="60269-108">La función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) se usa para determinar los valores de la estructura [**sockaddr**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="60269-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="60269-109">En este ejemplo, la primera dirección IP devuelta por la función **función getaddrinfo** se usa para especificar la estructura **sockaddr** que se pasa a [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span><span class="sxs-lookup"><span data-stu-id="60269-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="60269-110">Si se produce un error en la llamada de **conexión** a la primera dirección IP, intente la siguiente estructura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) en la lista vinculada devuelta por la función **función getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="60269-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="60269-111">La información especificada en la estructura [**sockaddr**](sockaddr-2.md) incluye:</span><span class="sxs-lookup"><span data-stu-id="60269-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="60269-112">la dirección IP del servidor al que el cliente intentará conectarse.</span><span class="sxs-lookup"><span data-stu-id="60269-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="60269-113">número de puerto del servidor al que se conectará el cliente.</span><span class="sxs-lookup"><span data-stu-id="60269-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="60269-114">Este puerto se especificó como el puerto 27015 cuando el cliente llamó a la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="60269-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="60269-115">Siguiente paso: [enviar y recibir datos en el cliente](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="60269-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="60269-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60269-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60269-117">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="60269-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="60269-118">Aplicación cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="60269-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="60269-119">Crear un socket para el cliente</span><span class="sxs-lookup"><span data-stu-id="60269-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
