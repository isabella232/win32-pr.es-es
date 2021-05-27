---
title: Marca de tiempo de Winsock
description: Las marcas de tiempo de paquetes son una característica fundamental para muchas aplicaciones de sincronización de &mdash; reloj, por ejemplo, el Protocolo de tiempo de precisión. Cuanto más se acerque la generación de marca de tiempo a cuando el hardware del adaptador de red recibe o envía un paquete, más precisa puede ser la aplicación de sincronización.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559990"
---
# <a name="winsock-timestamping"></a><span data-ttu-id="e44eb-104">Marca de tiempo de Winsock</span><span class="sxs-lookup"><span data-stu-id="e44eb-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="e44eb-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="e44eb-105">Introduction</span></span>

<span data-ttu-id="e44eb-106">Las marcas de tiempo de paquetes son una característica fundamental para muchas aplicaciones de sincronización de &mdash; reloj, por ejemplo, el Protocolo de tiempo de precisión.</span><span class="sxs-lookup"><span data-stu-id="e44eb-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="e44eb-107">Cuanto más se acerque la generación de marca de tiempo a cuando el hardware del adaptador de red recibe o envía un paquete, más precisa puede ser la aplicación de sincronización.</span><span class="sxs-lookup"><span data-stu-id="e44eb-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="e44eb-108">Por lo tanto, las API de marca de tiempo descritas en este tema proporcionan a la aplicación un mecanismo para notificar las marcas de tiempo que se generan muy por debajo del nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="e44eb-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="e44eb-109">En concreto, una marca de tiempo de software en la interfaz entre el minipuerto y NDIS, y una marca de tiempo de hardware en el hardware NIC.</span><span class="sxs-lookup"><span data-stu-id="e44eb-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="e44eb-110">La API de marca de tiempo puede mejorar en gran medida la precisión de la sincronización del reloj.</span><span class="sxs-lookup"><span data-stu-id="e44eb-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="e44eb-111">Actualmente, la compatibilidad está en el ámbito de los sockets del Protocolo de datagramas de usuario (UDP).</span><span class="sxs-lookup"><span data-stu-id="e44eb-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="e44eb-112">Marcas de tiempo de recepción</span><span class="sxs-lookup"><span data-stu-id="e44eb-112">Receive timestamps</span></span>

<span data-ttu-id="e44eb-113">Configure la recepción de marca de tiempo de recepción a [**través SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e44eb-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="e44eb-114">Use esa IOCTL para habilitar la recepción de la marca de tiempo de recepción.</span><span class="sxs-lookup"><span data-stu-id="e44eb-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="e44eb-115">Cuando recibe un datagrama mediante la función [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su marca de tiempo (si está disponible) se encuentra en el mensaje SO_TIMESTAMP **control.**</span><span class="sxs-lookup"><span data-stu-id="e44eb-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="e44eb-116">**SO_TIMESTAMP** (0x300A) se define en `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="e44eb-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="e44eb-117">Los datos del mensaje de control se devuelven como **UINT64.**</span><span class="sxs-lookup"><span data-stu-id="e44eb-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="e44eb-118">Transmisión de marcas de tiempo</span><span class="sxs-lookup"><span data-stu-id="e44eb-118">Transmit timestamps</span></span>

<span data-ttu-id="e44eb-119">La recepción de la marca de tiempo de transmisión también [**se configura a través SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e44eb-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="e44eb-120">Use esa IOCTL para habilitar la recepción de marca de tiempo de transmisión y especifique el número de marcas de tiempo de transmisión que el sistema almacenará en búfer.</span><span class="sxs-lookup"><span data-stu-id="e44eb-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="e44eb-121">A medida que se generan marcas de tiempo de transmisión, se agregan al búfer.</span><span class="sxs-lookup"><span data-stu-id="e44eb-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="e44eb-122">Si el búfer está lleno, se descartan las nuevas marcas de tiempo de transmisión.</span><span class="sxs-lookup"><span data-stu-id="e44eb-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="e44eb-123">Al enviar un datagrama, asocie el datagrama con un **SO_TIMESTAMP_ID** de control.</span><span class="sxs-lookup"><span data-stu-id="e44eb-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="e44eb-124">Debe contener un identificador único.</span><span class="sxs-lookup"><span data-stu-id="e44eb-124">This should contain a unique identifier.</span></span> <span data-ttu-id="e44eb-125">Envíe el datagrama, junto con su **mensaje SO_TIMESTAMP_ID** control, mediante [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span><span class="sxs-lookup"><span data-stu-id="e44eb-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="e44eb-126">Es posible que las marcas de tiempo de transmisión no estén disponibles inmediatamente después **de que WSASendMsg devuelva** .</span><span class="sxs-lookup"><span data-stu-id="e44eb-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="e44eb-127">A medida que las marcas de tiempo de transmisión están disponibles, se colocan en un búfer por socket.</span><span class="sxs-lookup"><span data-stu-id="e44eb-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="e44eb-128">Use la [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL para sondear la marca de tiempo por su identificador.</span><span class="sxs-lookup"><span data-stu-id="e44eb-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="e44eb-129">Si la marca de tiempo está disponible, se quita del búfer y se devuelve.</span><span class="sxs-lookup"><span data-stu-id="e44eb-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="e44eb-130">Si la marca de tiempo no está disponible, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) devuelve **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="e44eb-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="e44eb-131">Si se genera una marca de tiempo de transmisión mientras el búfer está lleno, se descarta la nueva marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e44eb-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="e44eb-132">**SO_TIMESTAMP_ID** (0x300B) se define en `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="e44eb-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="e44eb-133">Debe proporcionar los datos del mensaje de control como **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="e44eb-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="e44eb-134">Las marcas de tiempo se representan como un valor de contador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e44eb-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="e44eb-135">La frecuencia del contador depende del origen de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e44eb-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="e44eb-136">Para las marcas de tiempo de software, el contador es un valor [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) y puede determinar su frecuencia a través de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span><span class="sxs-lookup"><span data-stu-id="e44eb-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="e44eb-137">En el caso de las marcas de tiempo de hardware nic, la frecuencia del contador depende del hardware nic y se puede determinar con información adicional que proporciona [**CaptureInterfaceHardwareCrossTimestamp.**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp)</span><span class="sxs-lookup"><span data-stu-id="e44eb-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="e44eb-138">Para determinar el origen de las marcas de tiempo, use las funciones [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) y [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)</span><span class="sxs-lookup"><span data-stu-id="e44eb-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="e44eb-139">Además de la configuración de nivel de socket mediante [**la opción SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket para habilitar la recepción de marca de tiempo para un socket, también se necesita la configuración de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="e44eb-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="e44eb-140">Estimación de la latencia de la ruta de acceso de envío del socket</span><span class="sxs-lookup"><span data-stu-id="e44eb-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="e44eb-141">En esta sección, usaremos marcas de tiempo de transmisión para calcular la latencia de la ruta de acceso de envío del socket.</span><span class="sxs-lookup"><span data-stu-id="e44eb-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="e44eb-142">Si tiene una aplicación existente que consume marcas de tiempo de E/S de nivel de aplicación donde la marca de tiempo debe estar lo más cerca posible del punto de transmisión real, este ejemplo proporciona una descripción cuantitativa de la cantidad de API de marca de tiempo de Winsock que puede mejorar la precisión de &mdash; &mdash; la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e44eb-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="e44eb-143">En el ejemplo se supone que solo hay una tarjeta de interfaz de red (NIC) en el sistema y que *interfaceLuid* es el LUID de ese adaptador.</span><span class="sxs-lookup"><span data-stu-id="e44eb-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="e44eb-144">Estimación de la latencia de la ruta de acceso de recepción del socket</span><span class="sxs-lookup"><span data-stu-id="e44eb-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="e44eb-145">Este es un ejemplo similar para la ruta de acceso de recepción.</span><span class="sxs-lookup"><span data-stu-id="e44eb-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="e44eb-146">En el ejemplo se supone que solo hay una tarjeta de interfaz de red (NIC) en el sistema y que *interfaceLuid* es el LUID de ese adaptador.</span><span class="sxs-lookup"><span data-stu-id="e44eb-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a><span data-ttu-id="e44eb-147">Una limitación</span><span class="sxs-lookup"><span data-stu-id="e44eb-147">A limitation</span></span>

<span data-ttu-id="e44eb-148">Una limitación de las API de marca de tiempo de Winsock es que llamar a [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) es siempre una operación sin bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e44eb-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="e44eb-149">Incluso llamar a la IOCTL de forma OVERLAPPED da como resultado una devolución inmediata de **WSACTLCTLDBLOCK** si actualmente no hay marcas de tiempo de transmisión disponibles.</span><span class="sxs-lookup"><span data-stu-id="e44eb-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="e44eb-150">Puesto que es posible que las marcas de tiempo de transmisión no estén disponibles inmediatamente después de que [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) vuelva, la aplicación debe sondear la IOCTL hasta que la marca de tiempo esté disponible.</span><span class="sxs-lookup"><span data-stu-id="e44eb-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="e44eb-151">Se garantiza que una marca de tiempo de transmisión esté disponible después de una llamada correcta a **WSASendMsg,** dado que el búfer de marca de tiempo de transmisión no está lleno.</span><span class="sxs-lookup"><span data-stu-id="e44eb-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
