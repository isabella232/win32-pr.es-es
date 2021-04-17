---
title: Trabajar con próximos saltos
description: La API de RTMv2 permite a los clientes trabajar con la lista de próximos saltos que están asociados a rutas y destinos.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419072"
---
# <a name="working-with-next-hops"></a><span data-ttu-id="f8e8d-103">Trabajar con próximos saltos</span><span class="sxs-lookup"><span data-stu-id="f8e8d-103">Working with Next Hops</span></span>

<span data-ttu-id="f8e8d-104">La API de RTMv2 permite a los clientes trabajar con la lista de próximos saltos que están asociados a rutas y destinos.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-104">The RTMv2 API allows clients to work with the list of next hops that are associated with routes and destinations.</span></span> <span data-ttu-id="f8e8d-105">Los clientes pueden agregar o actualizar un próximo salto llamando a [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="f8e8d-105">Clients can add or update a next hop by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="f8e8d-106">Los clientes pueden eliminar un próximo salto mediante [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span><span class="sxs-lookup"><span data-stu-id="f8e8d-106">Clients can delete a next hop using [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop).</span></span> <span data-ttu-id="f8e8d-107">Los clientes pueden buscar los próximos saltos llamando a [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span><span class="sxs-lookup"><span data-stu-id="f8e8d-107">Clients can search for next hops by calling [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).</span></span>

<span data-ttu-id="f8e8d-108">Los clientes también pueden actualizar el próximo salto directamente.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-108">Clients can also update the next hop directly.</span></span> <span data-ttu-id="f8e8d-109">Para ello, el cliente debe bloquear primero el próximo salto con la función [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) .</span><span class="sxs-lookup"><span data-stu-id="f8e8d-109">To do so, the client must first lock the next hop with the [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) function.</span></span> <span data-ttu-id="f8e8d-110">A continuación, el cliente puede usar el puntero directo a la estructura de [**\_ \_ información de NEXTHOP**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) del administrador de tablas de enrutamiento para realizar las modificaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-110">Then the client can use the direct pointer to the routing table manager's [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure to make necessary modifications.</span></span> <span data-ttu-id="f8e8d-111">Por último, el cliente puede desbloquear el próximo salto.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-111">Finally, the client can unlock the next hop.</span></span>

> [!Note]  
> <span data-ttu-id="f8e8d-112">Los campos dirección de próximo salto e índice de interfaz del próximo salto identifican de forma única el próximo salto y no deben modificarse.</span><span class="sxs-lookup"><span data-stu-id="f8e8d-112">The next-hop address and interface index fields in the next hop uniquely identify the next hop and should not be modified.</span></span>

 

 

 




