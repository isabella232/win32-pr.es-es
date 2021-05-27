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
# <a name="winsock-timestamping"></a>Marca de tiempo de Winsock

## <a name="introduction"></a>Introducción

Las marcas de tiempo de paquetes son una característica fundamental para muchas aplicaciones de sincronización de &mdash; reloj, por ejemplo, el Protocolo de tiempo de precisión. Cuanto más se acerque la generación de marca de tiempo a cuando el hardware del adaptador de red recibe o envía un paquete, más precisa puede ser la aplicación de sincronización.

Por lo tanto, las API de marca de tiempo descritas en este tema proporcionan a la aplicación un mecanismo para notificar las marcas de tiempo que se generan muy por debajo del nivel de aplicación. En concreto, una marca de tiempo de software en la interfaz entre el minipuerto y NDIS, y una marca de tiempo de hardware en el hardware NIC. La API de marca de tiempo puede mejorar en gran medida la precisión de la sincronización del reloj. Actualmente, la compatibilidad está en el ámbito de los sockets del Protocolo de datagramas de usuario (UDP).

## <a name="receive-timestamps"></a>Marcas de tiempo de recepción

Configure la recepción de marca de tiempo de recepción a [**través SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Use esa IOCTL para habilitar la recepción de la marca de tiempo de recepción. Cuando recibe un datagrama mediante la función [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su marca de tiempo (si está disponible) se encuentra en el mensaje SO_TIMESTAMP **control.**

**SO_TIMESTAMP** (0x300A) se define en `mstcpip.h` . Los datos del mensaje de control se devuelven como **UINT64.**

## <a name="transmit-timestamps"></a>Transmisión de marcas de tiempo

La recepción de la marca de tiempo de transmisión también [**se configura a través SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Use esa IOCTL para habilitar la recepción de marca de tiempo de transmisión y especifique el número de marcas de tiempo de transmisión que el sistema almacenará en búfer. A medida que se generan marcas de tiempo de transmisión, se agregan al búfer. Si el búfer está lleno, se descartan las nuevas marcas de tiempo de transmisión.

Al enviar un datagrama, asocie el datagrama con un **SO_TIMESTAMP_ID** de control. Debe contener un identificador único. Envíe el datagrama, junto con su **mensaje SO_TIMESTAMP_ID** control, mediante [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg). Es posible que las marcas de tiempo de transmisión no estén disponibles inmediatamente después **de que WSASendMsg devuelva** . A medida que las marcas de tiempo de transmisión están disponibles, se colocan en un búfer por socket. Use la [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL para sondear la marca de tiempo por su identificador. Si la marca de tiempo está disponible, se quita del búfer y se devuelve. Si la marca de tiempo no está disponible, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) devuelve **WSAEWOULDBLOCK**. Si se genera una marca de tiempo de transmisión mientras el búfer está lleno, se descarta la nueva marca de tiempo.

**SO_TIMESTAMP_ID** (0x300B) se define en `mstcpip.h` . Debe proporcionar los datos del mensaje de control como **UINT32**.

Las marcas de tiempo se representan como un valor de contador de 64 bits. La frecuencia del contador depende del origen de la marca de tiempo. Para las marcas de tiempo de software, el contador es un valor [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) y puede determinar su frecuencia a través de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency). En el caso de las marcas de tiempo de hardware nic, la frecuencia del contador depende del hardware nic y se puede determinar con información adicional que proporciona [**CaptureInterfaceHardwareCrossTimestamp.**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp) Para determinar el origen de las marcas de tiempo, use las funciones [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) y [**GetInterfaceSupportedTimestampCapabilities.**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities)

Además de la configuración de nivel de socket mediante [**la opción SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket para habilitar la recepción de marca de tiempo para un socket, también se necesita la configuración de nivel de sistema.

## <a name="estimating-latency-of-socket-send-path"></a>Estimación de la latencia de la ruta de acceso de envío del socket

En esta sección, usaremos marcas de tiempo de transmisión para calcular la latencia de la ruta de acceso de envío del socket. Si tiene una aplicación existente que consume marcas de tiempo de E/S de nivel de aplicación donde la marca de tiempo debe estar lo más cerca posible del punto de transmisión real, este ejemplo proporciona una descripción cuantitativa de la cantidad de API de marca de tiempo de Winsock que puede mejorar la precisión de &mdash; &mdash; la aplicación.

En el ejemplo se supone que solo hay una tarjeta de interfaz de red (NIC) en el sistema y que *interfaceLuid* es el LUID de ese adaptador.

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

## <a name="estimating-latency-of-socket-receive-path"></a>Estimación de la latencia de la ruta de acceso de recepción del socket

Este es un ejemplo similar para la ruta de acceso de recepción. En el ejemplo se supone que solo hay una tarjeta de interfaz de red (NIC) en el sistema y que *interfaceLuid* es el LUID de ese adaptador.

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

## <a name="a-limitation"></a>Una limitación

Una limitación de las API de marca de tiempo de Winsock es que llamar a [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) es siempre una operación sin bloqueo. Incluso llamar a la IOCTL de forma OVERLAPPED da como resultado una devolución inmediata de **WSACTLCTLDBLOCK** si actualmente no hay marcas de tiempo de transmisión disponibles. Puesto que es posible que las marcas de tiempo de transmisión no estén disponibles inmediatamente después de que [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) vuelva, la aplicación debe sondear la IOCTL hasta que la marca de tiempo esté disponible. Se garantiza que una marca de tiempo de transmisión esté disponible después de una llamada correcta a **WSASendMsg,** dado que el búfer de marca de tiempo de transmisión no está lleno.
