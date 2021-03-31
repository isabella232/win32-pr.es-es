---
description: Tipos de subprocesos del dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de subprocesos del dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423276"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="313f5-103">Tipos de subprocesos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="313f5-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="313f5-104">Las llamadas a un dispensador de recursos COM+ pueden originarse en uno de los siguientes tipos de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="313f5-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="313f5-105">Subproceso de apartamento (STA)</span><span class="sxs-lookup"><span data-stu-id="313f5-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="313f5-106">Subproceso libre (MTA)</span><span class="sxs-lookup"><span data-stu-id="313f5-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="313f5-107">Subproceso no COM (subproceso de recolector de elementos no utilizados del [Administrador de dispensadores](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="313f5-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="313f5-108">Si un dispensador de recursos no es un objeto COM, debe ser capaz de controlar las llamadas que llegan desde cualquier subproceso en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="313f5-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="313f5-109">Si un dispensador de recursos es un objeto COM, el objeto COM se debe registrar con un modelo de subprocesos de **ambos**.</span><span class="sxs-lookup"><span data-stu-id="313f5-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="313f5-110">Esto permite a los subprocesos STA o MTA crear y usar el dispensador de recursos sin un conmutador de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="313f5-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="313f5-111">Si un dispensador de recursos crea y usa otro objeto COM (por ejemplo, un administrador de recursos fuera de proceso), es posible que el dispensador de recursos tenga que mantener varios servidores proxy en este otro objeto COM y asegurarse de que las llamadas al objeto se realizan utilizando el proxy adecuado para el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="313f5-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="313f5-112">Cuando el dispensador de recursos crea este objeto, calcula las referencias y guarda la referencia.</span><span class="sxs-lookup"><span data-stu-id="313f5-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="313f5-113">Antes de volver a llamar al objeto, se debe anular la serialización para crear un proxy para el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="313f5-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="313f5-114">Podría ser más eficaz almacenar en caché estos proxies por subproceso manteniendo una asignación del identificador de subproceso a un puntero proxy.</span><span class="sxs-lookup"><span data-stu-id="313f5-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="313f5-115">Esta asignación se expande a medida que se usan nuevos subprocesos en el proceso.</span><span class="sxs-lookup"><span data-stu-id="313f5-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="313f5-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="313f5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="313f5-117">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="313f5-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



