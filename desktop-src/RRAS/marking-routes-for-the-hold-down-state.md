---
title: Marcar rutas para el estado Hold-Down
description: Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un tiempo determinado después de que se elimine la última ruta al destino.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994321"
---
# <a name="marking-routes-for-the-hold-down-state"></a><span data-ttu-id="00a09-103">Marcar rutas para el estado Hold-Down</span><span class="sxs-lookup"><span data-stu-id="00a09-103">Marking Routes for the Hold-Down State</span></span>

<span data-ttu-id="00a09-104">Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un tiempo determinado después de que se elimine la última ruta al destino.</span><span class="sxs-lookup"><span data-stu-id="00a09-104">Some clients, such as distance vector protocols like RIP and DVMRP, require that destinations be advertised as unreachable for a certain time after the last route to the destination is deleted.</span></span> <span data-ttu-id="00a09-105">La última ruta que se elimine debe anunciarse como inaccesible aunque lleguen las rutas más recientes.</span><span class="sxs-lookup"><span data-stu-id="00a09-105">The last route that is deleted must be advertised as unreachable even if newer routes arrive in the meantime.</span></span> <span data-ttu-id="00a09-106">La última ruta eliminada se marca como en *Estado de suspensión*.</span><span class="sxs-lookup"><span data-stu-id="00a09-106">The last route deleted is marked as being in a *hold-down state*.</span></span> <span data-ttu-id="00a09-107">El proceso de suspensión impide la formación de bucles de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="00a09-107">The hold-down process prevents the formation of routing loops.</span></span> <span data-ttu-id="00a09-108">Los bucles de enrutamiento se producen cuando un protocolo de enrutamiento anuncia información de enrutamiento obsoleta.</span><span class="sxs-lookup"><span data-stu-id="00a09-108">Routing loops are caused when a routing protocol advertises obsolete routing information.</span></span> <span data-ttu-id="00a09-109">Cuando expire el tiempo de espera, estos protocolos reanudarán su anuncio con la nueva ruta más adecuada.</span><span class="sxs-lookup"><span data-stu-id="00a09-109">When the hold-down expires, these protocols resume their advertisement with the new best route.</span></span>

<span data-ttu-id="00a09-110">Un protocolo que implementa Estados de suspensión indica que un destino está en estado de suspensión mediante la función [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) .</span><span class="sxs-lookup"><span data-stu-id="00a09-110">A protocol that implements hold-down states indicates that a destination is in a hold-down state by using the [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) function.</span></span> <span data-ttu-id="00a09-111">El cliente llama a esta función cuando anuncia la mejor ruta a este destino.</span><span class="sxs-lookup"><span data-stu-id="00a09-111">The client calls this function when it advertises the best route to this destination.</span></span> <span data-ttu-id="00a09-112">Si posteriormente se eliminan todas las rutas a este destino, la última ruta que se elimina se mantiene en estado de suspensión durante el período de tiempo especificado en la llamada anterior a **RtmHoldDestination**.</span><span class="sxs-lookup"><span data-stu-id="00a09-112">If all routes to this destination are later deleted, the last route that is deleted is kept in a hold-down state for the period of time specified in the earlier call to **RtmHoldDestination**.</span></span>

<span data-ttu-id="00a09-113">Cuando un protocolo anuncia un destino, la información de ruta que se usa depende de si el protocolo utiliza Estados de retención y si existe una ruta en el estado de retención para el destino.</span><span class="sxs-lookup"><span data-stu-id="00a09-113">When a protocol advertises a destination, the route information that is used depends on whether the protocol uses hold-down states and if a route in the hold-down state exists for the destination.</span></span>

<span data-ttu-id="00a09-114">Los protocolos que no utilizan Estados de suspensión pueden omitir la información de ruta relacionada con los Estados de retención de un destino y siempre anuncian la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="00a09-114">Protocols that do not use hold-down states can ignore route information that relates to hold-down states for a destination, and always advertise the best route.</span></span>

<span data-ttu-id="00a09-115">Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [usar el estado Hold-Down de la ruta](use-the-route-hold-down-state.md).</span><span class="sxs-lookup"><span data-stu-id="00a09-115">For sample code that shows how to use these functions, see [Use the Route Hold-Down State](use-the-route-hold-down-state.md).</span></span>

 

 




