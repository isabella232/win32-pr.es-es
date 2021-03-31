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
# <a name="ipv6-support"></a><span data-ttu-id="97fc0-103">Compatibilidad con IPv6</span><span class="sxs-lookup"><span data-stu-id="97fc0-103">IPv6 Support</span></span>

<span data-ttu-id="97fc0-104">Con el fin de admitir IPv4 e IPv6 en Windows XP con Service Pack 1 (SP1) y en Windows Server 2003, una aplicación tiene que crear dos sockets, un socket para su uso con IPv4 y un socket para su uso con IPv6.</span><span class="sxs-lookup"><span data-stu-id="97fc0-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="97fc0-105">La aplicación debe controlar estos dos sockets por separado.</span><span class="sxs-lookup"><span data-stu-id="97fc0-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="97fc0-106">Si un proveedor de servicios TCP/IP en Windows XP con SP1 y en Windows Server 2003 admite el direccionamiento IPv4 e IPv6, debe crear dos sockets independientes y escuchar por separado en estos Sockets:</span><span class="sxs-lookup"><span data-stu-id="97fc0-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="97fc0-107">Una vez para IPv4.</span><span class="sxs-lookup"><span data-stu-id="97fc0-107">Once for IPv4.</span></span>
-   <span data-ttu-id="97fc0-108">Una vez para la familia de direcciones IPv6.</span><span class="sxs-lookup"><span data-stu-id="97fc0-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="97fc0-109">Windows Vista y versiones posteriores ofrecen la posibilidad de crear un socket IPv6 único que pueda controlar el tráfico IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="97fc0-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="97fc0-110">Por ejemplo, se crea un socket de escucha TCP para IPv6, se coloca en modo de pila doble y se enlaza al puerto 5001.</span><span class="sxs-lookup"><span data-stu-id="97fc0-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="97fc0-111">Este socket de doble pila puede aceptar conexiones de clientes TCP IPv6 que se conectan al puerto 5001 y desde clientes TCP IPv4 que se conectan al puerto 5001.</span><span class="sxs-lookup"><span data-stu-id="97fc0-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="97fc0-112">Esta característica permite un diseño de aplicaciones enormemente simplificado y reduce la sobrecarga de recursos necesaria para las operaciones de publicación en dos sockets independientes.</span><span class="sxs-lookup"><span data-stu-id="97fc0-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="97fc0-113">Sin embargo, hay algunas restricciones que deben cumplirse para poder usar un socket de doble pila.</span><span class="sxs-lookup"><span data-stu-id="97fc0-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="97fc0-114">Para obtener más información, consulte [sockets de dos pilas](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="97fc0-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="97fc0-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) devuelve dos estructuras de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para cada uno de los tipos de socket admitidos ( \_ Stream sock, sock \_ DGRAM, sock \_ raw).</span><span class="sxs-lookup"><span data-stu-id="97fc0-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="97fc0-116">**IAddressFamily** debe establecerse en AF \_ inet para direccionamiento IPv4 y en AF \_ inet6 para direccionamiento IPv6.</span><span class="sxs-lookup"><span data-stu-id="97fc0-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="97fc0-117">Las direcciones IPv6 se describen en las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="97fc0-117">The IPv6 addresses are described in the following structures.</span></span>

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

<span data-ttu-id="97fc0-118">Si una aplicación usa funciones de Windows Sockets 1,1 y desea usar direcciones IPv6, puede seguir usando todas las funciones antiguas que toman la estructura [**sockaddr**](sockaddr-2.md) como uno de los parámetros ([**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)y [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), etc.).</span><span class="sxs-lookup"><span data-stu-id="97fc0-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="97fc0-119">El único cambio necesario es usar **sockaddr \_ IN6** en lugar de **sockaddr \_ en**.</span><span class="sxs-lookup"><span data-stu-id="97fc0-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="97fc0-120">Sin embargo, las funciones de resolución de nombres ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), etc.) y las funciones de conversión de direcciones ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) no se pueden reutilizar porque suponen que una dirección IP tiene una longitud de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="97fc0-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="97fc0-121">Una aplicación que desea realizar la resolución de nombres y la conversión de direcciones para direcciones IPv6 debe usar funciones específicas de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="97fc0-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="97fc0-122">Se han incorporado muchas funciones nuevas para permitir que las aplicaciones de Windows Sockets 2 aprovechen IPv6, incluidas las funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="97fc0-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="97fc0-123">Para obtener más información sobre cómo habilitar las funcionalidades de IPv6 en una aplicación, consulte la [Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="97fc0-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
