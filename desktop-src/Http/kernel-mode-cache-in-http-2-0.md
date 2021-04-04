---
title: Caché de modo kernel
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076262"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="be860-103">Caché de modo kernel</span><span class="sxs-lookup"><span data-stu-id="be860-103">Kernel Mode Cache</span></span>

<span data-ttu-id="be860-104">La API del servidor HTTP versión 2,0 permite a las aplicaciones almacenar en caché las respuestas con contenido estático en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="be860-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="be860-105">Se consigue un mayor rendimiento cuando las solicitudes se atienden desde la memoria caché del kernel sin pasar al modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="be860-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="be860-106">La API del servidor HTTP aplica las configuraciones de propiedades adecuadas a todas las solicitudes atendidas desde la caché del kernel, incluidas las respuestas de registro.</span><span class="sxs-lookup"><span data-stu-id="be860-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="be860-107">Sin embargo, las solicitudes que requieren autenticación no se servirán desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="be860-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="be860-108">La API del servidor HTTP limita la memoria caché del modo kernel a las solicitudes que cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="be860-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="be860-109">El verbo de solicitud es GET y se ha recibido toda la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be860-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="be860-110">La solicitud no debe tener un cuerpo de entidad.</span><span class="sxs-lookup"><span data-stu-id="be860-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="be860-111">El protocolo HTTP es la versión 1,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="be860-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="be860-112">El encabezado "translate: f" no está presente.</span><span class="sxs-lookup"><span data-stu-id="be860-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="be860-113">No hay encabezados que no sean "expect: 100-Continue".</span><span class="sxs-lookup"><span data-stu-id="be860-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="be860-114">El encabezado Authorization no está presente.</span><span class="sxs-lookup"><span data-stu-id="be860-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="be860-115">Los encabezados Range y If-Range no están presentes.</span><span class="sxs-lookup"><span data-stu-id="be860-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="be860-116">Además de las restricciones de la solicitud, la respuesta también debe cumplir las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="be860-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="be860-117">De forma predeterminada, el tamaño de la respuesta está limitado a 256 KB.</span><span class="sxs-lookup"><span data-stu-id="be860-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="be860-118">Para cambiar el tamaño de la respuesta almacenada en caché, establezca el valor del registro **UriMaxUriBytes** en el número de bytes necesario.</span><span class="sxs-lookup"><span data-stu-id="be860-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="be860-119">La respuesta completa debe proporcionarse en una única llamada a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span><span class="sxs-lookup"><span data-stu-id="be860-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="be860-120">No se debe suprimir el encabezado de fecha de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be860-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="be860-121">Si el encabezado last-modified está presente, el valor del encabezado debe tener la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="be860-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="be860-122">El valor de hora de este encabezado se usa para la comprobación del control de caché.</span><span class="sxs-lookup"><span data-stu-id="be860-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="be860-123">La memoria caché del modo kernel tiene espacio suficiente para almacenar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be860-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="be860-124">De forma predeterminada, está habilitada la caché de respuesta de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="be860-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="be860-125">Si no se cumple alguna de las condiciones para la solicitud o respuesta mencionada anteriormente, se enviará la respuesta, pero no se almacenará en caché.</span><span class="sxs-lookup"><span data-stu-id="be860-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="be860-126">En la API del servidor HTTP versión 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) incluye un parámetro *pCachePolicy* opcional para pasar la estructura de la [**\_ \_ Directiva de caché http**](/windows/desktop/api/Http/ns-http-http_cache_policy) .</span><span class="sxs-lookup"><span data-stu-id="be860-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="be860-127">Las aplicaciones usan la estructura de la Directiva de caché para configurar la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="be860-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




