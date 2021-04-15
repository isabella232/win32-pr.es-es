---
title: Agregar y actualizar rutas mediante RtmAddRouteToDest
description: La función RtmAddRouteToDest se usa para agregar nuevas rutas y actualizar las rutas existentes para un destino. En los siguientes procedimientos se explican ambos casos. En el código de ejemplo siguiente se muestra cómo implementar el primer procedimiento.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3594aee054e6815094834bedbc1aae158fc4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676188"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a><span data-ttu-id="6f8b3-105">Agregar y actualizar rutas mediante RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="6f8b3-105">Add and Update Routes Using RtmAddRouteToDest</span></span>

<span data-ttu-id="6f8b3-106">La función [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) se usa para agregar nuevas rutas y actualizar las rutas existentes para un destino.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-106">The function [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) is used to add new routes and update existing routes for a destination.</span></span> <span data-ttu-id="6f8b3-107">En los siguientes procedimientos se explican ambos casos.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-107">The following procedures explain both cases.</span></span> <span data-ttu-id="6f8b3-108">En el código de ejemplo siguiente se muestra cómo implementar el primer procedimiento.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-108">The sample code that follows shows how to implement the first procedure.</span></span>

<span data-ttu-id="6f8b3-109">**Para agregar una ruta, el cliente debe realizar los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="6f8b3-109">**To add a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="6f8b3-110">Si el cliente ya ha almacenado en la memoria caché el controlador de próximo salto, vaya al paso 4.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-110">If the client has already cached the next-hop handle, go to step 4.</span></span>
2.  <span data-ttu-id="6f8b3-111">Cree una estructura de [**\_ \_ información de NEXTHOP de RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) y rellénelo con la información adecuada.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-111">Create an [**RTM\_NEXTHOP\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) structure and fill it with the appropriate information.</span></span>
3.  <span data-ttu-id="6f8b3-112">Agregue el próximo salto a la tabla de enrutamiento llamando a [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span><span class="sxs-lookup"><span data-stu-id="6f8b3-112">Add the next hop to the routing table by calling [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop).</span></span> <span data-ttu-id="6f8b3-113">El administrador de tabla de enrutamiento devuelve un identificador al próximo salto.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-113">The routing table manager returns a handle to the next hop.</span></span> <span data-ttu-id="6f8b3-114">Si el próximo salto ya existe, la tabla de enrutamiento no agrega el próximo salto; en su lugar, devuelve el identificador al próximo salto.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-114">If the next hop already exists, the routing table does not add the next hop; instead it returns the handle to the next hop.</span></span>
4.  <span data-ttu-id="6f8b3-115">Cree una estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) y rellénelo con la información adecuada, incluido el identificador de próximo salto devuelto por el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-115">Create an [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure and fill it with the appropriate information, including the next-hop handle returned by the routing table manager.</span></span>
5.  <span data-ttu-id="6f8b3-116">Agregue la ruta a la tabla de enrutamiento llamando a [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span><span class="sxs-lookup"><span data-stu-id="6f8b3-116">Add the route to the routing table by calling [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest).</span></span> <span data-ttu-id="6f8b3-117">El administrador de tablas de enrutamiento compara la nueva ruta con las rutas que ya están en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-117">The routing table manager compares the new route to the routes that are already in the routing table.</span></span> <span data-ttu-id="6f8b3-118">Dos rutas son iguales si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f8b3-118">Two routes are equal if all of the following conditions are true:</span></span>

    -   <span data-ttu-id="6f8b3-119">La ruta se está agregando al mismo destino.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-119">The route is being added to the same destination.</span></span>
    -   <span data-ttu-id="6f8b3-120">El mismo cliente agrega la ruta, tal y como lo especifica el miembro **propietario** de la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="6f8b3-120">The route is being added by the same client as specified by the **Owner** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>
    -   <span data-ttu-id="6f8b3-121">El mismo vecino anuncia la ruta, tal y como lo especifica el miembro **vecino** de la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) .</span><span class="sxs-lookup"><span data-stu-id="6f8b3-121">The route is advertised by the same neighbor as specified by the **Neighbor** member of the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

    <span data-ttu-id="6f8b3-122">Si existe la ruta, el administrador de tablas de enrutamiento devuelve el identificador de la ruta existente.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-122">If the route exists, the routing table manager returns the handle to the existing route.</span></span> <span data-ttu-id="6f8b3-123">De lo contrario, el administrador de tablas de enrutamiento agrega la ruta y devuelve el identificador de la nueva ruta.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-123">Otherwise, the routing table manager adds the route and returns the handle to the new route.</span></span>

    <span data-ttu-id="6f8b3-124">El cliente puede establecer el parámetro de *\_ marcas de cambio* en RTM \_ Route \_ Change \_ New para indicar al administrador de la tabla de enrutamiento que agregue una nueva ruta en el destino, incluso si existe otra ruta con los mismos campos de propietario y vecino.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-124">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_NEW to instruct the routing table manager to add a new route on the destination, even if another route with the same owner and neighbor fields exists.</span></span>

    <span data-ttu-id="6f8b3-125">El cliente puede establecer el parámetro de *\_ marcas de cambio* en la \_ ruta RTM \_ \_ primero para indicar al administrador de tablas de enrutamiento que actualice la primera ruta en el destino propiedad del cliente.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-125">The client can set the *Change\_Flags* parameter to RTM\_ROUTE\_CHANGE\_FIRST to tell the routing table manager to update the first route on the destination owned by the client.</span></span> <span data-ttu-id="6f8b3-126">Esta actualización se puede realizar si existe una ruta de este tipo, incluso si el campo vecino no coincide.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-126">This update can be performed if such a route exists, even if the neighbor field does not match.</span></span> <span data-ttu-id="6f8b3-127">Esta marca la usan los clientes que mantienen una única ruta por destino.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-127">This flag is used by clients that maintain a single route per destination.</span></span>

<span data-ttu-id="6f8b3-128">**Para actualizar una ruta, el cliente debe realizar los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="6f8b3-128">**To update a route, the client should take the following steps**</span></span>

1.  <span data-ttu-id="6f8b3-129">Llame a [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) con el identificador de la ruta.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-129">Call [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) with the handle to the route.</span></span> <span data-ttu-id="6f8b3-130">El identificador es el que el cliente ha almacenado previamente en la memoria caché o lo ha devuelto el administrador de tabla de enrutamiento desde una llamada que devuelve un identificador de ruta como **RtmGetRouteInfo**.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-130">The handle is either one previously cached by the client, or returned by the routing table manager from a call that returns a route handle such as **RtmGetRouteInfo**.</span></span>
2.  <span data-ttu-id="6f8b3-131">Realice los cambios en la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) devuelta por el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-131">Make the changes to the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure that is returned by the routing table manager.</span></span>
3.  <span data-ttu-id="6f8b3-132">Llame a [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) con el identificador de la ruta y la estructura de [**\_ \_ información de ruta de RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) modificada.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-132">Call [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) with the handle to the route and the changed [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure.</span></span>

<span data-ttu-id="6f8b3-133">En el código de ejemplo siguiente se muestra cómo agregar una ruta a un destino mediante el administrador de tablas de enrutamiento como intermediario.</span><span class="sxs-lookup"><span data-stu-id="6f8b3-133">The following sample code shows how to add a route to a destination using the routing table manager as an intermediary.</span></span>


```C++
// Add a route to a destination given by (addr, masklen)
// using a next hop reachable with an interface

RTM_NEXTHOP_INFO NextHopInfo;

// First, create and add a next hop to the caller's
// next-hop tree (if it does not already exist)

ZeroMemory(&NextHopInfo, sizeof(RTM_NEXTHOP_INFO);

RTM_IPV4_MAKE_NET_ADDRESS(&NextHopInfo.NextHopAddress,
                          nexthop, // Address of the next hop
                          32);

NextHopInfo.InterfaceIndex = interface;

NextHopHandle = NULL;

Status = RtmAddNextHop(RtmRegHandle,
                       &NextHopInfo,
                       &NextHopHandle,
                       &ChangeFlags);

if (Status == NO_ERROR)
{
    // Created a new next hop or found an old one

        // Fill in the route information for the route
    
    ZeroMemory(&RouteInfo, sizeof(RTM_ROUTE_INFO);

    // Fill in the destination network's address and mask values
    RTM_IPV4_MAKE_NET_ADDRESS(&NetAddress, addr, masklen);

    // Assume 'neighbour learnt from' is the first next hop
    RouteInfo.Neighbour = NextHopHandle;

    // Set metric for route; Preference set internally
    RouteInfo.PrefInfo.Metric = metric;

    // Adding a route to both the unicast and multicast views
    RouteInfo.BelongsToViews = RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST;

    RouteInfo.NextHopsList.NumNextHops = 1;
    RouteInfo.NextHopsList.NextHops[0] = NextHopHandle;

    // If you want to add a new route, regardless of
    // whether a similar route already exists, use the following 
    //     ChangeFlags = RTM_ROUTE_CHANGE_NEW;

    ChangeFlags = 0;

    Status = RtmAddRouteToDest(RtmRegHandle,
                               &RouteHandle,     // Can be NULL if you do not need handle
                               &NetAddress,
                               &RouteInfo,
                               1000,             // Time out route after 1000 ms
                               RouteListHandle1, // Also add the route to this list
                               0,
                               NULL,
                               &ChangeFlags);

    if (Status == NO_ERROR)
    {
        if (ChangeFlags & RTM_ROUTE_CHANGE_NEW)
        {
        ; // A new route has been created
        }
        else
        {
        ; // An existing route is updated
        }

        if (ChangeFlags & RTM_ROUTE_CHANGE_BEST)
        {
        ; // Best route information has changed
        }

        // Release the route handle if you do not need it
        RtmReleaseRoutes(RtmRegHandle, 1, &RouteHandle);
    }

    // Also release the next hop since it is no longer needed 
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHopHandle);
}
```



 

 




