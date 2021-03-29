---
title: Actualización de las rutas en su lugar mediante RtmUpdateAndUnlockRoute
description: La actualización en contexto suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto, como el que usa la función RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075881"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a><span data-ttu-id="3fcaf-103">Actualización de las rutas en su lugar mediante RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="3fcaf-103">Updating Routes In Place Using RtmUpdateAndUnlockRoute</span></span>

<span data-ttu-id="3fcaf-104">La actualización en contexto suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto, como el que usa la función [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) .</span><span class="sxs-lookup"><span data-stu-id="3fcaf-104">Updating in place is generally more efficient than updating the routing table with an indirect method such as that used by the [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) function.</span></span> <span data-ttu-id="3fcaf-105">Este método es más eficaz porque el cliente no necesita obtener un identificador ni pasar la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) hacia y desde el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="3fcaf-105">This method is more efficient because the client is not required to obtain a handle, nor to pass the [**RTM\_ROUTE\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) structure to and from the routing table manager.</span></span> <span data-ttu-id="3fcaf-106">Este método también tarda menos tiempo.</span><span class="sxs-lookup"><span data-stu-id="3fcaf-106">This method also takes less time.</span></span> <span data-ttu-id="3fcaf-107">Sin embargo, la actualización directa de la tabla de enrutamiento puede ser arriesgada, ya que el administrador de tablas de enrutamiento no funciona como intermediario.</span><span class="sxs-lookup"><span data-stu-id="3fcaf-107">However, directly updating the routing table can be risky, since the routing table manager is not functioning as an intermediary.</span></span>

<span data-ttu-id="3fcaf-108">Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [actualizar una ruta en contexto mediante RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span><span class="sxs-lookup"><span data-stu-id="3fcaf-108">For sample code that shows how to use these functions, see [Update a Route In Place Using RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).</span></span>

 

 




