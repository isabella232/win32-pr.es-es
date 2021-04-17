---
description: Después de enlazar el socket a una dirección IP y un puerto del sistema, el servidor debe escuchar en esa dirección IP y el puerto para las solicitudes de conexión entrantes.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Escuchar en un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696374"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="86064-103">Escuchar en un socket</span><span class="sxs-lookup"><span data-stu-id="86064-103">Listening on a Socket</span></span>

<span data-ttu-id="86064-104">Después de enlazar el socket a una dirección IP y un puerto del sistema, el servidor debe escuchar en esa dirección IP y el puerto para las solicitudes de conexión entrantes.</span><span class="sxs-lookup"><span data-stu-id="86064-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="86064-105">Para escuchar en un socket</span><span class="sxs-lookup"><span data-stu-id="86064-105">To listen on a socket</span></span>

<span data-ttu-id="86064-106">Llame a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , pasando como parámetros el socket creado y un valor para el *trabajo pendiente*, la longitud máxima de la cola de conexiones pendientes que se va a aceptar.</span><span class="sxs-lookup"><span data-stu-id="86064-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="86064-107">En este ejemplo, el parámetro de *trabajo pendiente* se estableció en **SOMAXCONN**.</span><span class="sxs-lookup"><span data-stu-id="86064-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="86064-108">Este valor es una constante especial que indica al proveedor Winsock de este socket que permita un número máximo razonable de conexiones pendientes en la cola.</span><span class="sxs-lookup"><span data-stu-id="86064-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="86064-109">Compruebe si hay errores generales en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="86064-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="86064-110">Siguiente paso: [aceptar una conexión](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="86064-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="86064-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86064-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86064-112">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="86064-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="86064-113">Aplicación Winsock Server</span><span class="sxs-lookup"><span data-stu-id="86064-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="86064-114">Enlazar un socket</span><span class="sxs-lookup"><span data-stu-id="86064-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



