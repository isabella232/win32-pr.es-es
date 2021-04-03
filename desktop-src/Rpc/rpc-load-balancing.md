---
title: Equilibrio de carga de RPC
description: Equilibrio de carga de RPC
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075165"
---
# <a name="rpc-load-balancing"></a><span data-ttu-id="8b13e-103">Equilibrio de carga de RPC</span><span class="sxs-lookup"><span data-stu-id="8b13e-103">RPC Load Balancing</span></span>

<span data-ttu-id="8b13e-104">El equilibrio de carga de Microsoft RPC está diseñado para proporcionar una solución escalable para escenarios en los que se exige una carga elevada de tráfico de [RPC a través de http](remote-procedure-calls-using-rpc-over-http.md) .</span><span class="sxs-lookup"><span data-stu-id="8b13e-104">Microsoft RPC Load Balancing is intended to provide a scalable solution for scenarios which demand a high load of [RPC over HTTP](remote-procedure-calls-using-rpc-over-http.md) traffic.</span></span> <span data-ttu-id="8b13e-105">El objetivo principal del Load Balancer RPC es asegurarse de que una granja de servidores puede atender el tráfico RPC/HTTP para mejorar la escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="8b13e-105">The RPC Load Balancer’s primary purpose is to ensure RPC/HTTP traffic can be serviced by a server farm to improve scalability.</span></span> <span data-ttu-id="8b13e-106">Para ello, RPC debe asegurarse de que el mismo punto de conexión de servidor en la granja de servidores presta servicio a todas las conexiones de un proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="8b13e-106">To achieve this, RPC must ensure that all connections from a client process are serviced by the same server endpoint in the server farm.</span></span> <span data-ttu-id="8b13e-107">La Load Balancer RPC se implementa como un servicio que se ejecuta junto con el servicio de proxy RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b13e-107">The RPC Load Balancer is implemented as a service which runs in conjunction with the RPC over HTTP Proxy service.</span></span>

<span data-ttu-id="8b13e-108">Para habilitar el equilibrio de carga, el servicio de equilibrio de carga de RPC que se ejecuta en cada uno de los servidores se comunica entre sí para determinar el servidor preferido para la conexión de cliente inicial.</span><span class="sxs-lookup"><span data-stu-id="8b13e-108">To enable load balancing, the RPC Load Balancing service running on each of the servers communicates with each other to determine the preferred server for the initial client connection.</span></span> <span data-ttu-id="8b13e-109">Este proceso se denomina arbitraje y se produce en el momento de la conexión inicial del cliente.</span><span class="sxs-lookup"><span data-stu-id="8b13e-109">This process is called arbitration and it occurs at the time of the initial client connection.</span></span> <span data-ttu-id="8b13e-110">Para reducir el tráfico entre servidores, el servicio de equilibrio de carga de RPC elige el extremo local para atender la conexión si el cliente no está ya asociado a un servidor.</span><span class="sxs-lookup"><span data-stu-id="8b13e-110">To reduce cross server traffic, the RPC Load Balancing service chooses the local endpoint to service the connection if the client is not already associated with a server.</span></span> <span data-ttu-id="8b13e-111">Para una conexión de cliente determinada, el resultado del arbitraje es una de estas dos posibilidades:</span><span class="sxs-lookup"><span data-stu-id="8b13e-111">For a given client connection, the outcome of arbitration is one of two possibilities:</span></span>

-   <span data-ttu-id="8b13e-112">Si el cliente ya ha realizado una conexión, el servidor que debe recibir la conexión por primera vez controlará las conexiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8b13e-112">If the client has already made a connection, the server to first receive the connection will handle the subsequent connections.</span></span>
-   <span data-ttu-id="8b13e-113">Si esta es la primera conexión desde el cliente, el arbitraje dará lugar al servidor local que controla la conexión y, por tanto, a todas las conexiones del cliente.</span><span class="sxs-lookup"><span data-stu-id="8b13e-113">If this is the first connection from the client, arbitration will result in the local server handling the connection, and thus all connections from the client.</span></span> <span data-ttu-id="8b13e-114">Esta información, una vez determinada, se confirmará en los otros servicios de Load Balancer de RPC de la granja de servidores, lo que les informará del servidor que controla todas las solicitudes del cliente.</span><span class="sxs-lookup"><span data-stu-id="8b13e-114">This information, once determined, will be committed to the other RPC Load Balancer services in the server farm, thus informing them of the server handling all of the client’s requests.</span></span>

<span data-ttu-id="8b13e-115">En esta sección se proporciona información general sobre el equilibrio de carga de RPC en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b13e-115">This section provides an overview of RPC Load Balancing in the following topics:</span></span>

-   [<span data-ttu-id="8b13e-116">Implementar el equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="8b13e-116">Deploying Load Balancing</span></span>](deploying-load-balancing.md)
-   [<span data-ttu-id="8b13e-117">Configurar el equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="8b13e-117">Configuring Load Balancing</span></span>](configuring-load-balancing.md)
-   [<span data-ttu-id="8b13e-118">Prácticas recomendadas de equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="8b13e-118">Load Balancing Best Practices</span></span>](load-balancing-best-practices.md)

## <a name="requirements"></a><span data-ttu-id="8b13e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b13e-119">Requirements</span></span>

<span data-ttu-id="8b13e-120">El servicio de equilibrio de carga de RPC es compatible con los servidores que ejecutan Windows Server 2008 R2 o posterior y los clientes que ejecutan Windows 7 o versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="8b13e-120">The RPC Load Balancing service is supported on servers running Windows Server 2008 R2 or later and clients running Windows 7 or later versions of Windows.</span></span>

<span data-ttu-id="8b13e-121">El servicio de proxy RPC, el servicio de equilibrio de carga de RPC y los puntos de conexión de servidor deben ejecutarse en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="8b13e-121">The RPC Proxy service, the RPC Load Balancing service and the server endpoints must all be running on the same machine.</span></span> <span data-ttu-id="8b13e-122">Además, todos los servidores de la granja de servidores deben ser capaces de atender el punto de conexión solicitado.</span><span class="sxs-lookup"><span data-stu-id="8b13e-122">Additionally, all servers in the server farm must be capable of servicing the requested endpoint.</span></span> <span data-ttu-id="8b13e-123">Para obtener información sobre la configuración del servicio de proxy RPC y el servicio de equilibrio de carga de RPC, vea [configurar equipos para RPC a través de http](configuring-computers-for-rpc-over-http.md) y [configurar el equilibrio de carga](configuring-load-balancing.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8b13e-123">For information on configuring the RPC Proxy service and the RPC Load Balancing service, see [Configuring Computers for RPC over HTTP](configuring-computers-for-rpc-over-http.md) and [Configuring Load Balancing](configuring-load-balancing.md), respectively.</span></span>

## <a name="limitations"></a><span data-ttu-id="8b13e-124">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="8b13e-124">Limitations</span></span>

<span data-ttu-id="8b13e-125">En este momento, el equilibrio de carga RPC solo admite una granja de servidores por recurso.</span><span class="sxs-lookup"><span data-stu-id="8b13e-125">At this time, RPC Load Balancing supports only one server farm per resource.</span></span> <span data-ttu-id="8b13e-126">Todos los servidores de todas las granjas de servidores deben ser capaces de atender también todos los recursos.</span><span class="sxs-lookup"><span data-stu-id="8b13e-126">All servers in all server farms must be capable of servicing all resources as well.</span></span>

 

 




