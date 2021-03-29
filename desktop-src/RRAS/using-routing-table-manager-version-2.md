---
title: Usar el administrador de tablas de enrutamiento versión 2
description: Antes de empezar a desarrollar clientes que usan las API de RTMv2, revise los problemas de programación de RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 2, tareas
- Administrador de tablas de enrutamiento versión 2 RRAS, tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994332"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="62858-105">Usar el administrador de tablas de enrutamiento versión 2</span><span class="sxs-lookup"><span data-stu-id="62858-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="62858-106">Antes de empezar a desarrollar clientes que usan las API de RTMv2, revise los [problemas de programación de RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="62858-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="62858-107">Esta sección contiene código de ejemplo que se puede usar al desarrollar clientes como protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="62858-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="62858-108">Problemas de programación de RTMv2</span><span class="sxs-lookup"><span data-stu-id="62858-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="62858-109">Registro con el administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="62858-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="62858-110">Enumerar las entidades registradas</span><span class="sxs-lookup"><span data-stu-id="62858-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="62858-111">Obtener y llamar a los métodos exportados de un cliente</span><span class="sxs-lookup"><span data-stu-id="62858-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="62858-112">Registrar para la notificación de cambios</span><span class="sxs-lookup"><span data-stu-id="62858-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="62858-113">Agregar y actualizar rutas mediante RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="62858-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="62858-114">Actualización de una ruta en contexto mediante RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="62858-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="62858-115">Usar el estado de Hold-Down de ruta</span><span class="sxs-lookup"><span data-stu-id="62858-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="62858-116">Enumerar todos los destinos</span><span class="sxs-lookup"><span data-stu-id="62858-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="62858-117">Enumerar todas las rutas</span><span class="sxs-lookup"><span data-stu-id="62858-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="62858-118">Buscar la mejor ruta</span><span class="sxs-lookup"><span data-stu-id="62858-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="62858-119">Buscar rutas mediante un árbol de prefijo</span><span class="sxs-lookup"><span data-stu-id="62858-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="62858-120">Acceder al puntero opaco en un destino</span><span class="sxs-lookup"><span data-stu-id="62858-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="62858-121">Usar una lista de rutas de Client-Specific</span><span class="sxs-lookup"><span data-stu-id="62858-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="62858-122">Usar la devolución de llamada de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="62858-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




