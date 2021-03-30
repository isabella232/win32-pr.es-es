---
description: Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento. Un contenedor es una colección de contextos contenidos en un proceso.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de subprocesos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "103819842"
---
# <a name="com-threading-models"></a><span data-ttu-id="f6466-104">Modelos de subprocesos COM+</span><span class="sxs-lookup"><span data-stu-id="f6466-104">COM+ Threading Models</span></span>

<span data-ttu-id="f6466-105">Los modelos de subprocesos COM+ están diseñados en torno a una colección de objetos denominada apartamento.</span><span class="sxs-lookup"><span data-stu-id="f6466-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="f6466-106">Un contenedor es una colección de contextos contenidos en un proceso, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="f6466-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Diagrama que muestra una colección de contextos en una actividad, dentro de un apartamento, dentro de un proceso.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="f6466-108">Las llamadas dentro de un contenedor son directas, mientras que las llamadas entre apartamentos (fuera de proceso) son indirectas y requieren código de proxy y código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f6466-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="f6466-109">Los apartamentos permiten objetos con diferentes propiedades de sincronización y reentrada y tienen dos categorías: de un solo subproceso y multiproceso.</span><span class="sxs-lookup"><span data-stu-id="f6466-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="f6466-110">Los objetos de un contenedor uniproceso (STA) se ejecutan en el subproceso determinado en el que se crearon.</span><span class="sxs-lookup"><span data-stu-id="f6466-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="f6466-111">Sta permite que solo se ejecute un método a la vez.</span><span class="sxs-lookup"><span data-stu-id="f6466-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="f6466-112">Están diseñados para las interfaces de usuario y se basan en la cola de mensajes de Microsoft Windows para procesar las llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="f6466-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="f6466-113">Los objetos de un contenedor multiproceso (MTA) se ejecutan en cualquier subproceso y permiten que se produzca cualquier número de métodos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="f6466-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="f6466-114">Los MTA admiten la reentrada implícitamente.</span><span class="sxs-lookup"><span data-stu-id="f6466-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="f6466-115">Las clases COM+ se marcan con una propiedad **ThreadingModel** que permite a com+ crear el objeto en el apartamento adecuado.</span><span class="sxs-lookup"><span data-stu-id="f6466-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="f6466-116">Para determinar en qué apartamento se crea un objeto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa la propiedad **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="f6466-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="f6466-117">Los subprocesos deben llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para poder usar com+.</span><span class="sxs-lookup"><span data-stu-id="f6466-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="f6466-118">Esto los crea dentro del apartamento y el contexto correctos.</span><span class="sxs-lookup"><span data-stu-id="f6466-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="f6466-119">Se determina que el apartamento del subproceso principal es el primer STA llamado por **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="f6466-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="f6466-120">Normalmente se asocia con el subproceso principal de un proceso.</span><span class="sxs-lookup"><span data-stu-id="f6466-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="f6466-121">**CoInitializeEx** indica el tipo de Apartamento requerido por el subproceso mediante el establecimiento de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f6466-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="f6466-122">**COinit \_ Multithreaded**: localiza el subproceso en el apartamento multiproceso único.</span><span class="sxs-lookup"><span data-stu-id="f6466-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="f6466-123">**COinit \_ APARTMENTTHREADED**: coloca el subproceso en un nuevo STA.</span><span class="sxs-lookup"><span data-stu-id="f6466-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="f6466-124">En los siguientes temas de esta sección se proporciona más información acerca del uso de los modelos de subprocesos y apartamentos en COM+:</span><span class="sxs-lookup"><span data-stu-id="f6466-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="f6466-125">Atributo del modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="f6466-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="f6466-126">Apartamentos neutros</span><span class="sxs-lookup"><span data-stu-id="f6466-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="f6466-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6466-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6466-128">Procesos, subprocesos y apartamentos</span><span class="sxs-lookup"><span data-stu-id="f6466-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="f6466-129">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="f6466-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
