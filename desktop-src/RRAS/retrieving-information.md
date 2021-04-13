---
title: Recuperar información
description: RTMv2 permite a un cliente recuperar la información a la que hace referencia un identificador determinado mediante las funciones RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo y RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268371"
---
# <a name="retrieving-information"></a><span data-ttu-id="58113-103">Recuperar información</span><span class="sxs-lookup"><span data-stu-id="58113-103">Retrieving Information</span></span>

<span data-ttu-id="58113-104">RTMv2 permite a un cliente recuperar la información a la que hace referencia un identificador determinado mediante las funciones [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)y [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="58113-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="58113-105">Estas llamadas a función tienen funciones correspondientes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) para liberar los identificadores asociados a la estructura de información devuelta por el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="58113-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="58113-106">La información de los clientes solo está disponible en la instancia actual y en la familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="58113-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="58113-107">Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [Buscar la mejor ruta](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="58113-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="58113-108">Usar RtmGetExactMatchRoute y RtmGetExactMatchDestination</span><span class="sxs-lookup"><span data-stu-id="58113-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="58113-109">Los clientes usan las funciones [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) y [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) para buscar una ruta o un destino específicos.</span><span class="sxs-lookup"><span data-stu-id="58113-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="58113-110">Estas funciones ahorran tiempo al realizar el trabajo de comparación para el cliente.</span><span class="sxs-lookup"><span data-stu-id="58113-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="58113-111">Por ejemplo, cuando RIP actualiza una ruta, RIP debe conservar la información de métrica anterior.</span><span class="sxs-lookup"><span data-stu-id="58113-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="58113-112">RIP busca la ruta y su información.</span><span class="sxs-lookup"><span data-stu-id="58113-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="58113-113">Después, RIP puede copiar la información y actualizar la ruta.</span><span class="sxs-lookup"><span data-stu-id="58113-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="58113-114">Usar RtmGetMostSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="58113-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="58113-115">La función [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) se usa para buscar el destino que mejor coincida con el prefijo de red especificado.</span><span class="sxs-lookup"><span data-stu-id="58113-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="58113-116">Por ejemplo, el administrador del grupo de multidifusión usa esta función para realizar una comprobación de reenvío de rutas inversas (RPF) en una sola dirección.</span><span class="sxs-lookup"><span data-stu-id="58113-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="58113-117">La función también se puede usar para buscar el próximo salto local para un próximo salto remoto determinado.</span><span class="sxs-lookup"><span data-stu-id="58113-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="58113-118">Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [buscar rutas mediante un árbol de prefijo](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) y [Buscar la mejor ruta](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="58113-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="58113-119">Usar RtmGetLessSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="58113-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="58113-120">La función [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) se usa para buscar el destino que es la siguiente mejor coincidencia para el prefijo de red especificado.</span><span class="sxs-lookup"><span data-stu-id="58113-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="58113-121">Se puede llamar a esta función varias veces para devolver la siguiente coincidencia menos específica, hasta que no coincidan más destinos.</span><span class="sxs-lookup"><span data-stu-id="58113-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="58113-122">Se llama a esta función después de una llamada a [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span><span class="sxs-lookup"><span data-stu-id="58113-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="58113-123">Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [buscar rutas mediante un árbol de prefijos](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="58113-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="58113-124">Usar RtmIsBestRoute</span><span class="sxs-lookup"><span data-stu-id="58113-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="58113-125">La función [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permite a un cliente averiguar rápidamente si una ruta determinada es la mejor ruta a un destino.</span><span class="sxs-lookup"><span data-stu-id="58113-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="58113-126">Por ejemplo, un cliente puede necesitar almacenar una ruta determinada solo si se trata de la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="58113-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="58113-127">Por lo tanto, el cliente puede llamar a esta función, en lugar de enumerar todas las rutas y realizar la comparación.</span><span class="sxs-lookup"><span data-stu-id="58113-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




