---
title: Actualización de una ruta en su lugar mediante RtmUpdateAndUnlockRoute
description: En el procedimiento siguiente se describen los pasos usados para actualizar una ruta en su lugar. El código de ejemplo siguiente muestra cómo implementar el procedimiento.
ms.assetid: 3598a28f-8ade-4b3f-9d31-4f2c84df2dd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb79b86645d77f0ee44ffd06b8ef6f403dbd8ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265564"
---
# <a name="update-a-route-in-place-using-rtmupdateandunlockroute"></a>Actualización de una ruta en su lugar mediante RtmUpdateAndUnlockRoute

En el procedimiento siguiente se describen los pasos usados para actualizar una ruta en su lugar. El código de ejemplo siguiente muestra cómo implementar el procedimiento.

**Para actualizar una ruta en su lugar, el cliente debe realizar los pasos siguientes**

1.  Para bloquear la ruta, llame [**a RtmLockRoute.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockroute) Actualmente, esta función bloquea realmente el destino de la ruta. El administrador de tabla de enrutamiento devuelve un puntero a la ruta.
2.  Use el puntero a la estructura [**RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) del administrador de tablas de enrutamiento, obtenida en el paso 1, para realizar los cambios necesarios en la ruta. Solo determinados miembros de la **estructura \_ ROUTE INFO \_ de RTM** se pueden modificar al actualizar en su lugar. Estos miembros son: **Cuatro,** **PrefInfo,** **EntitySpecificInfo,** **BelongsToViews** y **NextHopsList.**
    > [!Note]  
    > Si el cliente agrega información a los miembros **Desuso** o **NextHopsList,** el cliente debe llamar a [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) para incrementar explícitamente el recuento de referencias que el administrador de tabla de enrutamiento mantiene en el objeto de próximo salto. De forma similar, si el cliente quita información del miembro **NextHopsList,** el cliente debe llamar a [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) para disminuir el recuento de referencias.

     

3.  Llame [**a RtmUpdateAndUnlockRoute para**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmupdateandunlockroute) notificar al administrador de tablas de enrutamiento que se ha realizado un cambio. El administrador de tablas de enrutamiento confirma los cambios, actualiza el destino para reflejar la nueva información y, a continuación, desbloquea la ruta.

En el código de ejemplo siguiente se muestra cómo actualizar una ruta directamente mediante un puntero a la información de ruta real de la tabla de enrutamiento.


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



 

 




