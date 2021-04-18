---
description: Una vez que el socket está escuchando una conexión, el programa debe controlar las solicitudes de conexión en ese socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Aceptación de una conexión (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652423"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="84782-103">Aceptación de una conexión (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="84782-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="84782-104">Una vez que el socket está escuchando una conexión, el programa debe controlar las solicitudes de conexión en ese socket.</span><span class="sxs-lookup"><span data-stu-id="84782-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="84782-105">**Para aceptar una conexión en un socket**</span><span class="sxs-lookup"><span data-stu-id="84782-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="84782-106">Cree un objeto de **socket** temporal denominado ClientSocket para aceptar conexiones de los clientes.</span><span class="sxs-lookup"><span data-stu-id="84782-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="84782-107">Normalmente, una aplicación de servidor se diseñaría para escuchar las conexiones de varios clientes.</span><span class="sxs-lookup"><span data-stu-id="84782-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="84782-108">En el caso de los servidores de alto rendimiento, se suelen usar varios subprocesos para administrar varias conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="84782-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="84782-109">Hay varias técnicas de programación diferentes con Winsock que se pueden usar para realizar escuchas de varias conexiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="84782-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="84782-110">Una técnica de programación consiste en crear un bucle continuo que compruebe las solicitudes de conexión mediante la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (consulte [escucha en un socket](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="84782-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="84782-111">Si se produce una solicitud de conexión, la aplicación llama a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) y pasa el trabajo a otro subproceso para controlar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84782-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="84782-112">Son posibles otras técnicas de programación.</span><span class="sxs-lookup"><span data-stu-id="84782-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="84782-113">Tenga en cuenta que este ejemplo básico es muy sencillo y no utiliza varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="84782-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="84782-114">El ejemplo también simplemente escucha y acepta una única conexión.</span><span class="sxs-lookup"><span data-stu-id="84782-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="84782-115">Una vez aceptada la conexión de cliente, una aplicación de servidor pasaría normalmente el socket de cliente aceptado (la variable ClientSocket del código de ejemplo anterior) a un subproceso de trabajo o a un puerto de finalización de e/s y seguir aceptando conexiones adicionales.</span><span class="sxs-lookup"><span data-stu-id="84782-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="84782-116">En este ejemplo básico, el servidor continúa con el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="84782-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="84782-117">Existen otras técnicas de programación que se pueden utilizar para realizar escuchas y aceptar varias conexiones.</span><span class="sxs-lookup"><span data-stu-id="84782-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="84782-118">Esto incluye el uso de las funciones [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="84782-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="84782-119">En los [ejemplos avanzados de Winsock](getting-started-with-winsock.md) que se incluyen con el kit de desarrollo de software (SDK) de Microsoft Windows se muestran ejemplos de algunas de estas técnicas de programación.</span><span class="sxs-lookup"><span data-stu-id="84782-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="84782-120">En los sistemas UNIX, una técnica de programación común para los servidores era que una aplicación escuche conexiones.</span><span class="sxs-lookup"><span data-stu-id="84782-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="84782-121">Cuando se aceptó una conexión, el proceso primario llamaría a la función **Fork** para crear un nuevo proceso secundario con el fin de controlar la conexión de cliente, heredando el socket del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="84782-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="84782-122">Esta técnica de programación no se admite en Windows, ya que la función **Fork** no se admite.</span><span class="sxs-lookup"><span data-stu-id="84782-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="84782-123">Esta técnica tampoco suele ser adecuada para los servidores de alto rendimiento, ya que los recursos necesarios para crear un nuevo proceso son mucho mayores que los necesarios para un subproceso.</span><span class="sxs-lookup"><span data-stu-id="84782-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="84782-124">Siguiente paso: [recibir y enviar datos en el servidor](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="84782-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="84782-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84782-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84782-126">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="84782-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="84782-127">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="84782-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="84782-128">Escuchar en un socket</span><span class="sxs-lookup"><span data-stu-id="84782-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
