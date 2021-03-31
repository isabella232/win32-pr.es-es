---
title: Actualización de una ruta en contexto mediante RtmUpdateAndUnlockRoute
description: En el procedimiento siguiente se describen los pasos que se usan para actualizar una ruta en contexto. En el código de ejemplo siguiente se muestra cómo implementar el procedimiento.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418869"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="f5665-104">Actualización de una ruta en contexto mediante RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="f5665-104">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="f5665-105">En el procedimiento siguiente se describen los pasos que se usan para actualizar una ruta en contexto.</span><span class="sxs-lookup"><span data-stu-id="f5665-105">The following procedure outlines the steps used to update a route in place.</span></span> <span data-ttu-id="f5665-106">En el código de ejemplo siguiente se muestra cómo implementar el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f5665-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="f5665-107">**Para actualizar una ruta en contexto, el cliente debe realizar los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="f5665-107">**To update a route in place, the client should take the following steps**</span></span>

1.  <span data-ttu-id="f5665-108">Bloquee la ruta mediante una llamada a [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span><span class="sxs-lookup"><span data-stu-id="f5665-108">Lock the route by calling [**RtmLockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute).</span></span> <span data-ttu-id="f5665-109">Actualmente, esta función bloquea el destino de la ruta.</span><span class="sxs-lookup"><span data-stu-id="f5665-109">Currently, this function actually locks the route's destination.</span></span> <span data-ttu-id="f5665-110">El administrador de tablas de enrutamiento devuelve un puntero a la ruta.</span><span class="sxs-lookup"><span data-stu-id="f5665-110">The routing table manager returns a pointer to the route.</span></span>
2.  <span data-ttu-id="f5665-111">Use el puntero a la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) del administrador de tablas de enrutamiento, obtenida en el paso 1, para realizar los cambios necesarios en la ruta.</span><span class="sxs-lookup"><span data-stu-id="f5665-111">Use the pointer to the routing table manager's [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure, obtained in step 1, to make the necessary changes to the route.</span></span> <span data-ttu-id="f5665-112">Solo se pueden modificar determinados miembros de la estructura de **\_ \_ información de ruta RTM** al actualizarse.</span><span class="sxs-lookup"><span data-stu-id="f5665-112">Only certain members of the **RTM\_ROUTE\_INFO** structure can be modified when updating in place.</span></span> <span data-ttu-id="f5665-113">Estos miembros son: **vecino**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews** y **NextHopsList**.</span><span class="sxs-lookup"><span data-stu-id="f5665-113">These members are: **Neighbour**, **PrefInfo**, **EntitySpecificInfo**, **BelongsToViews**, and **NextHopsList**.</span></span>
    > [!Note]  
    > <span data-ttu-id="f5665-114">Si el cliente agrega información a los miembros de **vecino** o **NextHopsList** , el cliente debe llamar a [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) para incrementar explícitamente el recuento de referencias que el administrador de tabla de enrutamiento mantiene en el objeto de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="f5665-114">If the client adds information to either the **Neighbour** or **NextHopsList** members, the client must call [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) to explicitly increment the reference count that the routing table manager keeps on the next-hop object.</span></span> <span data-ttu-id="f5665-115">Del mismo modo, si el cliente quita información del miembro **NextHopsList** , el cliente debe llamar a [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) para reducir el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="f5665-115">Similarly, if the client removes information from the **NextHopsList** member, the client must call [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) to decrement the reference count.</span></span>

     

3.  <span data-ttu-id="f5665-116">Llame a [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) para notificar al administrador de tablas de enrutamiento que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="f5665-116">Call [**RtmUpdateAndUnlockRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) to notify the routing table manager that a change has taken place.</span></span> <span data-ttu-id="f5665-117">El administrador de tablas de enrutamiento confirma los cambios, actualiza el destino para reflejar la nueva información y, a continuación, desbloquea la ruta.</span><span class="sxs-lookup"><span data-stu-id="f5665-117">The routing table manager commits the changes, updates the destination to reflect the new information, and then unlocks the route.</span></span>

<span data-ttu-id="f5665-118">En el código de ejemplo siguiente se muestra cómo actualizar una ruta directamente, utilizando un puntero a la información de ruta real en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="f5665-118">The following sample code shows how to update a route directly, using a pointer to the actual route information in the routing table.</span></span>


```C++
Status = RtmLockRoute(RtmRegHandle,
                      RouteHandle,
                      TRUE,
                      TRUE,
                      &RoutePointer);

if (Status == NO_ERROR)
{
        // Update route parameters in place (i.e., directly on 
// the routing table manager's copy)
    
    // Update the metric and views of the route
    RoutePointer->PrefInfo.Metric = 16;

    // Change the views so that the route belongs to only the multicast view
    RoutePointer->BelongsToViews = RTM_VIEW_MASK_MCAST;

    // Set the entity-specific information to X
    RoutePointer->EntitySpecificInfo = X;

    // Note that the following manipulation of
    // next-hop references is not needed when
    // using RtmAddRouteToDest, as it is done
    // by the routing table manager automatically
    
    // Change next hop from NextHop1 to NextHop2
    NextHop1 = RoutePointer->NextHopsList.NextHop[0];

    // Explicitly dereference the old next hop
    RtmReleaseNextHops(RtmRegHandle, 1, &NextHop1);

    RoutePointer->NextHopsList.NextHop[0] = NextHop2;

    // Explicitly reference next hop being added
    RtmReferenceHandles(RtmRegHandle, 1, &NextHop2);

    // Call the routing table manager to indicate that route information
    // has changed, and that its position might
    // have to be rearranged and the corresponding destination
    // needs to be updated to reflect this change.
    
    Status = RtmUpdateAndUnlockRoute(RtmRegHandle,
                                     RouteHandle,
                                     INFINITE, // Keep forever
                                     NULL,
                                     0,
                                     NULL,
                                     &ChangeFlags);
    ASSERT(Status == NO_ERROR);
}
```



 

 




