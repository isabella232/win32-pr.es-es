---
title: Rutas estáticas y autoestáticas
description: Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994509"
---
# <a name="static-and-autostatic-routes"></a><span data-ttu-id="20703-103">Rutas estáticas y autoestáticas</span><span class="sxs-lookup"><span data-stu-id="20703-103">Static and Autostatic Routes</span></span>

<span data-ttu-id="20703-104">Normalmente, las rutas a redes remotas se obtienen dinámicamente a través de protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="20703-104">Typically, routes to remote networks are obtained dynamically through routing protocols.</span></span> <span data-ttu-id="20703-105">Sin embargo, el administrador también puede *inicializar* la tabla de enrutamiento proporcionando rutas manualmente.</span><span class="sxs-lookup"><span data-stu-id="20703-105">However, the administrator can also *seed* the routing table by providing routes manually.</span></span> <span data-ttu-id="20703-106">Estas rutas se conocen como *estáticas*.</span><span class="sxs-lookup"><span data-stu-id="20703-106">These routes are referred to as *static*.</span></span> <span data-ttu-id="20703-107">Una ruta estática está asociada a una interfaz que representa la red remota.</span><span class="sxs-lookup"><span data-stu-id="20703-107">A static route is associated with an interface that represents the remote network.</span></span> <span data-ttu-id="20703-108">A diferencia de las rutas dinámicas, las rutas estáticas se conservan incluso si el enrutador se reinicia o la interfaz está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="20703-108">Unlike dynamic routes, static routes are retained even if the router is restarted or the interface is disabled.</span></span>

<span data-ttu-id="20703-109">Una ruta *autoestática* se obtiene a través de un protocolo de enrutamiento, pero una vez obtenida se comporta como una ruta estática.</span><span class="sxs-lookup"><span data-stu-id="20703-109">An *autostatic* route is obtained through a routing protocol, but once obtained behaves like a static route.</span></span> <span data-ttu-id="20703-110">El proceso para obtener rutas autoestáticas es el siguiente: el administrador de enrutadores IP o IPX emite una solicitud para que un protocolo de enrutamiento actualice la información de enrutamiento de una interfaz específica.</span><span class="sxs-lookup"><span data-stu-id="20703-110">The process for obtaining autostatic routes is as follows: The IP or IPX router manager issues a request that a routing protocol update the routing information for a specific interface.</span></span> <span data-ttu-id="20703-111">Los resultados de la actualización se convierten después en rutas estáticas.</span><span class="sxs-lookup"><span data-stu-id="20703-111">The results of the update are then converted into static routes.</span></span> <span data-ttu-id="20703-112">Tenga en cuenta que solo determinados protocolos de enrutamiento admiten solicitudes de actualizaciones de rutas autoestáticas.</span><span class="sxs-lookup"><span data-stu-id="20703-112">Note that only certain routing protocols support requests for autostatic route updates.</span></span>

 

 




