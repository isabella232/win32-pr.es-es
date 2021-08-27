---
title: Enumerar todas las rutas
description: En el procedimiento siguiente se describen los pasos usados para enumerar cualquiera de las entidades usadas por la API RTMv2. El código de ejemplo siguiente muestra cómo enumerar todas las rutas.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f8707c7cf78f274fedaca3fb4882ae36dbd569ab5fa1260ec3b6cb663aced3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101855"
---
# <a name="enumerate-all-routes"></a>Enumerar todas las rutas

En el procedimiento siguiente se describen los pasos usados para enumerar cualquiera de las entidades usadas por la API RTMv2. El código de ejemplo siguiente muestra cómo enumerar todas las rutas.

**El proceso básico para cada enumeración es el siguiente:**

1.  Inicie la enumeración obteniendo un identificador del administrador de tablas de enrutamiento. Llame [**a RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) y [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) para proporcionar los criterios que especifican el tipo de información que se enumera. Este criterio incluye, entre otros, un intervalo de destinos, una interfaz determinada y las vistas en las que reside la información.
2.  Llame [**a RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) y [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) una o varias veces para recuperar datos hasta que el administrador de tablas de enrutamiento devuelva ERROR \_ NO MORE \_ \_ ITEMS. Los datos de ruta, destino y próximo salto se devuelven por orden de la información de dirección (y los valores de preferencia y métrica, si se enumeran las rutas).
3.  Llame [**a RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) y [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) cuando los identificadores o estructuras de información asociados a la enumeración ya no sean necesarios.
4.  Llame [**a RtmDeleteEnumHandle para**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) liberar el identificador de enumeración que se devolvió cuando se creó la enumeración. Esta función se usa para liberar el identificador para todos los tipos de enumeraciones.

> [!Note]  
> Las rutas que se encuentran en estado de retención solo se enumeran cuando un cliente solicita datos de todas las vistas mediante RTM \_ VIEW \_ MASK \_ ANY.

 

El código de ejemplo siguiente muestra cómo enumerar todas las rutas de la tabla de enrutamiento.


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



 

 




