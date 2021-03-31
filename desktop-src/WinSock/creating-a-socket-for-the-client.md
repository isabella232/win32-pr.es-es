---
description: Después de la inicialización, se debe crear una instancia de un objeto de SOCKET para que lo use el cliente.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Crear un socket para el cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907954"
---
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="d5eb4-103">Crear un socket para el cliente</span><span class="sxs-lookup"><span data-stu-id="d5eb4-103">Creating a socket for the client</span></span>

<span data-ttu-id="d5eb4-104">Después de la inicialización, se debe crear una instancia de un objeto de **socket** para que lo use el cliente.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="d5eb4-105">**Para crear un socket**</span><span class="sxs-lookup"><span data-stu-id="d5eb4-105">**To create a socket**</span></span>

1.  <span data-ttu-id="d5eb4-106">Declare un objeto [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) que contenga una estructura [**sockaddr**](sockaddr-2.md) e inicialice estos valores.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="d5eb4-107">Para esta aplicación, la familia de direcciones de Internet no está especificada, por lo que se puede devolver una dirección IPv6 o IPv4.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="d5eb4-108">La aplicación solicita que el tipo de socket sea un socket de secuencia para el protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="d5eb4-109">Llame a la función [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) solicitando la dirección IP para el nombre de servidor que se ha pasado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="d5eb4-110">El puerto TCP del servidor al que se conectará el cliente se define de forma predeterminada \_ como 27015 en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="d5eb4-111">La función **función getaddrinfo** devuelve su valor como un entero en el que se comprueban los errores.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  <span data-ttu-id="d5eb4-112">Cree un objeto de **socket** llamado ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="d5eb4-113">Llame a la función [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y devuelva su valor a la variable ConnectSocket.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="d5eb4-114">Para esta aplicación, use la primera dirección IP devuelta por la llamada a [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) que coincida con la familia de direcciones, el tipo de socket y el protocolo especificados en el parámetro *hints* .</span><span class="sxs-lookup"><span data-stu-id="d5eb4-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="d5eb4-115">En este ejemplo, se especificó un socket de flujo TCP con un tipo de socket de \_ flujo Sock y un protocolo de IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="d5eb4-116">No se especificó la familia de direcciones (AF \_ unspec), por lo que la dirección IP devuelta podría ser una dirección IPv6 o IPv4 para el servidor.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="d5eb4-117">Si la aplicación cliente desea conectarse solo con IPv6 o IPv4, la familia de direcciones debe establecerse en AF \_ inet6 para IPv6 o AF \_ inet para IPv4 en el parámetro *hints* .</span><span class="sxs-lookup"><span data-stu-id="d5eb4-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="d5eb4-118">Compruebe si hay errores para asegurarse de que el socket es un socket válido.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="d5eb4-119">Los parámetros pasados a la función de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) se pueden cambiar para implementaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="d5eb4-120">La detección de errores es una parte fundamental del correcto código de red.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="d5eb4-121">Si se produce un error en la llamada de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , devuelve un socket no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="d5eb4-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="d5eb4-122">La instrucción **If** del código anterior se usa para detectar los errores que se hayan producido al crear el socket.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="d5eb4-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve un número de error asociado al último error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="d5eb4-124">En función de la aplicación, es posible que sea necesario realizar una comprobación de errores más extensa.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="d5eb4-125">Por ejemplo, si se establece *hints.ai_family* en **AF_UNSPEC** puede producirse un error en la llamada Connect.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="d5eb4-126">Si esto ocurre, utilice en su lugar un valor de IPv4 (**AF_INET**) o IPv6 (**AF_INET6**) específico.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="d5eb4-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) se usa para terminar el uso de la \_ dll WS2 32.</span><span class="sxs-lookup"><span data-stu-id="d5eb4-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="d5eb4-128">Siguiente paso: [conectarse a un socket](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="d5eb4-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5eb4-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5eb4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5eb4-130">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="d5eb4-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="d5eb4-131">Inicializando Winsock</span><span class="sxs-lookup"><span data-stu-id="d5eb4-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="d5eb4-132">Aplicación cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="d5eb4-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
