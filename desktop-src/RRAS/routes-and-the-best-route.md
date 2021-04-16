---
title: Rutas y la mejor ruta
description: Una ruta es una ruta de acceso de red \ 0034; \ 0034; a un destino que tiene un costo determinado asociado. El costo se representa mediante sus preferencias administrativas y su métrica específica del protocolo. Las rutas con costos menores son preferibles a las demás rutas.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676272"
---
# <a name="routes-and-the-best-route"></a><span data-ttu-id="480e4-105">Rutas y la mejor ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-105">Routes and the Best Route</span></span>

<span data-ttu-id="480e4-106">Una ruta es una "ruta de acceso de red" a un destino que tiene un costo concreto asociado.</span><span class="sxs-lookup"><span data-stu-id="480e4-106">A route is a "network path" to a destination that has a certain cost associated with it.</span></span> <span data-ttu-id="480e4-107">El costo se representa mediante sus preferencias administrativas y su métrica específica del protocolo.</span><span class="sxs-lookup"><span data-stu-id="480e4-107">The cost is represented by its administrative preference and its protocol-specific metric.</span></span> <span data-ttu-id="480e4-108">Las rutas con costos menores son preferibles a las demás rutas.</span><span class="sxs-lookup"><span data-stu-id="480e4-108">Routes with lower costs are preferred over all other routes.</span></span>

<span data-ttu-id="480e4-109">Una entrada de ruta en la tabla de enrutamiento incluye:</span><span class="sxs-lookup"><span data-stu-id="480e4-109">A route entry in the routing table includes:</span></span>

-   <span data-ttu-id="480e4-110">Identificador del destino.</span><span class="sxs-lookup"><span data-stu-id="480e4-110">A handle to the destination</span></span>
-   <span data-ttu-id="480e4-111">Propietario de esta ruta.</span><span class="sxs-lookup"><span data-stu-id="480e4-111">The owner of this route</span></span>
-   <span data-ttu-id="480e4-112">El vecino (del mismo nivel) que proporcionó la información de ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-112">The neighbor (peer) that provided the route information</span></span>
-   <span data-ttu-id="480e4-113">Marcas asociadas al estado de la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-113">Flags associated with the state of the route</span></span>
-   <span data-ttu-id="480e4-114">Marcas asociadas a la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-114">Flags associated with the route</span></span>
-   <span data-ttu-id="480e4-115">La preferencia y la métrica de la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-115">The preference and metric for the route</span></span>
-   <span data-ttu-id="480e4-116">Lista de vistas a las que pertenece la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-116">The list of views to which the route belongs</span></span>
-   <span data-ttu-id="480e4-117">Información privada para el propietario de la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-117">Information that is private to the owner of the route</span></span>
-   <span data-ttu-id="480e4-118">Lista de próximos saltos usados para alcanzar el destino.</span><span class="sxs-lookup"><span data-stu-id="480e4-118">A list of next hops used to reach the destination</span></span>

<span data-ttu-id="480e4-119">Los siguientes valores, que se toman juntos, identifican de forma única una ruta en la tabla de enrutamiento:</span><span class="sxs-lookup"><span data-stu-id="480e4-119">The following values, taken together, uniquely identify a route in the routing table:</span></span>

-   <span data-ttu-id="480e4-120">La red de destino</span><span class="sxs-lookup"><span data-stu-id="480e4-120">The destination network</span></span>
-   <span data-ttu-id="480e4-121">Propietario de la ruta.</span><span class="sxs-lookup"><span data-stu-id="480e4-121">The owner of the route</span></span>
-   <span data-ttu-id="480e4-122">El vecino que proporcionó la ruta</span><span class="sxs-lookup"><span data-stu-id="480e4-122">The neighbor who supplied the route</span></span>

## <a name="metrics-and-preference"></a><span data-ttu-id="480e4-123">Métricas y preferencias</span><span class="sxs-lookup"><span data-stu-id="480e4-123">Metrics and Preference</span></span>

<span data-ttu-id="480e4-124">Cada ruta tiene una preferencia administrativa (especificada por la Directiva de enrutamiento) y una métrica dependiente del cliente.</span><span class="sxs-lookup"><span data-stu-id="480e4-124">Each route has an administrative preference (specified by the routing policy), and a client-dependent metric.</span></span> <span data-ttu-id="480e4-125">El administrador de tablas de enrutamiento usa esta información para determinar qué ruta es la mejor ruta a un destino.</span><span class="sxs-lookup"><span data-stu-id="480e4-125">The routing table manager uses this information to determine which route is the better route to a destination.</span></span> <span data-ttu-id="480e4-126">Las rutas con preferencia más baja son rutas mejores (una es la más baja y, por tanto, la mejor opción).</span><span class="sxs-lookup"><span data-stu-id="480e4-126">Routes with lower preference are better routes (one being lowest, and therefore best).</span></span> <span data-ttu-id="480e4-127">Si dos rutas tienen la misma preferencia, la ruta con la métrica inferior es la más adecuada.</span><span class="sxs-lookup"><span data-stu-id="480e4-127">If two routes have the same preference, the route with the lower metric is the better route.</span></span>

<span data-ttu-id="480e4-128">Normalmente, la preferencia de una ruta viene determinada por la preferencia del cliente que agregó la ruta.</span><span class="sxs-lookup"><span data-stu-id="480e4-128">Normally, the preference of a route is determined by the preference of the client that added the route.</span></span> <span data-ttu-id="480e4-129">Sin embargo, para las rutas agregadas mediante la herramienta de administración de Netsh.exe, se puede especificar un valor de preferencia en función de cada ruta.</span><span class="sxs-lookup"><span data-stu-id="480e4-129">However, for any routes added using the Netsh.exe management tool, a preference value can be specified on a per-route basis.</span></span>

<span data-ttu-id="480e4-130">La preferencia se usa normalmente para indicar la prioridad entre los clientes.</span><span class="sxs-lookup"><span data-stu-id="480e4-130">Preference is normally used to indicate priority between clients.</span></span> <span data-ttu-id="480e4-131">Por ejemplo, un administrador puede asignar a OSPF una preferencia inferior (mejor) que RIP.</span><span class="sxs-lookup"><span data-stu-id="480e4-131">For example, an administrator can assign OSPF a lower (better) preference than RIP.</span></span> <span data-ttu-id="480e4-132">En este caso, las rutas OSPF son preferibles a las rutas RIP.</span><span class="sxs-lookup"><span data-stu-id="480e4-132">In this case, OSPF routes are preferable to RIP routes.</span></span>

 

 




