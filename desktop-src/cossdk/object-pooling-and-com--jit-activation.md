---
description: La activación JIT de COM+ se pone en peligro entre los clientes expansivos y los servidores expansivos con el fin de obtener un rendimiento óptimo. Los clientes obtienen referencias a objetos, mientras que los servidores pueden administrar con mayor precisión el uso de memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Agrupación de objetos y activación JIT de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423491"
---
# <a name="object-pooling-and-com-jit-activation"></a><span data-ttu-id="84fb8-104">Agrupación de objetos y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="84fb8-104">Object Pooling and COM+ JIT Activation</span></span>

<span data-ttu-id="84fb8-105">La activación JIT de COM+ se pone en peligro entre los clientes expansivos y los servidores expansivos con el fin de obtener un rendimiento óptimo.</span><span class="sxs-lookup"><span data-stu-id="84fb8-105">COM+ JIT activation essentially strikes a compromise between greedy clients and greedy servers for the sake of getting optimal performance.</span></span> <span data-ttu-id="84fb8-106">Los clientes obtienen referencias a objetos, mientras que los servidores pueden administrar con mayor precisión el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="84fb8-106">Clients get to keep object references, while servers can more closely manage memory utilization.</span></span>

<span data-ttu-id="84fb8-107">Puede refinar aún más mediante el uso de la [agrupación de objetos com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="84fb8-107">You can refine this further by using [COM+ Object Pooling](com--object-pooling.md).</span></span> <span data-ttu-id="84fb8-108">Al agrupar los objetos que están activados con JIT, puede dedicar una determinada cantidad de memoria para almacenar un cierto número de objetos activos en la memoria, listos para su reutilización inmediata.</span><span class="sxs-lookup"><span data-stu-id="84fb8-108">By pooling objects that are JIT activated, you can dedicate a certain amount of memory to hold a certain number of objects active in memory, ready for immediate reuse.</span></span> <span data-ttu-id="84fb8-109">Esto resulta más útil cuando los objetos son caros de crear, como en el caso de que contengan varios recursos.</span><span class="sxs-lookup"><span data-stu-id="84fb8-109">This makes the most sense when objects are expensive to create, as in the case where they hold multiple resources.</span></span>

<span data-ttu-id="84fb8-110">Agrupar objetos activados con JIT de esta manera, puede lograr las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="84fb8-110">Pooling JIT-activated objects in this manner, you can achieve the following benefits:</span></span>

-   <span data-ttu-id="84fb8-111">Tiempos de reactivación de objetos muy acelerados.</span><span class="sxs-lookup"><span data-stu-id="84fb8-111">Greatly accelerated object reactivation times.</span></span>
-   <span data-ttu-id="84fb8-112">Reutilización de los recursos caros que contienen los objetos.</span><span class="sxs-lookup"><span data-stu-id="84fb8-112">Reuse of any expensive resources the objects are holding.</span></span>
-   <span data-ttu-id="84fb8-113">Un control más preciso de la memoria y el uso de recursos para los objetos agrupados.</span><span class="sxs-lookup"><span data-stu-id="84fb8-113">More precise governing of memory and resource use for the pooled objects.</span></span>
-   <span data-ttu-id="84fb8-114">Retención de flexibilidad administrativa para que la aplicación pueda escalar para usar los recursos disponibles y adaptarse al cambio de los requisitos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="84fb8-114">Retention of administrative flexibility so that your application can scale to use available resources and adapt to changing performance requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84fb8-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84fb8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84fb8-116">Conceptos de activación Just-in-Time de COM+</span><span class="sxs-lookup"><span data-stu-id="84fb8-116">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="84fb8-117">Agrupación de objetos COM+</span><span class="sxs-lookup"><span data-stu-id="84fb8-117">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="84fb8-118">Habilitar la activación JIT para un componente</span><span class="sxs-lookup"><span data-stu-id="84fb8-118">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="84fb8-119">Transacciones y activación JIT de COM+</span><span class="sxs-lookup"><span data-stu-id="84fb8-119">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



