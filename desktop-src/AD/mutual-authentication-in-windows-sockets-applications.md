---
title: Autenticación mutua en aplicaciones de Windows Sockets
description: Los servicios de Microsoft Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios, o bien pueden usar puntos de conexión de servicio.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en aplicaciones de Windows Sockets
- Active Directory, uso, autenticación mutua, en aplicaciones de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268273"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="608e9-105">Autenticación mutua en aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="608e9-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="608e9-106">Los servicios de Microsoft Windows Sockets pueden usar las API de registro y resolución (RnR) para publicar servicios, o bien pueden usar puntos de conexión de servicio.</span><span class="sxs-lookup"><span data-stu-id="608e9-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="608e9-107">Para obtener más información y un ejemplo de código que muestra cómo realizar la autenticación mutua para un servicio de Windows Sockets que se publica mediante un punto de conexión de servicio, consulte [autenticación mutua en un servicio de Windows Sockets con un SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="608e9-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="608e9-108">En este ejemplo de código se usa un paquete de seguridad de SSPI para administrar las negociaciones de autenticación entre un cliente y el servicio WinSock.</span><span class="sxs-lookup"><span data-stu-id="608e9-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="608e9-109">Un servicio WinSock RnR puede usar un código similar para realizar la autenticación mutua mediante un paquete SSPI.</span><span class="sxs-lookup"><span data-stu-id="608e9-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="608e9-110">En este caso, el servicio crearía sus SPN con el nombre distintivo de la entrada del servicio en el contenedor WinsockServices del directorio.</span><span class="sxs-lookup"><span data-stu-id="608e9-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="608e9-111">Por ejemplo, si el servicio se registra a sí mismo con el nombre "WinSockRnRSampleService", crearía el SPN del servicio a partir del nombre distintivo siguiente:</span><span class="sxs-lookup"><span data-stu-id="608e9-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




