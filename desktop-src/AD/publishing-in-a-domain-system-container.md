---
title: Publicación en un contenedor de sistema de dominio
description: El contenedor System de una partición de dominio contiene información operativa por dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Publicación en un contenedor de sistema de dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903097"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="f2ea2-104">Publicación en un contenedor de sistema de dominio</span><span class="sxs-lookup"><span data-stu-id="f2ea2-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="f2ea2-105">El contenedor System de una partición de dominio contiene información operativa por dominio.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="f2ea2-106">Esto incluye la Directiva de seguridad local predeterminada, el seguimiento de vínculos de archivos, las reuniones de red y los contenedores para el registro y la resolución de Windows Sockets (RnR) y los puntos de conexión del servicio de nombres de RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="f2ea2-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="f2ea2-107">De forma predeterminada, el contenedor System está oculto y proporciona un lugar cómodo para almacenar objetos que son de interés para los administradores, pero no para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="f2ea2-108">Los servicios que no están vinculados a un solo host pueden querer crear sus SCP en el contenedor del sistema de una partición de dominio.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="f2ea2-109">Esta alternativa puede ser útil para los servicios con réplicas instaladas en varios hosts, cada réplica proporciona servicios idénticos a los clientes de todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="f2ea2-110">Permite agrupar todos los objetos del servicio replicado bajo un único contenedor.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="f2ea2-111">Los servicios que crean objetos específicos del servicio en el contenedor del sistema deben hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2ea2-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="f2ea2-112">Cree un subcontenedor de **contenedor** de clase de objeto como un elemento secundario inmediato del contenedor del sistema.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="f2ea2-113">Asigne a este subcontenedor un nombre que lo identifique claramente como perteneciente al servicio.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="f2ea2-114">Cree los objetos relacionados con el servicio en este subcontenedor.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="f2ea2-115">Por ejemplo, NetMeeting usa el contenedor reuniones para publicar objetos de reunión de red.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="f2ea2-116">Un proveedor con varios productos puede usar una estrategia similar para agrupar objetos relacionados con el servicio para todos sus productos.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="f2ea2-117">En este caso, podría crear un objeto **contenedor** con un nombre que identifique claramente al proveedor; a continuación, cree objetos de **contenedor** para cada servicio como elementos secundarios del contenedor del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="f2ea2-118">Cree el contenedor específico del proveedor como un elemento secundario del contenedor del sistema.</span><span class="sxs-lookup"><span data-stu-id="f2ea2-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




