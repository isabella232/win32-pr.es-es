---
title: Acerca de WinINet
description: La interfaz de programación de aplicaciones (API) de Windows Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para tener acceso a los recursos de Internet.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Acerca de WinINet WinINet
- WinINet WinINet, acerca de
- WinINet WinINet, página de inicio
- Windows Internet WinINet
- Internet, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994984"
---
# <a name="about-wininet"></a><span data-ttu-id="27277-108">Acerca de WinINet</span><span class="sxs-lookup"><span data-stu-id="27277-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="27277-109">En el caso de los contenedores de aplicaciones desde la versión 1709 de Windows 10, HTTP/2 (consulte [RFC7540](https://tools.ietf.org/html/rfc7540)) está activada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="27277-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="27277-110">La interfaz de programación de aplicaciones (API) de Windows Internet (WinINet) permite que la aplicación interactúe con los protocolos FTP y HTTP para tener acceso a los recursos de Internet.</span><span class="sxs-lookup"><span data-stu-id="27277-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="27277-111">A medida que evolucionan los estándares, estas funciones controlan los cambios en los protocolos subyacentes, lo que les permite mantener un comportamiento coherente.</span><span class="sxs-lookup"><span data-stu-id="27277-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="27277-112">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También permite a las aplicaciones interactuar con Gopher.</span><span class="sxs-lookup"><span data-stu-id="27277-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="27277-113">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="27277-113">For more information, see:</span></span>

-   [<span data-ttu-id="27277-114">WinINet frente a WinHTTP</span><span class="sxs-lookup"><span data-stu-id="27277-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="27277-115">Controladores de HINTERNET</span><span class="sxs-lookup"><span data-stu-id="27277-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="27277-116">Compatibilidad con IP versión 6</span><span class="sxs-lookup"><span data-stu-id="27277-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="27277-117">Codificación de contenido \_</span><span class="sxs-lookup"><span data-stu-id="27277-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="27277-118">Almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="27277-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="27277-119">Funciones comunes</span><span class="sxs-lookup"><span data-stu-id="27277-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="27277-120">Sesiones FTP</span><span class="sxs-lookup"><span data-stu-id="27277-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="27277-121">Sesiones HTTP</span><span class="sxs-lookup"><span data-stu-id="27277-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="27277-122">Cookies HTTP</span><span class="sxs-lookup"><span data-stu-id="27277-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="27277-123">Operación asincrónica</span><span class="sxs-lookup"><span data-stu-id="27277-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="27277-124">Controlar la autenticación</span><span class="sxs-lookup"><span data-stu-id="27277-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="27277-125">Controlar localizadores uniformes de recursos</span><span class="sxs-lookup"><span data-stu-id="27277-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="27277-126">Instrucciones de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="27277-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="27277-127">Protocolos de Internet</span><span class="sxs-lookup"><span data-stu-id="27277-127">Internet Protocols</span></span>

<span data-ttu-id="27277-128">Los dos protocolos de Internet principales son FTP y HTTP.</span><span class="sxs-lookup"><span data-stu-id="27277-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="27277-129">Para obtener más información acerca de estos protocolos, consulte los documentos RFC (solicitud de comentarios) para FTP y HTTP:</span><span class="sxs-lookup"><span data-stu-id="27277-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="27277-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *Protocolo de transferencia de archivos (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="27277-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="27277-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Protocolo de transferencia de hipertexto: http/1.0*.</span><span class="sxs-lookup"><span data-stu-id="27277-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="27277-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Protocolo de transferencia de hipertexto: http/1.1*.</span><span class="sxs-lookup"><span data-stu-id="27277-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="27277-133">(Es posible que estos recursos no estén disponibles en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="27277-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="27277-134">**Windows XP y Windows Server 2003 R2 y versiones anteriores:** También se admitía el protocolo Gopher.</span><span class="sxs-lookup"><span data-stu-id="27277-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="27277-135">Consulte [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *el protocolo Gopher de Internet*.</span><span class="sxs-lookup"><span data-stu-id="27277-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
