---
title: Notificación de congestión explícita (ECN) de Winsock
description: Algunas aplicaciones o protocolos basados en el Protocolo de datagramas de usuario (UDP) (por ejemplo, QUIC) buscan aprovechar el uso de puntos de código de notificación de congestión explícita (ECN) para mejorar la latencia y la vibración en las redes congestión.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 79b38611cd0301d0b5d301592eec02b68c02353246c67a6c94528417623834f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322028"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Notificación de congestión explícita (ECN) de Winsock

## <a name="introduction"></a>Introducción

Algunas aplicaciones o protocolos basados en el Protocolo de datagramas de usuario (UDP) (por ejemplo, QUIC) buscan aprovechar el uso de puntos de código de notificación de congestión explícita (ECN) para mejorar la latencia y la vibración en las redes congestión.

Las API de WINSOCK ECN extienden la interfaz de mensajes de control **getsockopt** setsockopt, así como la interfaz de mensaje de /  &mdash; control [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) con compatibilidad para modificar y recibir puntos de código ECN en &mdash; encabezados IP. La funcionalidad proporcionada permite obtener y establecer puntos de código ECN por paquete.

Para obtener más información sobre ECN, vea [Adición de notificación de congestión explícita (ECN) a IP.](https://tools.ietf.org/html/rfc3168)

La aplicación no puede especificar el punto de código Congestión encontrada (CE) al enviar datagramas. El envío devolverá el error **WSAEINVAL.**

## <a name="query-ecn-with-wsagetrecvipecn"></a>Consulta de ECN con WSAGetRecvIPEcn

[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) es una función insertable, definida en `ws2tcpip.h` .

Llame a **WSAGetRecvIPEcn** para consultar la habilitación actual de recibir el mensaje de control **IP_ECN** (o **IPV6_ECN)** a través [**de LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

Consulte también la [**estructura WSAMSG.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)

- **Protocolo:** IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type:** IP_ECN (50 decimales)
- **Descripción:** especifica o recibe el punto de código ECN en el campo de encabezado IPv4 tipo de servicio (TOS).

- **Protocolo:** IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type:** IPV6_ECN (50 decimales)
- **Descripción:** especifica o recibe el punto de código ECN en el campo de encabezado IPv6 de la clase de tráfico.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Especificar ECN con WSASetRecvIPEcn

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) es una función insertable, definida en `ws2tcpip.h` .

Llame a **WSASetRecvIPEcn** para especificar si la pila IP debe rellenar el búfer de control con un mensaje que contenga el punto de código ECN del campo de encabezado IPv4 tipo de servicio (o campo de encabezado IPv6 de clase de tráfico) en un datagrama recibido. Cuando se establece en `TRUE` , [**LPFN_WSARECVMSG función (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) devuelve datos de control opcionales que contienen el punto de código ECN del datagrama recibido. El tipo de mensaje de control devuelto **se IP_ECN** **(o IPV6_ECN**) con IPPROTO_IP nivel **(o IPPROTO_IPV6**).  Los datos del mensaje de control se devuelven como **int.** Esta opción solo es válida en sockets de datagramas (el tipo de socket debe **ser SOCK_DGRAM**).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Ejemplo de código 1 &mdash; aplicación que anuncia compatibilidad con ECN

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Aplicación de ejemplo de código 2 &mdash; que detecta congestión

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

## <a name="see-also"></a>Consulte también

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
