---
title: Apagado y limpieza
description: Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075827"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="c6300-103">Apagado y limpieza</span><span class="sxs-lookup"><span data-stu-id="c6300-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="c6300-104">Para que una aplicación finalice correctamente, debe realizar las siguientes operaciones de limpieza:</span><span class="sxs-lookup"><span data-stu-id="c6300-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="c6300-105">Quite todas las direcciones URL registradas del grupo de direcciones URL mediante una llamada a la función [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para anular el registro de las direcciones URL registradas previamente en la llamada a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span><span class="sxs-lookup"><span data-stu-id="c6300-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="c6300-106">Cierre el grupo de direcciones URL mediante una llamada a la función [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) .</span><span class="sxs-lookup"><span data-stu-id="c6300-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="c6300-107">Todos los grupos de direcciones URL creados en una sesión de servidor deben cerrarse antes de cerrar la sesión de servidor.</span><span class="sxs-lookup"><span data-stu-id="c6300-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="c6300-108">Cierre la sesión del servidor mediante una llamada a [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span><span class="sxs-lookup"><span data-stu-id="c6300-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="c6300-109">Cierre el identificador de la cola de solicitudes llamando a [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span><span class="sxs-lookup"><span data-stu-id="c6300-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="c6300-110">Finalice los recursos creados por la API del servidor HTTP mediante una llamada a la función [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con la configuración de marca coincidente para cada llamada que la aplicación realizó originalmente en [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="c6300-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="c6300-111">Cada una de estas llamadas finaliza todos los recursos creados en la llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="c6300-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




