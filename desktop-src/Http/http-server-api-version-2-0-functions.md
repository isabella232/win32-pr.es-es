---
title: Funciones de la API de servidor HTTP versión 2.0
description: La API del servidor HTTP versión 2.0 proporciona las siguientes funciones.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funciones de la API de servidor HTTP versión 2.0
- Functions HTTP, HTTP Server API versión 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549080"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="a93be-105">Funciones de la API de servidor HTTP versión 2.0</span><span class="sxs-lookup"><span data-stu-id="a93be-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="a93be-106">La API del servidor HTTP versión 2.0 proporciona las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="a93be-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="a93be-107">Función</span><span class="sxs-lookup"><span data-stu-id="a93be-107">Function</span></span> | <span data-ttu-id="a93be-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a93be-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="a93be-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="a93be-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="a93be-110">Delega una solicitud de la cola de solicitudes de origen a la cola de solicitudes de destino.</span><span class="sxs-lookup"><span data-stu-id="a93be-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="a93be-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="a93be-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="a93be-112">Recupera un identificador de grupo de direcciones URL para una dirección URL y una cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="a93be-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="a93be-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="a93be-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="a93be-114">Comprueba si se admite una característica determinada.</span><span class="sxs-lookup"><span data-stu-id="a93be-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="a93be-115">Sesión de servidor</span><span class="sxs-lookup"><span data-stu-id="a93be-115">Server session</span></span>

| <span data-ttu-id="a93be-116">Función</span><span class="sxs-lookup"><span data-stu-id="a93be-116">Function</span></span> | <span data-ttu-id="a93be-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a93be-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="a93be-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="a93be-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="a93be-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="a93be-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="a93be-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="a93be-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="a93be-122">Grupos de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="a93be-122">URL Groups</span></span>

| <span data-ttu-id="a93be-123">Función</span><span class="sxs-lookup"><span data-stu-id="a93be-123">Function</span></span> | <span data-ttu-id="a93be-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a93be-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="a93be-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a93be-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="a93be-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a93be-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="a93be-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a93be-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="a93be-128">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="a93be-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="a93be-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="a93be-130">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="a93be-131">Cola de solicitudes</span><span class="sxs-lookup"><span data-stu-id="a93be-131">Request Queue</span></span>

| <span data-ttu-id="a93be-132">Función</span><span class="sxs-lookup"><span data-stu-id="a93be-132">Function</span></span> | <span data-ttu-id="a93be-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a93be-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="a93be-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a93be-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="a93be-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a93be-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="a93be-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="a93be-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="a93be-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="a93be-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="a93be-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="a93be-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="a93be-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="a93be-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a93be-140">Related topics</span></span>

[<span data-ttu-id="a93be-141">Estructuras de LA API del servidor HTTP versión 2.0</span><span class="sxs-lookup"><span data-stu-id="a93be-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
