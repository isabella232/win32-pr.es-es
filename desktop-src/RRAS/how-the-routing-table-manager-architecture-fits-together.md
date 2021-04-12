---
title: Cómo encaja la arquitectura del administrador de tablas de enrutamiento
description: En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357791"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a><span data-ttu-id="5bc7b-104">Cómo encaja la arquitectura del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="5bc7b-104">How the Routing Table Manager Architecture Fits Together</span></span>

<span data-ttu-id="5bc7b-105">En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-105">The following illustration shows the relationship between the different components of a router.</span></span>

![relación entre los componentes del enrutador](images/rtsrvarch.png)

<span data-ttu-id="5bc7b-107">Cuando se arranca el enrutador, se inicia el servicio Administrador de enrutadores, así como uno o más protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-107">When the router is bootstrapped, the router manager service is started, as well as one or more routing protocols.</span></span> <span data-ttu-id="5bc7b-108">Los protocolos de enrutamiento están asociados a las diversas interfaces en el enrutador.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-108">Routing protocols are associated with the various interfaces on the router.</span></span> <span data-ttu-id="5bc7b-109">El administrador de enrutadores también inicia el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-109">The router manager also starts the routing table manager.</span></span>

<span data-ttu-id="5bc7b-110">En la ilustración siguiente se muestra la relación entre los clientes y los distintos componentes del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-110">The following illustration shows the relationship between clients and the different components of the routing table manager.</span></span>

![relación entre los clientes y los componentes del administrador de tablas de enrutamiento](images/rtmentrel.png)

<span data-ttu-id="5bc7b-112">El administrador de enrutadores inicia una o varias instancias del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-112">The router manager starts one or more instances of the routing table manager.</span></span> <span data-ttu-id="5bc7b-113">Cuando se inician varias instancias del administrador de tablas de enrutamiento, el enrutador se ha configurado para actuar como uno o más enrutadores virtuales.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-113">When multiple instances of the routing table manager are started, the router has been configured to act as one or more virtual routers.</span></span> <span data-ttu-id="5bc7b-114">Cada instancia del administrador de tabla de enrutamiento posee una o más interfaces; cada interfaz solo puede ser propiedad de una instancia del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-114">Each instance of the routing table manager owns one or more interfaces; each interface can only be owned by one instance of the routing table manager.</span></span>

<span data-ttu-id="5bc7b-115">Cada instancia del administrador de tabla de enrutamiento es independiente de las demás; no se intercambia información entre las instancias.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-115">Each instance of the routing table manager is independent from the others; no information is exchanged between the instances.</span></span>

<span data-ttu-id="5bc7b-116">Cada instancia del administrador de tablas de enrutamiento contiene una o más tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-116">Each instance of the routing table manager contains one or more routing tables.</span></span> <span data-ttu-id="5bc7b-117">Cada tabla de enrutamiento está asociada a una familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-117">Each routing table is associated with an address family.</span></span>

<span data-ttu-id="5bc7b-118">Cada tabla de enrutamiento contiene una o más vistas.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-118">Each routing table contains one or more views.</span></span> <span data-ttu-id="5bc7b-119">En este ejemplo, la tabla de enrutamiento se muestra con una vista de unidifusión y multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-119">In this example, the routing table is shown with a unicast and multicast view.</span></span> <span data-ttu-id="5bc7b-120">Cada vista es un subconjunto de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-120">Each view is a subset of the routing table.</span></span>

<span data-ttu-id="5bc7b-121">En la ilustración siguiente se muestra la relación entre los clientes y varias instancias del administrador de tablas de enrutamiento, las tablas de enrutamiento y las vistas.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-121">The following illustration shows the relationship between clients and multiple instances of the routing table manager, routing tables, and views.</span></span>

![clientes de relaciones, administrador de tablas de enrutamiento, tablas de enrutamiento, vistas](images/multrtabrel.png)

<span data-ttu-id="5bc7b-123">Una instancia del cliente se puede registrar varias veces con una instancia del administrador de tablas de enrutamiento, una vez por cada familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-123">An instance of the client can register multiple times with an instance of the routing table manager — once per address family.</span></span> <span data-ttu-id="5bc7b-124">Un cliente se puede registrar con cada instancia del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-124">A client can register with each instance of the routing table manager.</span></span>

<span data-ttu-id="5bc7b-125">En la ilustración siguiente se muestra cómo se relacionan las entradas de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-125">The following illustration shows how the routing table entries are related.</span></span> <span data-ttu-id="5bc7b-126">Para obtener más información sobre las entradas de la tabla de enrutamiento, consulte entradas de la [tabla de enrutamiento](routing-table-entries.md).</span><span class="sxs-lookup"><span data-stu-id="5bc7b-126">For more information on routing table entries, see [Routing Table Entries](routing-table-entries.md).</span></span>

![relación entre las entradas de la tabla de enrutamiento](images/nexthop.png)

<span data-ttu-id="5bc7b-128">La tabla de enrutamiento contiene destinos.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-128">The routing table contains destinations.</span></span> <span data-ttu-id="5bc7b-129">Cada destino está relacionado con una o más rutas.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-129">Each destination is related to one or more routes.</span></span> <span data-ttu-id="5bc7b-130">Cada ruta tiene cero, uno o más punteros a los saltos siguientes que están asociados a la ruta.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-130">Each route has zero, one, or more pointers to next hops that are associated with the route.</span></span> <span data-ttu-id="5bc7b-131">Cada puntero hace referencia al próximo salto real de la lista de próximos saltos.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-131">Each pointer refers to the actual next hop in the list of next hops.</span></span> <span data-ttu-id="5bc7b-132">Cada cliente que se registra con el administrador de tablas de enrutamiento crea una lista de los saltos siguientes que el cliente posee.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-132">Each client that registers with the routing table manager creates a list of next hops that the client owns.</span></span>

<span data-ttu-id="5bc7b-133">Las rutas solo pueden contener punteros a la lista de próximo salto asociada al cliente que posee la ruta.</span><span class="sxs-lookup"><span data-stu-id="5bc7b-133">Routes can only contain pointers to the next-hop list associated with the client that owns the route.</span></span>

 

 




