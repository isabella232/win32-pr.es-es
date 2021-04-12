---
title: Implementar el equilibrio de carga
description: Implementar el equilibrio de carga
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268566"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="925ec-103">Implementar el equilibrio de carga</span><span class="sxs-lookup"><span data-stu-id="925ec-103">Deploying Load Balancing</span></span>

<span data-ttu-id="925ec-104">A continuación se muestra el entorno de implementación típico y el caso de uso que se utiliza en el equilibrador de carga de RPC:</span><span class="sxs-lookup"><span data-stu-id="925ec-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![equilibrio de carga de RPC](images/rpc-load-balancing.png)

1.  <span data-ttu-id="925ec-106">El cliente RPC realiza una conexión RPC/HTTP con la granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="925ec-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="925ec-107">La conexión se reenvía a través de la red a un equilibrador de carga de front-end</span><span class="sxs-lookup"><span data-stu-id="925ec-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="925ec-108">El equilibrador de carga de front-end elige un servidor para atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="925ec-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="925ec-109">En este ejemplo, el equilibrador de carga de front-end reenvía la conexión al servidor 1.</span><span class="sxs-lookup"><span data-stu-id="925ec-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="925ec-110">El servicio del equilibrador de carga de RPC arbitra la conexión.</span><span class="sxs-lookup"><span data-stu-id="925ec-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="925ec-111">Determina que esta es la primera conexión desde el cliente y asocia la conexión con el servidor local, servidor 1.</span><span class="sxs-lookup"><span data-stu-id="925ec-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="925ec-112">El cliente realiza una segunda solicitud RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="925ec-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="925ec-113">La solicitud se reenvía a través de la red al equilibrador de carga de front-end.</span><span class="sxs-lookup"><span data-stu-id="925ec-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="925ec-114">El equilibrador de carga de front-end elige un servidor para atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="925ec-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="925ec-115">En este caso, el equilibrador de carga front-end elige el servidor 2 para atender la solicitud.</span><span class="sxs-lookup"><span data-stu-id="925ec-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="925ec-116">El servicio RPC Load Balancer arbitra la conexión.</span><span class="sxs-lookup"><span data-stu-id="925ec-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="925ec-117">Reconoce que el servidor 1 está realizando el mantenimiento de las conexiones de este cliente.</span><span class="sxs-lookup"><span data-stu-id="925ec-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="925ec-118">La conexión se reenvía al servidor 1.</span><span class="sxs-lookup"><span data-stu-id="925ec-118">The connection is forwarded to Server 1.</span></span>

 

 




