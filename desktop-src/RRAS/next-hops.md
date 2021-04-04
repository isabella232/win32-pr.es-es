---
title: Próximos saltos
description: Las rutas tienen uno o más saltos próximos asociados.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075201"
---
# <a name="next-hops"></a><span data-ttu-id="d4c67-103">Próximos saltos</span><span class="sxs-lookup"><span data-stu-id="d4c67-103">Next Hops</span></span>

<span data-ttu-id="d4c67-104">Las rutas tienen uno o más saltos próximos asociados.</span><span class="sxs-lookup"><span data-stu-id="d4c67-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="d4c67-105">Si el destino no está en una red conectada directamente, el próximo salto es la dirección del siguiente enrutador (o red) de la red de salida que puede enrutar mejor los datos al destino.</span><span class="sxs-lookup"><span data-stu-id="d4c67-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="d4c67-106">La mejor ruta es la ruta que tiene el menor costo, en función de la Directiva de enrutamiento en uso.</span><span class="sxs-lookup"><span data-stu-id="d4c67-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="d4c67-107">Cada próximo salto se puede usar para reenviar los datos de la ruta de acceso al destino.</span><span class="sxs-lookup"><span data-stu-id="d4c67-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="d4c67-108">Todas las rutas que posee un cliente comparten un conjunto común de entradas de próximo salto agregadas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d4c67-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="d4c67-109">Cada próximo salto se identifica de forma única mediante la dirección del próximo salto y el índice de interfaz que se usa para alcanzar el próximo salto.</span><span class="sxs-lookup"><span data-stu-id="d4c67-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="d4c67-110">Si el próximo salto no se conecta directamente, se marca como un próximo salto "remoto".</span><span class="sxs-lookup"><span data-stu-id="d4c67-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="d4c67-111">En este caso, el reenviador debe realizar otra búsqueda mediante la dirección de red del próximo salto.</span><span class="sxs-lookup"><span data-stu-id="d4c67-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="d4c67-112">Esta búsqueda es necesaria para encontrar el próximo salto "local" que se usa para alcanzar el próximo salto remoto y el destino.</span><span class="sxs-lookup"><span data-stu-id="d4c67-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="d4c67-113">Una entrada de próximo salto en la tabla de enrutamiento incluye:</span><span class="sxs-lookup"><span data-stu-id="d4c67-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="d4c67-114">La dirección de red del próximo salto</span><span class="sxs-lookup"><span data-stu-id="d4c67-114">The network address of the next hop</span></span>
-   <span data-ttu-id="d4c67-115">Propietario del próximo salto.</span><span class="sxs-lookup"><span data-stu-id="d4c67-115">The owner of the next hop</span></span>
-   <span data-ttu-id="d4c67-116">El identificador de la interfaz de salida.</span><span class="sxs-lookup"><span data-stu-id="d4c67-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="d4c67-117">Estado del próximo salto</span><span class="sxs-lookup"><span data-stu-id="d4c67-117">The state of the next hop</span></span>
-   <span data-ttu-id="d4c67-118">Marcas asociadas al próximo salto</span><span class="sxs-lookup"><span data-stu-id="d4c67-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="d4c67-119">Información privada para el propietario del próximo salto</span><span class="sxs-lookup"><span data-stu-id="d4c67-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="d4c67-120">Identificador del destino correspondiente al próximo salto remoto.</span><span class="sxs-lookup"><span data-stu-id="d4c67-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




