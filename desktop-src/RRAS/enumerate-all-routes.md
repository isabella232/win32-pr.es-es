---
title: Enumerar todas las rutas
description: En el procedimiento siguiente se describen los pasos que se usan para enumerar cualquiera de las entidades que usa la API de RTMv2. En el código de ejemplo siguiente se muestra cómo enumerar todas las rutas.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776878"
---
# <a name="enumerate-all-routes"></a><span data-ttu-id="279b7-104">Enumerar todas las rutas</span><span class="sxs-lookup"><span data-stu-id="279b7-104">Enumerate All Routes</span></span>

<span data-ttu-id="279b7-105">En el procedimiento siguiente se describen los pasos que se usan para enumerar cualquiera de las entidades que usa la API de RTMv2.</span><span class="sxs-lookup"><span data-stu-id="279b7-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="279b7-106">En el código de ejemplo siguiente se muestra cómo enumerar todas las rutas.</span><span class="sxs-lookup"><span data-stu-id="279b7-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="279b7-107">**El proceso básico de cada enumeración es el siguiente:**</span><span class="sxs-lookup"><span data-stu-id="279b7-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="279b7-108">Inicie la enumeración obteniendo un identificador del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="279b7-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="279b7-109">Llame a [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) y [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) para proporcionar los criterios que especifican el tipo de información que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="279b7-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="279b7-110">Este criterio incluye, entre otros, un intervalo de destinos, una interfaz determinada y las vistas en las que reside la información.</span><span class="sxs-lookup"><span data-stu-id="279b7-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="279b7-111">Llame a [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) y [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) una o varias veces para recuperar los datos hasta que el administrador de tabla de enrutamiento devuelva el error \_ no \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="279b7-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="279b7-112">Se devuelven los datos de la ruta, el destino y el próximo salto en el orden de la información de dirección (y los valores de preferencia y métrica, si se enumeran las rutas).</span><span class="sxs-lookup"><span data-stu-id="279b7-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="279b7-113">Llame a [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) y [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) cuando los identificadores o las estructuras de información asociados a la enumeración ya no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="279b7-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="279b7-114">Llame a [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) para liberar el identificador de la enumeración que se devolvió cuando se creó la enumeración.</span><span class="sxs-lookup"><span data-stu-id="279b7-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="279b7-115">Esta función se usa para liberar el identificador de todos los tipos de enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="279b7-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="279b7-116">Las rutas que se encuentran en estado de suspensión solo se enumeran cuando un cliente solicita datos de todas las vistas con la \_ máscara de vista RTM \_ \_ any.</span><span class="sxs-lookup"><span data-stu-id="279b7-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="279b7-117">En el código de ejemplo siguiente se muestra cómo enumerar todas las rutas de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="279b7-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




