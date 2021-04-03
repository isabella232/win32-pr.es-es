---
title: Acerca de la versión 1 del administrador de tablas de enrutamiento
description: El administrador de tabla de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Servicio de enrutamiento y acceso remoto RRAS, administrador de tablas de enrutamiento versión 1
- RRAS del servicio de enrutamiento y acceso remoto, versión 1 del administrador de tablas de enrutamiento, descrito
- RRAS de administrador de tablas de enrutamiento versión 1
- Administrador de tablas de enrutamiento versión 1 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075845"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="46ed7-107">Acerca de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="46ed7-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="46ed7-108">**Windows Server 2003:** Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="46ed7-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="46ed7-109">Las nuevas aplicaciones deben usar la API del administrador de tablas de enrutamiento versión 2.</span><span class="sxs-lookup"><span data-stu-id="46ed7-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="46ed7-110">El administrador de tabla de enrutamiento es un repositorio central de información de enrutamiento para todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="46ed7-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="46ed7-111">El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los componentes interesados, como los protocolos de enrutamiento, los agentes de administración y los agentes de supervisión.</span><span class="sxs-lookup"><span data-stu-id="46ed7-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="46ed7-112">El administrador de tablas de enrutamiento también determina la mejor ruta para cada red de destino conocida para los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="46ed7-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="46ed7-113">Determina esta ruta en función de las prioridades del Protocolo de enrutamiento y de las métricas asociadas a las rutas.</span><span class="sxs-lookup"><span data-stu-id="46ed7-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="46ed7-114">Tenga en cuenta que el administrador puede configurar las prioridades del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="46ed7-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="46ed7-115">A continuación, el administrador de tablas de enrutamiento pasa la información de la mejor ruta a los reenviadores y de nuevo a los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="46ed7-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="46ed7-116">Cada protocolo de enrutamiento llama a [**RtmRegisterClient**](rtmregisterclient.md) para registrar con el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="46ed7-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="46ed7-117">**RtmRegisterClient** devuelve un identificador que usa el protocolo de enrutamiento para agregar o eliminar entradas de ruta.</span><span class="sxs-lookup"><span data-stu-id="46ed7-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="46ed7-118">**RtmRegisterClient** también permite que el protocolo de enrutamiento registre un objeto de evento con el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="46ed7-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="46ed7-119">El administrador de tablas de enrutamiento señala este objeto de evento para notificar al Protocolo de enrutamiento los cambios en la información de la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="46ed7-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="46ed7-120">Todos los demás componentes pueden obtener información almacenada en el administrador de tablas de enrutamiento a través de la enumeración de rutas.</span><span class="sxs-lookup"><span data-stu-id="46ed7-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




