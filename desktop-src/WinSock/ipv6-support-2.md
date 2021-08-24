---
description: Compatibilidad con IPv6, anexo TCP/IP y Windows sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Compatibilidad con IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f48e5b46ef1fcf1a2257db4a04b5435443552bb49f6c3c2b2dc4784077dcbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794805"
---
# <a name="ipv6-support"></a>Compatibilidad con IPv6

Para admitir tanto IPv4 como IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, uno para su uso con IPv4 y otro para su uso con IPv6. La aplicación debe controlar estos dos sockets por separado.

Si un proveedor de servicios TCP/IP en Windows XP con SP1 y en Windows Server 2003 admite el direccionamiento IPv4 e IPv6, debe crear dos sockets independientes y escuchar por separado en estos sockets:

-   Una vez para IPv4.
-   Una vez para la familia de direcciones IPv6.

Windows Vista y versiones posteriores ofrecen la posibilidad de crear un único socket IPv6 que pueda controlar el tráfico IPv6 e IPv4. Por ejemplo, se crea un socket de escucha TCP para IPv6, se coloca en modo de pila dual y se enlaza al puerto 5001. Este socket de pila doble puede aceptar conexiones de clientes TCP IPv6 que se conectan al puerto 5001 y de clientes TCP IPv4 que se conectan al puerto 5001. Esta característica permite un diseño de aplicaciones muy simplificado y reduce la sobrecarga de recursos necesaria para publicar operaciones en dos sockets independientes. Sin embargo, hay algunas restricciones que deben cumplirse para poder usar un socket de pila doble. Para obtener más información, [vea Sockets de pila dual.](dual-stack-sockets.md)

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) devuelve dos estructuras INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada uno de los tipos de socket admitidos (SOCK \_ STREAM, SOCK \_ DGRAM y SOCK \_ RAW). **iAddressFamily** debe establecerse en AF INET para el direccionamiento \_ IPv4 y en AF INET6 para el \_ direccionamiento IPv6.

Las direcciones IPv6 se describen en las estructuras siguientes.

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

Si una aplicación usa funciones Windows Sockets 1.1 y desea usar direcciones IPv6, puede seguir usando todas las funciones antiguas que toman [](/windows/desktop/api/winsock/nf-winsock-sendto)la estructura [**sockaddr**](sockaddr-2.md) como uno de los parámetros [**(enlazar,**](/windows/desktop/api/winsock/nf-winsock-bind) [**conectar,**](/windows/desktop/api/Winsock2/nf-winsock2-connect)enviar y volver [**acvfrom,**](/windows/desktop/api/winsock/nf-winsock-recvfrom) [**aceptar,**](/windows/desktop/api/Winsock2/nf-winsock2-accept)etc.). El único cambio necesario es usar **sockaddr \_ en6** en lugar **de sockaddr \_ en**.

Sin embargo, las funciones de resolución de nombres [**(gethostbyname,**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) [**gethostbyaddr,**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)etc.) y las funciones de conversión de direcciones ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) no se pueden reutilizar porque suponen que una dirección IP tiene una longitud de 4 bytes. Una aplicación que quiera realizar la resolución de nombres y la conversión de direcciones para direcciones IPv6 debe usar Windows sockets 2 específicos. Se han introducido muchas funciones nuevas para permitir que las aplicaciones Windows Sockets 2 aprovechen las ventajas de IPv6, incluidas las funciones [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) [**y getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

Para obtener más información sobre cómo habilitar las funcionalidades de IPv6 en una aplicación, consulte la Guía [de IPv6 para Windows sockets de aplicaciones](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
