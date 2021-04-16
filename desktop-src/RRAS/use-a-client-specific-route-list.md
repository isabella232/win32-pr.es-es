---
title: Usar una lista de rutas de Client-Specific
description: En los procedimientos siguientes se describen los pasos para usar las listas de rutas específicas del cliente. En el código de ejemplo siguiente se muestra cómo implementar el procedimiento.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cfa893bda9e850527c7ebe35590dbe2d08a490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676231"
---
# <a name="use-a-client-specific-route-list"></a><span data-ttu-id="75450-104">Usar una lista de rutas de Client-Specific</span><span class="sxs-lookup"><span data-stu-id="75450-104">Use a Client-Specific Route List</span></span>

<span data-ttu-id="75450-105">En los procedimientos siguientes se describen los pasos para usar las listas de rutas específicas del cliente.</span><span class="sxs-lookup"><span data-stu-id="75450-105">The following procedures outlines the steps to use the client-specific route lists.</span></span> <span data-ttu-id="75450-106">En el código de ejemplo siguiente se muestra cómo implementar el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="75450-106">The sample code that follows shows how to implement the procedure.</span></span>

<span data-ttu-id="75450-107">**Para usar esta característica, un cliente debe realizar los siguientes pasos:**</span><span class="sxs-lookup"><span data-stu-id="75450-107">**To use this feature, a client should take the following steps**</span></span>

1.  <span data-ttu-id="75450-108">Llame a [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) para obtener un identificador del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="75450-108">Call [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) to obtain a handle from the routing table manager.</span></span>
2.  <span data-ttu-id="75450-109">Llame a [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) siempre que el cliente deba agregar una ruta a esta lista.</span><span class="sxs-lookup"><span data-stu-id="75450-109">Call [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) whenever the client must add a route to this list.</span></span>
3.  <span data-ttu-id="75450-110">Cuando el cliente ya no requiere la lista, debe llamar a [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) para quitar la lista.</span><span class="sxs-lookup"><span data-stu-id="75450-110">When the client no longer requires the list, it should call [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) to remove the list.</span></span>

<span data-ttu-id="75450-111">**Si el cliente debe enumerar las rutas de la lista, el cliente debe realizar los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="75450-111">**If the client must enumerate the routes on the list, the client should take the following steps**</span></span>

1.  <span data-ttu-id="75450-112">Llame a [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) para obtener un identificador de enumeración desde el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="75450-112">Call [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) to obtain an enumeration handle from the routing table manager.</span></span>
2.  <span data-ttu-id="75450-113">Llame a [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) para obtener los identificadores de las rutas de la lista.</span><span class="sxs-lookup"><span data-stu-id="75450-113">Call [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) to obtain the handles to the routes in the list.</span></span>
3.  <span data-ttu-id="75450-114">Llame a [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) para liberar los identificadores cuando ya no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="75450-114">Call [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) to release the handles when no longer required.</span></span>

<span data-ttu-id="75450-115">En el código de ejemplo siguiente se muestra cómo crear y utilizar una lista de rutas específica del cliente.</span><span class="sxs-lookup"><span data-stu-id="75450-115">The following sample code shows how to create and use a client-specific route list.</span></span>


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




