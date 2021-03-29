---
title: Marcas de consulta de tabla de enrutamiento
description: Use estas constantes para las consultas de tabla de enrutador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Marcas de consulta de tabla de enrutamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903915"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="e5e0d-104">Marcas de consulta de tabla de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="e5e0d-104">Routing Table Query Flags</span></span>

<span data-ttu-id="e5e0d-105">Use estas constantes para las consultas de tabla de enrutador.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="e5e0d-106">Constante</span><span class="sxs-lookup"><span data-stu-id="e5e0d-106">Constant</span></span>              | <span data-ttu-id="e5e0d-107">Value</span><span class="sxs-lookup"><span data-stu-id="e5e0d-107">Value</span></span>      | <span data-ttu-id="e5e0d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e0d-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e5e0d-109">RTM no \_ coincide con \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="e5e0d-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="e5e0d-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5e0d-110">0x00000000</span></span> | <span data-ttu-id="e5e0d-111">Coincide con ninguno de los criterios; se devuelven todas las rutas para el destino.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="e5e0d-112">propietario de la coincidencia de RTM \_ \_</span><span class="sxs-lookup"><span data-stu-id="e5e0d-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="e5e0d-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e5e0d-113">0x00000001</span></span> | <span data-ttu-id="e5e0d-114">Coincide con las rutas con el mismo propietario.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="e5e0d-115">\_vecino de coincidencia de RTM \_</span><span class="sxs-lookup"><span data-stu-id="e5e0d-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="e5e0d-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e5e0d-116">0x00000002</span></span> | <span data-ttu-id="e5e0d-117">Coincide con las rutas con el mismo vecino.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="e5e0d-118">\_preferencias de coincidencia de RTM \_</span><span class="sxs-lookup"><span data-stu-id="e5e0d-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="e5e0d-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e5e0d-119">0x00000004</span></span> | <span data-ttu-id="e5e0d-120">Coincide con las rutas que tienen la misma preferencia.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="e5e0d-121">\_próximo salto de coincidencia de RTM \_</span><span class="sxs-lookup"><span data-stu-id="e5e0d-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="e5e0d-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e5e0d-122">0x00000008</span></span> | <span data-ttu-id="e5e0d-123">Coincide con las rutas que tienen el mismo salto siguiente.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="e5e0d-124">\_interfaz de coincidencia de RTM \_</span><span class="sxs-lookup"><span data-stu-id="e5e0d-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="e5e0d-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5e0d-125">0x00000010</span></span> | <span data-ttu-id="e5e0d-126">Coincide con las rutas que se encuentran en la misma interfaz.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="e5e0d-127">\_coincidencia \_ completa de RTM</span><span class="sxs-lookup"><span data-stu-id="e5e0d-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="e5e0d-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="e5e0d-128">0x0000FFFF</span></span> | <span data-ttu-id="e5e0d-129">Coincide con rutas con todos los criterios.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="e5e0d-130">\_mejor \_ Protocolo RTM</span><span class="sxs-lookup"><span data-stu-id="e5e0d-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="e5e0d-131">0</span><span class="sxs-lookup"><span data-stu-id="e5e0d-131">0</span></span>          | <span data-ttu-id="e5e0d-132">Devuelve una ruta sin tener en consideración el protocolo que la posea.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="e5e0d-133">RTM \_ este \_ Protocolo</span><span class="sxs-lookup"><span data-stu-id="e5e0d-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="e5e0d-134">~0</span><span class="sxs-lookup"><span data-stu-id="e5e0d-134">~0</span></span>         | <span data-ttu-id="e5e0d-135">Devuelve la mejor ruta para el protocolo de llamada.</span><span class="sxs-lookup"><span data-stu-id="e5e0d-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




