---
description: El establecimiento de una sesión PGM es similar a la rutina de establecimiento de conexión asociada a una sesión TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Receptores y remitentes de PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541518"
---
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="86cb3-103">Receptores y remitentes de PGM</span><span class="sxs-lookup"><span data-stu-id="86cb3-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="86cb3-104">El establecimiento de una sesión PGM es similar a la rutina de establecimiento de conexión asociada a una sesión TCP.</span><span class="sxs-lookup"><span data-stu-id="86cb3-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="86cb3-105">La salida importante de una sesión TCP, sin embargo, es que se invierte la semántica del cliente y del servidor. el servidor (el remitente PGM) se conecta a un grupo de multidifusión, mientras que el cliente (el receptor PGM) espera a aceptar una conexión.</span><span class="sxs-lookup"><span data-stu-id="86cb3-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="86cb3-106">En los párrafos siguientes se detallan los pasos de programación necesarios para crear un remitente PGM y un receptor PGM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="86cb3-107">En esta página también se describen los modos de datos disponibles para las sesiones de PGM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="86cb3-108">Remitente PGM</span><span class="sxs-lookup"><span data-stu-id="86cb3-108">PGM Sender</span></span>

<span data-ttu-id="86cb3-109">**Para crear un remitente PGM, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="86cb3-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="86cb3-110">Cree un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="86cb3-111">[**enlazar**](/windows/desktop/api/winsock/nf-winsock-bind) el socket para la indirección \_ .</span><span class="sxs-lookup"><span data-stu-id="86cb3-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="86cb3-112">[**Conéctese**](/windows/desktop/api/Winsock2/nf-winsock2-connect) a la dirección de transmisión del grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="86cb3-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="86cb3-113">No se realiza ningún protocolo de enlace de sesión formal con ningún cliente.</span><span class="sxs-lookup"><span data-stu-id="86cb3-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="86cb3-114">El proceso de conexión es similar a una [**conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect)UDP, ya que asocia una dirección de extremo (el grupo de multidifusión) con el socket.</span><span class="sxs-lookup"><span data-stu-id="86cb3-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="86cb3-115">Una vez completado, se pueden enviar datos en el socket.</span><span class="sxs-lookup"><span data-stu-id="86cb3-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="86cb3-116">Cuando un remitente crea un socket PGM y lo conecta a una dirección de multidifusión, se crea una sesión PGM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="86cb3-117">Una sesión de multidifusión confiable se define mediante una combinación del identificador único global (GUID) y el puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="86cb3-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="86cb3-118">El transporte genera el GUID.</span><span class="sxs-lookup"><span data-stu-id="86cb3-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="86cb3-119">El transporte especifica el puerto sSource y no se proporciona ningún control sobre el que se utiliza el puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="86cb3-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="86cb3-120">No se permite recibir datos en un socket de remitente y se produce un error.</span><span class="sxs-lookup"><span data-stu-id="86cb3-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="86cb3-121">En el fragmento de código siguiente se muestra cómo configurar un remitente PGM:</span><span class="sxs-lookup"><span data-stu-id="86cb3-121">The following code snippet illustrates setting up a PGM sender:</span></span>


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a><span data-ttu-id="86cb3-122">Receptor PGM</span><span class="sxs-lookup"><span data-stu-id="86cb3-122">PGM Receiver</span></span>

<span data-ttu-id="86cb3-123">**Para crear un receptor PGM, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="86cb3-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="86cb3-124">Cree un socket PGM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="86cb3-125">[**enlazar**](/windows/desktop/api/winsock/nf-winsock-bind) el socket a la dirección del grupo de multidifusión en la que el remitente está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="86cb3-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="86cb3-126">Llame a la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) en el socket para poner el socket en modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="86cb3-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="86cb3-127">La función Listen devuelve cuando se detecta una sesión PGM en la dirección y el puerto del grupo de multidifusión especificado.</span><span class="sxs-lookup"><span data-stu-id="86cb3-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="86cb3-128">Llame a la función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) para obtener un nuevo identificador de socket correspondiente a la sesión.</span><span class="sxs-lookup"><span data-stu-id="86cb3-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="86cb3-129">Solo los datos PGM originales (ODATA) desencadenan la aceptación de una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="86cb3-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="86cb3-130">Como tal, el transporte puede recibir otro tráfico PGM (como paquetes SPM o RDATA), pero no se devuelve la función [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="86cb3-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="86cb3-131">Una vez aceptada una sesión, el identificador de socket devuelto se usa para recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="86cb3-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="86cb3-132">No se permite el envío de datos en un socket de recepción y se produce un error.</span><span class="sxs-lookup"><span data-stu-id="86cb3-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="86cb3-133">En el fragmento de código siguiente se muestra la configuración de un receptor PGM:</span><span class="sxs-lookup"><span data-stu-id="86cb3-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a><span data-ttu-id="86cb3-134">Modos de datos</span><span class="sxs-lookup"><span data-stu-id="86cb3-134">Data Modes</span></span>

<span data-ttu-id="86cb3-135">Las sesiones PGM tienen dos opciones para los modos de datos: modo de mensaje y modo de flujo.</span><span class="sxs-lookup"><span data-stu-id="86cb3-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="86cb3-136">El modo de mensaje es adecuado para las aplicaciones que necesitan enviar mensajes discretos, y se especifica mediante un tipo de socket de SOCK \_ RDM.</span><span class="sxs-lookup"><span data-stu-id="86cb3-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="86cb3-137">El modo de secuencia es adecuado para las aplicaciones que necesitan enviar datos de streaming a receptores, como aplicaciones de vídeo o de voz, y se especifica mediante un tipo de socket de \_ flujo sock.</span><span class="sxs-lookup"><span data-stu-id="86cb3-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="86cb3-138">La elección de modo afecta a la forma en que Winsock procesa los datos.</span><span class="sxs-lookup"><span data-stu-id="86cb3-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="86cb3-139">Considere el ejemplo siguiente: un remitente PGM del modo de mensaje realiza tres llamadas a la función [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , cada una con un búfer de 100 bytes.</span><span class="sxs-lookup"><span data-stu-id="86cb3-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="86cb3-140">Esta operación aparece en la conexión como tres paquetes PGM discretos.</span><span class="sxs-lookup"><span data-stu-id="86cb3-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="86cb3-141">En el lado del receptor, cada llamada a la función [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) devuelve solo 100 bytes, incluso si se proporciona un búfer de recepción mayor.</span><span class="sxs-lookup"><span data-stu-id="86cb3-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="86cb3-142">Por el contrario, con un remitente PGM en modo de transmisión, esas transmisiones de 3 100 bytes podrían fusionarse en menos de tres paquetes físicos en la conexión (o fusionarse en un BLOB de datos en el lado del receptor).</span><span class="sxs-lookup"><span data-stu-id="86cb3-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="86cb3-143">Como tal, cuando el receptor llama a una de las funciones de recepción de Windows Sockets, cualquier cantidad de datos que haya recibido el transporte PGM se puede devolver a la aplicación sin tener en cuenta cómo se han transmitido o recibido físicamente los datos.</span><span class="sxs-lookup"><span data-stu-id="86cb3-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



