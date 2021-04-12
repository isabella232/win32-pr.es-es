---
title: Single-Threaded y comunicación multiproceso
description: Single-Threaded y comunicación multiproceso
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356929"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="169ea-103">Single-Threaded y comunicación multiproceso</span><span class="sxs-lookup"><span data-stu-id="169ea-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="169ea-104">Un cliente o servidor que admita apartamentos de un solo subproceso y multiproceso tendrá un apartamento multiproceso, que contiene todos los subprocesos inicializados como de subprocesamiento libre y uno o más apartamentos de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="169ea-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="169ea-105">Se deben calcular las referencias de los punteros de interfaz entre apartamentos, pero se pueden usar sin serialización dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="169ea-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="169ea-106">COM sincronizará las llamadas a los objetos de un contenedor uniproceso.</span><span class="sxs-lookup"><span data-stu-id="169ea-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="169ea-107">COM no sincronizará las llamadas a los objetos del apartamento multiproceso.</span><span class="sxs-lookup"><span data-stu-id="169ea-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="169ea-108">Toda la información sobre apartamentos de un solo subproceso se aplica a los subprocesos marcados como modelo de apartamento y toda la información sobre apartamentos multiproceso se aplica a todos los subprocesos marcados como de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="169ea-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="169ea-109">Las reglas de subprocesos de apartamento se aplican a la comunicación entre apartamentos, que requiere que se calculen las referencias de los punteros de interfaz entre apartamentos con llamadas a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) y [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), tal y como se describe en [apartamentos de un solo subproceso](single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="169ea-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="169ea-110">Se aplican algunas consideraciones especiales cuando se trabaja con servidores en proceso.</span><span class="sxs-lookup"><span data-stu-id="169ea-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="169ea-111">Para obtener más información, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="169ea-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="169ea-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="169ea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="169ea-113">Acceso a interfaces entre apartamentos</span><span class="sxs-lookup"><span data-stu-id="169ea-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="169ea-114">Elegir el modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="169ea-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="169ea-115">Apartamentos multiproceso</span><span class="sxs-lookup"><span data-stu-id="169ea-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="169ea-116">Problemas de subprocesos de servidor en proceso</span><span class="sxs-lookup"><span data-stu-id="169ea-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="169ea-117">Procesos, subprocesos y apartamentos</span><span class="sxs-lookup"><span data-stu-id="169ea-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="169ea-118">Apartamentos de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="169ea-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




