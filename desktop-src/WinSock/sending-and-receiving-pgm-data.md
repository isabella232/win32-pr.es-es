---
description: El envío y la recepción de datos PGM es similar al envío o la recepción de datos en cualquier socket. Hay consideraciones específicas para PGM, que se describen en los párrafos siguientes.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Envío y recepción de datos PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156013"
---
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="89cc5-104">Envío y recepción de datos PGM</span><span class="sxs-lookup"><span data-stu-id="89cc5-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="89cc5-105">El envío y la recepción de datos PGM es similar al envío o la recepción de datos en cualquier socket.</span><span class="sxs-lookup"><span data-stu-id="89cc5-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="89cc5-106">Hay consideraciones específicas para PGM, que se describen en los párrafos siguientes.</span><span class="sxs-lookup"><span data-stu-id="89cc5-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="89cc5-107">Envío de datos PGM</span><span class="sxs-lookup"><span data-stu-id="89cc5-107">Sending PGM Data</span></span>

<span data-ttu-id="89cc5-108">Una vez que se crea una sesión de remitente PGM, los datos se envían mediante las distintas funciones de envío de Windows Sockets: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)y [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="89cc5-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="89cc5-109">Como los identificadores de Windows Sockets son identificadores del sistema de archivos, otras funciones como las funciones [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) y CRT también pueden transmitir datos.</span><span class="sxs-lookup"><span data-stu-id="89cc5-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="89cc5-110">En el fragmento de código siguiente se muestra una operación de remitente PGM:</span><span class="sxs-lookup"><span data-stu-id="89cc5-110">The following code snippet illustrates a PGM sender operation:</span></span>


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



<span data-ttu-id="89cc5-111">Cuando se usa el modo de mensaje (SOCK \_ RDM), cada llamada a una función Send da como resultado un mensaje discreto, que a veces no es deseable; una aplicación puede querer enviar un mensaje de 2 megabytes con varias llamadas a [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span><span class="sxs-lookup"><span data-stu-id="89cc5-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="89cc5-112">En tales circunstancias, el remitente puede establecer la opción [RM \_ set \_ Message \_ BOUNDARY](socket-options.md) socket para indicar el tamaño del mensaje que se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="89cc5-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="89cc5-113">Si la ventana de envío está llena, no se aceptará un nuevo envío desde la aplicación hasta que se haya avanzado la ventana.</span><span class="sxs-lookup"><span data-stu-id="89cc5-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="89cc5-114">Se produce un error al intentar enviar un socket que no es de bloqueo con WSAEWOULDBLOCK; un socket de bloqueo simplemente se bloquea hasta que la ventana avanza hasta el punto en el que los datos solicitados se pueden almacenar en búfer y enviar.</span><span class="sxs-lookup"><span data-stu-id="89cc5-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="89cc5-115">En e/s superpuestas, la operación no se completa hasta que la ventana avanza lo suficiente para alojar los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="89cc5-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="89cc5-116">Recibir datos PGM</span><span class="sxs-lookup"><span data-stu-id="89cc5-116">Receiving PGM Data</span></span>

<span data-ttu-id="89cc5-117">Una vez creada la sesión del receptor PGM, se reciben los datos mediante las distintas funciones de recepción de Windows Sockets: [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)y [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="89cc5-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="89cc5-118">Como los identificadores de Windows Sockets también son identificadores de archivo, las funciones [**readfile**](/windows/win32/api/fileapi/nf-fileapi-readfile) y CRT también se pueden usar para recibir datos de sesión PGM.</span><span class="sxs-lookup"><span data-stu-id="89cc5-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="89cc5-119">El transporte reenvía los datos al receptor a medida que llegan, siempre y cuando los datos estén en secuencia.</span><span class="sxs-lookup"><span data-stu-id="89cc5-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="89cc5-120">El transporte garantiza que los datos devueltos son contiguos y están libres de duplicados.</span><span class="sxs-lookup"><span data-stu-id="89cc5-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="89cc5-121">En el fragmento de código siguiente se muestra una operación de recepción PGM:</span><span class="sxs-lookup"><span data-stu-id="89cc5-121">The following code snippet illustrates a PGM receive operation:</span></span>


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



<span data-ttu-id="89cc5-122">Al usar el modo de mensaje (SOCK \_ RDM), el transporte indica cuándo se recibe un mensaje parcial, bien con el error WSAEMSGSIZE, o bien estableciendo la \_ marca parcial MSG al volver de las funciones [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) y [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="89cc5-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="89cc5-123">Cuando el último fragmento del mensaje completo se devuelve al cliente, no se indica el error o la marca.</span><span class="sxs-lookup"><span data-stu-id="89cc5-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="89cc5-124">Cuando la sesión finaliza correctamente, se produce un error en la operación de recepción con WSAEDISCON.</span><span class="sxs-lookup"><span data-stu-id="89cc5-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="89cc5-125">Cuando se produce la pérdida de datos en el transporte, PGM almacena temporalmente en búfer los paquetes fuera de secuencia e intenta recuperar los datos perdidos.</span><span class="sxs-lookup"><span data-stu-id="89cc5-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="89cc5-126">Si la pérdida de datos es irrecuperable, se produce un error en la operación de recepción con WSAECONNRESET y se termina la sesión.</span><span class="sxs-lookup"><span data-stu-id="89cc5-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="89cc5-127">La sesión se puede restablecer debido a diversas condiciones, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="89cc5-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="89cc5-128">El receptor o la velocidad de conexión entrante es demasiado lento para mantenerse al ritmo de la velocidad de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="89cc5-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="89cc5-129">Se produce una pérdida de datos excesiva, posiblemente debido a condiciones de red transitorias, como problemas de enrutamiento, inestabilidad de red, etc.</span><span class="sxs-lookup"><span data-stu-id="89cc5-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="89cc5-130">Se produce un error irrecuperable en el remitente.</span><span class="sxs-lookup"><span data-stu-id="89cc5-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="89cc5-131">Se produce un uso excesivo de los recursos en el equipo local, por ejemplo, si se supera el almacenamiento de búfer interno máximo permitido o si se encuentra una condición de recursos insuficientes.</span><span class="sxs-lookup"><span data-stu-id="89cc5-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="89cc5-132">Se produce un error de comprobación de coherencia de datos.</span><span class="sxs-lookup"><span data-stu-id="89cc5-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="89cc5-133">Un error en un componente PGM depende de, como TCP/IP o Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="89cc5-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="89cc5-134">Tanto el primer como el segundo elemento de la lista anterior pueden dar lugar a que el receptor realice un almacenamiento en búfer excesivo antes de quedarse sin recursos o antes de moverse más allá de la ventana del remitente.</span><span class="sxs-lookup"><span data-stu-id="89cc5-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="89cc5-135">Finalizar una sesión PGM</span><span class="sxs-lookup"><span data-stu-id="89cc5-135">Terminating A PGM Session</span></span>

<span data-ttu-id="89cc5-136">El remitente o receptor PGM puede detener el envío o la recepción de datos llamando a [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span><span class="sxs-lookup"><span data-stu-id="89cc5-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="89cc5-137">El receptor debe llamar a **closesocket** en los sockets de escucha y recepción para evitar pérdidas de identificadores.</span><span class="sxs-lookup"><span data-stu-id="89cc5-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="89cc5-138">Llamar a [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) en el remitente antes de llamar a **closesocket** garantiza que se envíen todos los datos y garantiza que los datos de reparación se mantengan hasta que la ventana de envío avance más allá de la última secuencia de datos, incluso si la propia aplicación finaliza.</span><span class="sxs-lookup"><span data-stu-id="89cc5-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
