---
title: Notificación de congestión explícita (ECN) de Winsock
description: Algunas aplicaciones o protocolos basados en el Protocolo de datagramas de usuario (UDP) (por ejemplo, QUIC) buscan aprovechar el uso de puntos de código de notificación de congestión explícita (ECN) para mejorar la latencia y la vibración en las redes congestión.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110560005"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="3b0e0-103">Notificación de congestión explícita (ECN) de Winsock</span><span class="sxs-lookup"><span data-stu-id="3b0e0-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="3b0e0-104">Introducción</span><span class="sxs-lookup"><span data-stu-id="3b0e0-104">Introduction</span></span>

<span data-ttu-id="3b0e0-105">Algunas aplicaciones o protocolos basados en el Protocolo de datagramas de usuario (UDP) (por ejemplo, QUIC) buscan aprovechar el uso de puntos de código de notificación de congestión explícita (ECN) para mejorar la latencia y la vibración en las redes congestión.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="3b0e0-106">Las API de WINSOCK ECN amplían la interfaz **getsockopt** setsockopt, así como la interfaz de mensaje de /  &mdash; control [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) con compatibilidad para modificar y recibir puntos de código ECN en &mdash; encabezados IP.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="3b0e0-107">La funcionalidad proporcionada permite obtener y establecer puntos de código ECN por paquete.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="3b0e0-108">Para obtener más información sobre ECN, vea [Adición de notificación de congestión explícita (ECN) a ip.](https://tools.ietf.org/html/rfc3168)</span><span class="sxs-lookup"><span data-stu-id="3b0e0-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="3b0e0-109">La aplicación no puede especificar el punto de código Congestión encontrada (CE) al enviar datagramas.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="3b0e0-110">El envío devolverá con el error **WSAEINVAL**.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="3b0e0-111">Consulta de ECN con WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="3b0e0-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="3b0e0-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) es una función insertable, definida en `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="3b0e0-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="3b0e0-113">Llame a **WSAGetRecvIPEcn** para consultar la habilitación actual de recibir el mensaje de control **IP_ECN** (o **IPV6_ECN)** a través [**de LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)</span><span class="sxs-lookup"><span data-stu-id="3b0e0-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="3b0e0-114">Consulte también la [**estructura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)</span><span class="sxs-lookup"><span data-stu-id="3b0e0-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="3b0e0-115">**Protocolo:** IPv4</span><span class="sxs-lookup"><span data-stu-id="3b0e0-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="3b0e0-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="3b0e0-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="3b0e0-117">**Cmsg_type:** IP_ECN (50 decimales)</span><span class="sxs-lookup"><span data-stu-id="3b0e0-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="3b0e0-118">**Descripción:** especifica o recibe el punto de código ECN en el campo de encabezado IPv4 tipo de servicio (TOS).</span><span class="sxs-lookup"><span data-stu-id="3b0e0-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="3b0e0-119">**Protocolo:** IPv6</span><span class="sxs-lookup"><span data-stu-id="3b0e0-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="3b0e0-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="3b0e0-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="3b0e0-121">**Cmsg_type:** IPV6_ECN (50 decimales)</span><span class="sxs-lookup"><span data-stu-id="3b0e0-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="3b0e0-122">**Descripción:** especifica o recibe el punto de código ECN en el campo de encabezado IPv6 de la clase de tráfico.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="3b0e0-123">Especificación de ECN con WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="3b0e0-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="3b0e0-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) es una función insertable, definida en `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="3b0e0-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="3b0e0-125">Llame a **WSASetRecvIPEcn** para especificar si la pila IP debe rellenar el búfer de control con un mensaje que contenga el punto de código ECN del campo de encabezado IPv4 tipo de servicio (o campo de encabezado IPv6 de clase de tráfico) en un datagrama recibido.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="3b0e0-126">Cuando se establece en `TRUE` , [**LPFN_WSARECVMSG función (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve datos de control opcionales que contienen el punto de código ECN del datagrama recibido.</span><span class="sxs-lookup"><span data-stu-id="3b0e0-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="3b0e0-127">El tipo de mensaje de control devuelto **se IP_ECN** (o **IPV6_ECN**) con IPPROTO_IP **nivel** **(o IPPROTO_IPV6**).</span><span class="sxs-lookup"><span data-stu-id="3b0e0-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="3b0e0-128">Los datos del mensaje de control se devuelven como **int.**</span><span class="sxs-lookup"><span data-stu-id="3b0e0-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="3b0e0-129">Esta opción solo es válida en sockets de datagramas (el tipo de socket debe **ser SOCK_DGRAM**).</span><span class="sxs-lookup"><span data-stu-id="3b0e0-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="3b0e0-130">Ejemplo de código 1 &mdash; aplicación que anuncia compatibilidad con ECN</span><span class="sxs-lookup"><span data-stu-id="3b0e0-130">Code example 1&mdash;application advertising ECN support</span></span>

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

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
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="3b0e0-131">Aplicación de ejemplo de código 2 &mdash; que detecta congestión</span><span class="sxs-lookup"><span data-stu-id="3b0e0-131">Code example 2&mdash;application detecting congestion</span></span>

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a><span data-ttu-id="3b0e0-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3b0e0-132">See also</span></span>

* [<span data-ttu-id="3b0e0-133">WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="3b0e0-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="3b0e0-134">WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="3b0e0-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
