---
title: Agregar y actualizar rutas mediante RtmAddRouteToDest
description: La función RtmAddRouteToDest se usa para agregar nuevas rutas y actualizar las rutas existentes para un destino. Los procedimientos siguientes explican ambos casos. El código de ejemplo siguiente muestra cómo implementar el primer procedimiento.
ms.assetid: 17a04511-69f8-4e50-993c-0e558ee72184
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64032aa5f73019e08bb82405d85ffa5ef85abd0526cf7748ec8881b97ab900e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030605"
---
# <a name="add-and-update-routes-using-rtmaddroutetodest"></a>Agregar y actualizar rutas mediante RtmAddRouteToDest

La función [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) se usa para agregar nuevas rutas y actualizar las rutas existentes para un destino. Los procedimientos siguientes explican ambos casos. El código de ejemplo siguiente muestra cómo implementar el primer procedimiento.

**Para agregar una ruta, el cliente debe realizar los pasos siguientes**

1.  Si el cliente ya ha almacenado en caché el identificador del próximo salto, vaya al paso 4.
2.  Cree una [**estructura \_ DE INFORMACIÓN NEXTHOP \_ de RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) y rellene con la información adecuada.
3.  Agregue el próximo salto a la tabla de enrutamiento mediante una llamada [**a RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). El administrador de tablas de enrutamiento devuelve un identificador al próximo salto. Si el próximo salto ya existe, la tabla de enrutamiento no agrega el próximo salto; en su lugar, devuelve el identificador al próximo salto.
4.  Cree una [**estructura RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) y rellene con la información adecuada, incluido el identificador de próximo salto devuelto por el administrador de tablas de enrutamiento.
5.  Agregue la ruta a la tabla de enrutamiento llamando [**a RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) El administrador de tablas de enrutamiento compara la nueva ruta con las rutas que ya están en la tabla de enrutamiento. Dos rutas son iguales si se cumplen todas las condiciones siguientes:

    -   La ruta se está agregando al mismo destino.
    -   El mismo cliente está agregando la ruta especificada por el miembro **Owner** de la estructura [**ROUTE INFO \_ \_ de RTM.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)
    -   El mismo vecino anuncia la ruta según lo especificado por el miembro **Vecino** de la estructura [**\_ RTM ROUTE \_ INFO.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)

    Si la ruta existe, el administrador de tablas de enrutamiento devuelve el identificador a la ruta existente. De lo contrario, el administrador de tablas de enrutamiento agrega la ruta y devuelve el identificador a la nueva ruta.

    El cliente puede establecer el parámetro *Change \_ Flags* en RTM ROUTE CHANGE NEW para indicar al administrador de tablas de enrutamiento que agregue una nueva ruta en el destino, incluso si existe otra ruta con el mismo propietario y los mismos campos \_ \_ \_ vecinos.

    El cliente puede establecer el parámetro *Change \_ Flags* en RTM ROUTE CHANGE FIRST para que el administrador de tablas de enrutamiento actualice la primera ruta en el destino propiedad \_ del \_ \_ cliente. Esta actualización se puede realizar si existe una ruta de este tipo, incluso si el campo vecino no coincide. Esta marca la usan los clientes que mantienen una sola ruta por destino.

**Para actualizar una ruta, el cliente debe realizar los pasos siguientes**

1.  Llame [**a RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) con el identificador de la ruta. El identificador es uno almacenado previamente en caché por el cliente o devuelto por el administrador de tablas de enrutamiento de una llamada que devuelve un identificador de ruta como **RtmGetRouteInfo**.
2.  Realice los cambios en la estructura [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) devuelta por el administrador de tablas de enrutamiento.
3.  Llame [**a RtmAddRouteToDest con**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) el identificador de la ruta y la estructura [**\_ RTM ROUTE INFO \_ modificada.**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info)

El código de ejemplo siguiente muestra cómo agregar una ruta a un destino mediante el administrador de tablas de enrutamiento como intermediario.


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



 

 




