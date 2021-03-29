---
title: Acerca del administrador de tablas de enrutamiento, versión 2
description: En la siguiente documentación se describe la tecnología del administrador de tablas de enrutamiento versión 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2, descrito
- Administrador de tabla de enrutamiento versión 2 RRAS
- Administrador de tablas de enrutamiento versión 2 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075844"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="d2784-107">Acerca del administrador de tablas de enrutamiento, versión 2</span><span class="sxs-lookup"><span data-stu-id="d2784-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="d2784-108">En la siguiente documentación se describe la tecnología del administrador de tablas de enrutamiento versión 2 (RTMv2).</span><span class="sxs-lookup"><span data-stu-id="d2784-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="d2784-109">RTMv2 API es una característica de Windows 2000 y sistemas operativos posteriores que puede usar para escribir protocolos de enrutamiento que interactúan con el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="d2784-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="d2784-110">El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="d2784-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="d2784-111">RTMv2 no está disponible para la versión 4,0 de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="d2784-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="d2784-112">Además, RTMv2 no se puede usar para protocolos de enrutamiento IPX que se ejecutan en Windows NT 4,0 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d2784-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="d2784-113">Si usa IPX o escribe protocolos de enrutamiento para Windows NT 4,0, consulte [acerca de la versión 1 del administrador de tablas de enrutamiento](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="d2784-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="d2784-114">En esta información general se describen los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2784-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="d2784-115">Componentes de la arquitectura del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="d2784-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="d2784-116">Registro con el administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="d2784-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="d2784-117">Enumerar entidades registradas</span><span class="sxs-lookup"><span data-stu-id="d2784-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="d2784-118">Usar métodos</span><span class="sxs-lookup"><span data-stu-id="d2784-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="d2784-119">Usar punteros opacos</span><span class="sxs-lookup"><span data-stu-id="d2784-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="d2784-120">Marcar rutas para el estado Hold-Down</span><span class="sxs-lookup"><span data-stu-id="d2784-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="d2784-121">Agregar rutas</span><span class="sxs-lookup"><span data-stu-id="d2784-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="d2784-122">Recuperar información de ruta</span><span class="sxs-lookup"><span data-stu-id="d2784-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="d2784-123">Actualizar rutas</span><span class="sxs-lookup"><span data-stu-id="d2784-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="d2784-124">Recibir notificación de cambios</span><span class="sxs-lookup"><span data-stu-id="d2784-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="d2784-125">Trabajar con próximos saltos</span><span class="sxs-lookup"><span data-stu-id="d2784-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="d2784-126">Enumerar entradas de la tabla de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="d2784-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="d2784-127">Buscar información específica en la tabla de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="d2784-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="d2784-128">Mantenimiento de listas de Client-Specific</span><span class="sxs-lookup"><span data-stu-id="d2784-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="d2784-129">Administrar identificadores</span><span class="sxs-lookup"><span data-stu-id="d2784-129">Managing Handles</span></span>](managing-handles.md)

 

 




