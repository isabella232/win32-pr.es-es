---
title: Cómo encaja la arquitectura de multidifusión
description: En esta sección se describe una configuración de ejemplo y cómo se ajustan los componentes principales.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269019"
---
# <a name="how-the-multicast-architecture-fits-together"></a><span data-ttu-id="042ee-103">Cómo encaja la arquitectura de multidifusión</span><span class="sxs-lookup"><span data-stu-id="042ee-103">How the Multicast Architecture Fits Together</span></span>

<span data-ttu-id="042ee-104">En esta sección se describe una configuración de ejemplo y cómo se ajustan los componentes principales.</span><span class="sxs-lookup"><span data-stu-id="042ee-104">This section describes a sample configuration and how the major components fit together.</span></span>

<span data-ttu-id="042ee-105">En la ilustración siguiente se muestra la relación entre los distintos componentes de un enrutador.</span><span class="sxs-lookup"><span data-stu-id="042ee-105">The following illustration shows the relationship between the various components of a router.</span></span>

![relación entre los componentes del enrutador de Windows 2000](images/mrarch1.png)

<span data-ttu-id="042ee-107">El administrador del grupo de multidifusión es una parte del servicio RRAS que se ejecuta en un servidor que funciona como enrutador.</span><span class="sxs-lookup"><span data-stu-id="042ee-107">The multicast group manager is a part of the RRAS service that runs on a server that is operating as a router.</span></span>

<span data-ttu-id="042ee-108">El enrutador mostrado tiene tres protocolos de enrutamiento de multidifusión (protocolo 1, protocolo 2, protocolo 3) que se ejecutan en él.</span><span class="sxs-lookup"><span data-stu-id="042ee-108">The router shown has three multicast routing protocols (Protocol 1, Protocol 2, Protocol 3) running on it.</span></span> <span data-ttu-id="042ee-109">Cada protocolo puede poseer una o más interfaces (en esta ilustración, el protocolo 1 es el propietario de la interfaz 1, el protocolo 2 es el propietario de la interfaz 2 y el protocolo 3 posee la interfaz 3).</span><span class="sxs-lookup"><span data-stu-id="042ee-109">Each protocol can own one or more interfaces (in this illustration, Protocol 1 owns Interface 1, Protocol 2 owns Interface 2, and Protocol 3 owns Interface 3).</span></span> <span data-ttu-id="042ee-110">Cada interfaz solo puede pertenecer a un protocolo de enrutamiento (además de a IGMP, que es un caso especial).</span><span class="sxs-lookup"><span data-stu-id="042ee-110">Each interface can be owned by only one routing protocol (in addition to IGMP, which is a special case).</span></span>

<span data-ttu-id="042ee-111">El administrador del grupo de multidifusión se ejecuta en el enrutador y coordina la distribución de la información de grupo entre los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="042ee-111">The multicast group manager runs on the router and coordinates the distribution of group information between the routing protocols.</span></span>

<span data-ttu-id="042ee-112">En la ilustración siguiente se muestra la relación entre dos enrutadores en una arquitectura de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="042ee-112">The following illustration shows the relationship between two routers in a multicast architecture.</span></span>

![relación entre dos enrutadores en la arquitectura de multidifusión](images/mrarch2.png)

<span data-ttu-id="042ee-114">En la ilustración anterior, el enrutador 2 envía un mensaje de multidifusión a la red 2 en la interfaz 3.</span><span class="sxs-lookup"><span data-stu-id="042ee-114">In the previous illustration, Router 2 sends a multicast message to Network 2 on Interface 3.</span></span> <span data-ttu-id="042ee-115">El enrutador 1 recibe el mensaje de multidifusión de la red 2 en la interfaz 3.</span><span class="sxs-lookup"><span data-stu-id="042ee-115">Router 1 receives the multicast message from Network 2 on Interface 3.</span></span> <span data-ttu-id="042ee-116">En ambos enrutadores, el protocolo 3 es el propietario de la interfaz correspondiente 3.</span><span class="sxs-lookup"><span data-stu-id="042ee-116">On both routers, Protocol 3 owns the respective Interface 3.</span></span>

<span data-ttu-id="042ee-117">En la ilustración siguiente se muestra la ruta de acceso a un mensaje de un origen de multidifusión (a un grupo de multidifusión) que se toma para alcanzar el host que se ha unido al grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="042ee-117">The following illustration shows the path a message from a multicast source (to a multicast group) takes to reach the host that has joined the multicast group.</span></span> <span data-ttu-id="042ee-118">Los enrutadores de la ilustración usan la misma configuración que las ilustraciones anteriores; sin embargo, no se muestran los detalles de la interfaz y el protocolo para que la figura sea simple.</span><span class="sxs-lookup"><span data-stu-id="042ee-118">The routers in the illustration use the same configuration as previous illustrations; however, the interface and protocol details are not shown in order to keep the figure simple.</span></span>

![Ruta de acceso del mensaje del origen de multidifusión al host de destino](images/mrarch3.png)

<span data-ttu-id="042ee-120">En el siguiente escenario se describen los eventos que tienen lugar cuando un host se une a un grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="042ee-120">The following scenario describes the events that take place when a host joins a multicast group.</span></span> <span data-ttu-id="042ee-121">Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.</span><span class="sxs-lookup"><span data-stu-id="042ee-121">Refer to the previous illustration for relationships between the various entities.</span></span>

1.  <span data-ttu-id="042ee-122">El host 1 se une al grupo de multidifusión G en la red 3.</span><span class="sxs-lookup"><span data-stu-id="042ee-122">Host 1 joins the multicast group G on Network 3.</span></span>
2.  <span data-ttu-id="042ee-123">El enrutador 3 aprende sobre G a través de IGMP.</span><span class="sxs-lookup"><span data-stu-id="042ee-123">Router 3 learns about G via IGMP.</span></span>
3.  <span data-ttu-id="042ee-124">El administrador del grupo de multidifusión en el enrutador 3 notifica al protocolo 3 del enrutador 3 que hay nuevos receptores para G.</span><span class="sxs-lookup"><span data-stu-id="042ee-124">The multicast group manager on Router 3 notifies Protocol 3 on Router 3 that there are new receivers for G.</span></span>
4.  <span data-ttu-id="042ee-125">Después, el protocolo 3 en el enrutador 3 notifica al protocolo 3 del enrutador 1 acerca de G.</span><span class="sxs-lookup"><span data-stu-id="042ee-125">Protocol 3 on Router 3 then notifies Protocol 3 on Router 1 about G.</span></span>
5.  <span data-ttu-id="042ee-126">A su vez, el protocolo 3 en el enrutador 1 notifica al administrador del grupo de multidifusión en el enrutador 1 acerca de G.</span><span class="sxs-lookup"><span data-stu-id="042ee-126">In turn, Protocol 3 on Router 1 notifies the multicast group manager on Router 1 about G.</span></span>
6.  <span data-ttu-id="042ee-127">A continuación, el administrador del grupo de multidifusión en el enrutador 1 notifica al protocolo 1 y al protocolo 2 acerca de G.</span><span class="sxs-lookup"><span data-stu-id="042ee-127">The multicast group manager on Router 1 then notifies Protocol 1 and Protocol 2 about G.</span></span>
7.  <span data-ttu-id="042ee-128">El protocolo 2 puede informar al enrutador 2 acerca de G si el protocolo está diseñado para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="042ee-128">Protocol 2 may inform Router 2 about G, if the protocol is designed to do so.</span></span>

<span data-ttu-id="042ee-129">En el siguiente escenario se describen los eventos que tienen lugar cuando se envía un mensaje a un grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="042ee-129">The following scenario describes the events that take place when a message is sent to a multicast group.</span></span> <span data-ttu-id="042ee-130">Consulte la ilustración anterior para ver las relaciones entre las distintas entidades.</span><span class="sxs-lookup"><span data-stu-id="042ee-130">Refer to the previous illustration for the relationships between the various entities.</span></span>

1.  <span data-ttu-id="042ee-131">Un origen de la red 1 envía un mensaje al grupo G.</span><span class="sxs-lookup"><span data-stu-id="042ee-131">A source on Network 1 sends a message to Group G.</span></span>
2.  <span data-ttu-id="042ee-132">El mensaje enviado desde los orígenes S va primero al enrutador 2, que, a continuación, lo reenvía al enrutador 1 mediante la interfaz 2 (ya que el protocolo 2 ha informado de que los receptores están en el nivel inferior).</span><span class="sxs-lookup"><span data-stu-id="042ee-132">The message sent from Source S goes first to Router 2, which then forwards it to Router 1 using Interface 2 (since Router 2 has been informed by Protocol 2 that receivers are present downstream).</span></span>
3.  <span data-ttu-id="042ee-133">El enrutador 1 reenvía el mensaje al enrutador 3 (puesto que el protocolo 2 ha informado de que el enrutador 1 es el mismo que el que los receptores están presentes).</span><span class="sxs-lookup"><span data-stu-id="042ee-133">Router 1 forwards the message to Router 3 (since Router 1 has been informed by Protocol 2 that receivers are present downstream).</span></span>
4.  <span data-ttu-id="042ee-134">El enrutador 3 reenvía el mensaje a la red 3 y, por tanto, llega al host 1.</span><span class="sxs-lookup"><span data-stu-id="042ee-134">Router 3 forwards the message to Network 3, and therefore it arrives at Host 1.</span></span>

<span data-ttu-id="042ee-135">Para obtener más información sobre la interacción del Protocolo de enrutamiento de multidifusión, consulte [RFC 2715](routing-protocols-request-for-comments.md), reglas de interoperabilidad para los protocolos de enrutamiento de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="042ee-135">For further information on multicast routing protocol interaction, see [RFC 2715](routing-protocols-request-for-comments.md), Interoperability Rules for Multicast Routing Protocols.</span></span>

 

 




