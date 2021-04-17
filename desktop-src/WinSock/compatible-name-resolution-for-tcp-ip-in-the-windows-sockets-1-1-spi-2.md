---
description: Windows Sockets 1,1 definía un número de rutinas que se usaban para la resolución de nombres IPv4 con redes TCP/IP. Normalmente se denominan funciones GetXbyY e incluyen lo siguiente.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Resolución de nombres compatible para TCP/IP en Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696396"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="6e7a2-104">Resolución de nombres compatible para TCP/IP en Windows Sockets 1,1 SPI</span><span class="sxs-lookup"><span data-stu-id="6e7a2-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="6e7a2-105">Windows Sockets 1,1 definía un número de rutinas que se usaban para la resolución de nombres IPv4 con redes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="6e7a2-106">Normalmente se denominan funciones **GetXbyY** e incluyen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="6e7a2-107">**GetHostName (**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="6e7a2-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="6e7a2-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="6e7a2-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="6e7a2-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="6e7a2-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="6e7a2-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="6e7a2-114">También se definieron versiones asincrónicas de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="6e7a2-115">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="6e7a2-116">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="6e7a2-117">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="6e7a2-118">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="6e7a2-119">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="6e7a2-120">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="6e7a2-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="6e7a2-121">Estas funciones son específicas de las redes TCP/IP; no se recomienda que los desarrolladores de aplicaciones independientes del Protocolo sigan usando estas funciones específicas del transporte.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="6e7a2-122">Sin embargo, para mantener la compatibilidad estricta con las versiones anteriores de Windows Sockets 1,1, las funciones anteriores siguen siendo compatibles, siempre que exista al menos un proveedor de espacios de nombres que admita la familia de direcciones de AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="6e7a2-123">El *\_32.dllWs2* implementa estas funciones de compatibilidad en cuanto a las nuevas funciones de resolución de nombres independientes del Protocolo mediante una secuencia adecuada de llamadas a funciones [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .</span><span class="sxs-lookup"><span data-stu-id="6e7a2-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="6e7a2-124">A continuación se proporcionan los detalles sobre cómo se asignan las funciones de **GetXbyY** a las funciones de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="6e7a2-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="6e7a2-125">El \_32.dll Ws2 controla las diferencias entre las versiones asincrónica y sincrónica de las funciones de **GetXbyY** , de modo que solo se describe la implementación de las funciones sincrónicas de **GetXbyY** .</span><span class="sxs-lookup"><span data-stu-id="6e7a2-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
