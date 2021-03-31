---
description: Compatibilidad con IPv6, anexo de TCP/IP y Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Compatibilidad con IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154271"
---
# <a name="ipv6-support"></a>Compatibilidad con IPv6

Con el fin de admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, un socket para su uso con IPv4 y un socket para su uso con IPv6. La aplicación debe controlar estos dos sockets por separado.

Si un proveedor de servicios TCP/IP en Windows XP con SP1 y en Windows Server 2003 admite el direccionamiento IPv4 e IPv6, debe crear dos sockets independientes y escuchar por separado en estos Sockets:

-   Una vez para IPv4.
-   Una vez para la familia de direcciones IPv6.

Windows Vista y versiones posteriores ofrecen la posibilidad de crear un socket IPv6 único que pueda controlar el tráfico IPv6 e IPv4. Por ejemplo, se crea un socket de escucha TCP para IPv6, se coloca en modo de pila doble y se enlaza al puerto 5001. Este socket de doble pila puede aceptar conexiones de clientes TCP IPv6 que se conectan al puerto 5001 y desde clientes TCP IPv4 que se conectan al puerto 5001. Esta característica permite un diseño de aplicaciones enormemente simplificado y reduce la sobrecarga de recursos necesaria para las operaciones de publicación en dos sockets independientes. Sin embargo, hay algunas restricciones que deben cumplirse para poder usar un socket de doble pila. Para obtener más información, consulte [sockets de dos pilas](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) devuelve dos estructuras de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada uno de los tipos de socket admitidos ( \_ Stream sock, sock \_ DGRAM, sock \_ raw). **IAddressFamily** debe establecerse en AF \_ inet para direccionamiento IPv4 y en AF \_ inet6 para direccionamiento IPv6.

Las direcciones IPv6 se describen en las siguientes estructuras.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

Si una aplicación usa funciones de Windows Sockets 1,1 y desea usar direcciones IPv6, puede seguir usando todas las funciones antiguas que toman la estructura [**sockaddr**](sockaddr-2.md) como uno de los parámetros ([**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)y [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), etc.). El único cambio necesario es usar **sockaddr \_ IN6** en lugar de **sockaddr \_ en**.

Sin embargo, las funciones de resolución de nombres ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), etc.) y las funciones de conversión de direcciones ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) no se pueden reutilizar porque suponen que una dirección IP tiene una longitud de 4 bytes. Una aplicación que desea realizar la resolución de nombres y la conversión de direcciones para direcciones IPv6 debe usar funciones específicas de Windows Sockets 2. Se han incorporado muchas funciones nuevas para permitir que las aplicaciones de Windows Sockets 2 aprovechen IPv6, incluidas las funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Para obtener más información sobre cómo habilitar las funcionalidades de IPv6 en una aplicación, consulte la [Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
