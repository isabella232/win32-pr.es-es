---
title: Funciones de la API del servidor HTTP versión 2,0
description: La API del servidor HTTP versión 2,0 proporciona las siguientes funciones.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funciones de la API del servidor HTTP versión 2,0
- Functions HTTP, API del servidor HTTP versión 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ab885d7fe45ed45d2233bd216b884d1cf9852
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418730"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="5aecf-105">Funciones de la API del servidor HTTP versión 2,0</span><span class="sxs-lookup"><span data-stu-id="5aecf-105">HTTP Server API Version 2.0 Functions</span></span>

<span data-ttu-id="5aecf-106">La API del servidor HTTP versión 2,0 proporciona las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="5aecf-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

## <a name="server-session"></a><span data-ttu-id="5aecf-107">Sesión de servidor</span><span class="sxs-lookup"><span data-stu-id="5aecf-107">Server Session</span></span>



| <span data-ttu-id="5aecf-108">Función</span><span class="sxs-lookup"><span data-stu-id="5aecf-108">Function</span></span>                                                                 | <span data-ttu-id="5aecf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aecf-109">Description</span></span> |
|--------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5aecf-110">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="5aecf-110">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession)                 |             |
| [<span data-ttu-id="5aecf-111">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="5aecf-111">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession)               |             |
| [<span data-ttu-id="5aecf-112">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-112">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) |             |
| [<span data-ttu-id="5aecf-113">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-113">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)     |             |



 

## <a name="url-groups"></a><span data-ttu-id="5aecf-114">Grupos de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="5aecf-114">URL Groups</span></span>



| <span data-ttu-id="5aecf-115">Función</span><span class="sxs-lookup"><span data-stu-id="5aecf-115">Function</span></span>                                                       | <span data-ttu-id="5aecf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aecf-116">Description</span></span> |
|----------------------------------------------------------------|-------------|
| [<span data-ttu-id="5aecf-117">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5aecf-117">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)           |             |
| [<span data-ttu-id="5aecf-118">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5aecf-118">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup)               |             |
| [<span data-ttu-id="5aecf-119">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5aecf-119">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup)                 |             |
| [<span data-ttu-id="5aecf-120">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-120">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) |             |
| [<span data-ttu-id="5aecf-121">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="5aecf-121">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) |             |
| [<span data-ttu-id="5aecf-122">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-122">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)     |             |



 

## <a name="request-queue"></a><span data-ttu-id="5aecf-123">Cola de solicitudes</span><span class="sxs-lookup"><span data-stu-id="5aecf-123">Request Queue</span></span>



| <span data-ttu-id="5aecf-124">Función</span><span class="sxs-lookup"><span data-stu-id="5aecf-124">Function</span></span>                                                               | <span data-ttu-id="5aecf-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aecf-125">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5aecf-126">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5aecf-126">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)                 |             |
| [<span data-ttu-id="5aecf-127">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5aecf-127">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)               |             |
| [<span data-ttu-id="5aecf-128">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-128">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) |             |
| [<span data-ttu-id="5aecf-129">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="5aecf-129">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)     |             |
| [<span data-ttu-id="5aecf-130">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="5aecf-130">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue)           |             |
| [<span data-ttu-id="5aecf-131">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="5aecf-131">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart)               |             |



 

## <a name="related-topics"></a><span data-ttu-id="5aecf-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5aecf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aecf-133">Estructuras 2,0 de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="5aecf-133">HTTP Server API Version 2.0 Structures</span></span>](http-server-api-version-2-0-structures.md)
</dt> </dl>

 

 




