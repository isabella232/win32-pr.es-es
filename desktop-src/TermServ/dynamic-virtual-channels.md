---
title: Canales virtuales dinámicos
description: Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418657"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="4b606-103">Canales virtuales dinámicos</span><span class="sxs-lookup"><span data-stu-id="4b606-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="4b606-104">Las API de canal virtual dinámico (DVC) amplían las API de canal virtual existentes para Servicios de Escritorio remoto, conocidas como API de canal virtual estático (SVC).</span><span class="sxs-lookup"><span data-stu-id="4b606-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="4b606-105">Las API de DVC abordan varias limitaciones que existían en las API de SVC entre el cliente y el servidor, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4b606-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="4b606-106">Un número limitado de canales</span><span class="sxs-lookup"><span data-stu-id="4b606-106">A limited number of channels</span></span>
-   <span data-ttu-id="4b606-107">Reconstrucción de paquetes</span><span class="sxs-lookup"><span data-stu-id="4b606-107">Packet reconstruction</span></span>

<span data-ttu-id="4b606-108">Las API de DVC le ayudarán a implementar módulos en el lado servidor y cliente de una conexión Servicios de Escritorio remoto que se comunican entre sí.</span><span class="sxs-lookup"><span data-stu-id="4b606-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="4b606-109">Al igual que muchas otras arquitecturas de cliente/servidor, se establece una conexión basada en un elemento de datos acordado comúnmente, denominado punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b606-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="4b606-110">Un ejemplo similar es TCP/IP, donde un punto de conexión se establece a través de una combinación de dirección IP del servidor y el nombre del puerto.</span><span class="sxs-lookup"><span data-stu-id="4b606-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="4b606-111">Otro ejemplo son las canalizaciones con nombre, donde un punto de conexión es una combinación del nombre del servidor y el nombre de la canalización.</span><span class="sxs-lookup"><span data-stu-id="4b606-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="4b606-112">En una conexión Servicios de Escritorio remoto solo hay dos lados implicados.</span><span class="sxs-lookup"><span data-stu-id="4b606-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="4b606-113">Por lo tanto, el punto de conexión consta de una cadena arbitraria simple que identifica la conexión de forma única.</span><span class="sxs-lookup"><span data-stu-id="4b606-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="4b606-114">Al igual que TCP/IP y las canalizaciones con nombre, se pueden iniciar varias conexiones desde el mismo nombre de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b606-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="4b606-115">En ese sentido, las conexiones no tienen nombres; solo un agente de escucha que espera las solicitudes entrantes en el extremo.</span><span class="sxs-lookup"><span data-stu-id="4b606-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="4b606-116">Las API de DVC se componen de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4b606-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="4b606-117">API de cliente</span><span class="sxs-lookup"><span data-stu-id="4b606-117">Client APIs</span></span>

    <span data-ttu-id="4b606-118">Estas API están disponibles en el cliente de Conexión a Escritorio remoto (RDC) como complemento.</span><span class="sxs-lookup"><span data-stu-id="4b606-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="4b606-119">El lado cliente está en modo pasivo, donde escucha las conexiones entrantes, pero no establece activamente una conexión.</span><span class="sxs-lookup"><span data-stu-id="4b606-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="4b606-120">API de servidor</span><span class="sxs-lookup"><span data-stu-id="4b606-120">Server APIs</span></span>

    <span data-ttu-id="4b606-121">Estas API inician activamente la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b606-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="4b606-122">Para obtener información sobre cómo escribir un módulo de canal virtual dinámico (DVC), consulte los [detalles de implementación de DVC](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="4b606-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




