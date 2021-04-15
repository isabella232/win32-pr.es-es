---
title: Elegir el modelo de subprocesos
description: Elegir el modelo de subprocesos
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419101"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="09927-103">Elegir el modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="09927-103">Choosing the Threading Model</span></span>

<span data-ttu-id="09927-104">La elección del modelo de subprocesos para un objeto depende de la función del objeto.</span><span class="sxs-lookup"><span data-stu-id="09927-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="09927-105">Un objeto que realiza operaciones de e/s extensas podría admitir el subprocesamiento libre para proporcionar la respuesta máxima a los clientes al permitir llamadas de interfaz durante la latencia de e/s.</span><span class="sxs-lookup"><span data-stu-id="09927-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="09927-106">Por otro lado, un objeto que interactúe con el usuario podría admitir el subprocesamiento de apartamento para sincronizar las llamadas COM entrantes con sus operaciones de ventana.</span><span class="sxs-lookup"><span data-stu-id="09927-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="09927-107">Es más fácil admitir el subprocesamiento de apartamento en apartamentos de un solo subproceso, ya que COM proporciona la sincronización por cada llamada.</span><span class="sxs-lookup"><span data-stu-id="09927-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="09927-108">Admitir el subprocesamiento libre es más difícil porque el objeto debe implementar la sincronización; sin embargo, la respuesta a los clientes puede ser mejor porque la sincronización se puede implementar para secciones de código más pequeñas.</span><span class="sxs-lookup"><span data-stu-id="09927-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09927-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09927-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09927-110">Acceso a interfaces entre apartamentos</span><span class="sxs-lookup"><span data-stu-id="09927-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="09927-111">Apartamentos multiproceso</span><span class="sxs-lookup"><span data-stu-id="09927-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="09927-112">Problemas de subprocesos de servidor en proceso</span><span class="sxs-lookup"><span data-stu-id="09927-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="09927-113">Procesos, subprocesos y apartamentos</span><span class="sxs-lookup"><span data-stu-id="09927-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="09927-114">Comunicación multiproceso y de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="09927-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="09927-115">Apartamentos de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="09927-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




