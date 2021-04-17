---
description: La API de gráficos del mismo nivel permite a las aplicaciones pasar datos entre pares de manera eficaz y confiable. Los conceptos básicos de la tecnología de gráficos del mismo nivel son los nodos de un grafo del mismo nivel y los avisos de eventos.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Acerca de la API de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667463"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="9d1bd-104">Acerca de la API de gráficos</span><span class="sxs-lookup"><span data-stu-id="9d1bd-104">About the Graphing API</span></span>

<span data-ttu-id="9d1bd-105">La API de gráficos del mismo nivel permite a las aplicaciones pasar datos entre pares de manera eficaz y confiable.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="9d1bd-106">Los conceptos básicos de la tecnología de gráficos del mismo nivel son los **nodos** de un grafo del mismo nivel y los avisos de eventos.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="9d1bd-107">Nodos</span><span class="sxs-lookup"><span data-stu-id="9d1bd-107">Nodes</span></span>

<span data-ttu-id="9d1bd-108">Un nodo representa una instancia específica de un elemento del mismo nivel en una red.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="9d1bd-109">La infraestructura de la API de gráficos del mismo nivel garantiza que cada nodo tiene una vista coherente de los datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="9d1bd-110">Un nodo tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="9d1bd-110">A node has the following features:</span></span>

-   <span data-ttu-id="9d1bd-111">Puede conectarse a un nodo diferente y formar una red interrelacionada denominada grafo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="9d1bd-112">Puede compartir datos con otros nodos de un gráfico en forma de [registro](records.md).</span><span class="sxs-lookup"><span data-stu-id="9d1bd-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="9d1bd-113">Puede crear conexiones directas independientes de los gráficos del mismo nivel establecidos mediante la [API de agrupación](about-the-grouping-api.md)del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="9d1bd-114">Las conexiones directas permiten a los nodos enviar datos privados entre sí.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="9d1bd-115">Avisos de eventos</span><span class="sxs-lookup"><span data-stu-id="9d1bd-115">Event Notices</span></span>

<span data-ttu-id="9d1bd-116">La API de gráficos del mismo nivel tiene una infraestructura de eventos que permite a una aplicación registrar y recibir un aviso de un evento del mismo nivel dentro de la infraestructura de la API de gráficos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="9d1bd-117">Cuando algo cambia dentro de un gráfico del mismo nivel, una aplicación envía un aviso de eventos para identificar que se ha producido un cambio.</span><span class="sxs-lookup"><span data-stu-id="9d1bd-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



