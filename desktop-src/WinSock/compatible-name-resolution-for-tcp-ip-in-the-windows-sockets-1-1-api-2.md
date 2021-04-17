---
description: Tenga en cuenta que todas las funciones de Windows Sockets 1,1 para la resolución de nombres son específicas de las redes TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696397"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="214c6-103">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="214c6-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="214c6-104">Todas las funciones de Windows Sockets 1,1 para la resolución de nombres son específicas de las redes TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="214c6-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="214c6-105">No se recomienda a los desarrolladores de aplicaciones seguir usando estas funciones específicas del transporte que solo admiten IPv4.</span><span class="sxs-lookup"><span data-stu-id="214c6-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="214c6-106">Los desarrolladores de aplicaciones deben usar las siguientes funciones que son independientes del protocolo y admiten la resolución de nombres IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="214c6-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="214c6-107">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="214c6-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="214c6-108">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="214c6-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="214c6-109">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="214c6-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="214c6-110">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="214c6-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="214c6-111">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="214c6-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="214c6-112">Windows Sockets 1,1 definía un número de rutinas que se usan para la resolución de nombres con redes TCP/IP (IP versión 4).</span><span class="sxs-lookup"><span data-stu-id="214c6-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="214c6-113">A veces se denominan funciones **getXbyY** e incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="214c6-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="214c6-114">**GetHostName (**</span><span class="sxs-lookup"><span data-stu-id="214c6-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="214c6-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="214c6-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="214c6-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="214c6-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="214c6-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="214c6-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="214c6-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="214c6-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="214c6-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="214c6-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="214c6-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="214c6-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="214c6-121">También se definieron versiones asincrónicas de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="214c6-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="214c6-122">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="214c6-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="214c6-123">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="214c6-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="214c6-124">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="214c6-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="214c6-125">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="214c6-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="214c6-126">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="214c6-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="214c6-127">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="214c6-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="214c6-128">También hay dos funciones, implementadas ahora en el Winsock2.dll, que se usan para convertir la notación de dirección IPv4 con puntos en y desde representaciones binarias y de cadena, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="214c6-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="214c6-129">**inet \_ addr**</span><span class="sxs-lookup"><span data-stu-id="214c6-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="214c6-130">**inet \_ ntoa**</span><span class="sxs-lookup"><span data-stu-id="214c6-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="214c6-131">Con el fin de mantener la compatibilidad estricta con las versiones anteriores de Windows Sockets 1,1, todas las funciones anteriores solo de IPv4 siguen siendo compatibles, siempre que haya al menos un proveedor de espacios de nombres presente que admita la familia de direcciones de AF \_ inet (estas funciones no son relevantes para la versión 6 de IP, que se indica mediante AF \_ inet6).</span><span class="sxs-lookup"><span data-stu-id="214c6-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="214c6-132">El \_32.dll Ws2 implementa estas funciones de compatibilidad en cuanto a las nuevas funciones de resolución de nombres independientes del Protocolo mediante una secuencia adecuada [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)de /  / llamadas a funciones de siguiente **fin** de WSALookupServiceBegin.</span><span class="sxs-lookup"><span data-stu-id="214c6-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="214c6-133">A continuación se proporcionan los detalles sobre cómo se asignan las funciones de **getXbyY** a las funciones de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="214c6-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="214c6-134">El \_32.dll WSs2 controla las diferencias entre las versiones asincrónica y sincrónica de las funciones de **getXbyY** , por lo que solo se describe la implementación de las funciones sincrónicas de **getXbyY** .</span><span class="sxs-lookup"><span data-stu-id="214c6-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="214c6-135">En esta sección se describe la resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="214c6-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="214c6-136">En la lista siguiente se describen los temas de esta sección:</span><span class="sxs-lookup"><span data-stu-id="214c6-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="214c6-137">Enfoque básico para GetXbyY en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="214c6-138">Funciones getprotobyname y getprotobynumber en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="214c6-139">Funciones getservbyname y getservbyport en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="214c6-140">Función gethostbyname en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="214c6-141">Función gethostbyaddr en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="214c6-142">Función GetHostName (en la API</span><span class="sxs-lookup"><span data-stu-id="214c6-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="214c6-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="214c6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="214c6-144">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="214c6-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="214c6-145">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="214c6-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
