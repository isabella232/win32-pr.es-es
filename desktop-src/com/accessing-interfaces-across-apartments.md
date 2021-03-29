---
title: Acceso a interfaces entre apartamentos
description: Acceso a interfaces entre apartamentos
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774796"
---
# <a name="accessing-interfaces-across-apartments"></a><span data-ttu-id="ebaa4-103">Acceso a interfaces entre apartamentos</span><span class="sxs-lookup"><span data-stu-id="ebaa4-103">Accessing Interfaces Across Apartments</span></span>

<span data-ttu-id="ebaa4-104">COM proporciona una manera para cualquier apartamento de un proceso de obtener acceso a una interfaz implementada en un objeto de cualquier otro apartamento del proceso.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-104">COM provides a way for any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.</span></span> <span data-ttu-id="ebaa4-105">Esto se realiza a través de la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="ebaa4-105">This is done through the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="ebaa4-106">Esta interfaz tiene tres métodos, que le permiten hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ebaa4-106">This interface has three methods, which allow you to do the following:</span></span>

-   <span data-ttu-id="ebaa4-107">Registre una interfaz como una interfaz *global* (processwide).</span><span class="sxs-lookup"><span data-stu-id="ebaa4-107">Register an interface as a *global* (processwide) interface.</span></span>
-   <span data-ttu-id="ebaa4-108">Obtiene un puntero a la interfaz de cualquier otro apartamento a través de una cookie.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-108">Get a pointer to that interface from any other apartment through a cookie.</span></span>
-   <span data-ttu-id="ebaa4-109">Revocar el registro global de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-109">Revoke the global registration of an interface.</span></span>

<span data-ttu-id="ebaa4-110">La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) es una manera eficaz de que un proceso almacene un puntero de interfaz en una ubicación de memoria a la que se puede tener acceso desde varios apartamentos dentro del proceso, como variables para todo el proceso y objetos *ágiles* (objetos de cálculo de referencias de subprocesamiento libre) que contienen punteros de interfaz a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-110">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as process-wide variables and *agile* objects (free-threaded, marshaled objects) containing interface pointers to other objects.</span></span>

<span data-ttu-id="ebaa4-111">Un objeto Agile no es consciente de la infraestructura COM subyacente en la que se ejecuta; en otras palabras, en qué apartamento, contexto y subproceso se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-111">An agile object is unaware of the underlying COM infrastructure in which it runs; in other words, what apartment, context, and thread it is executing on.</span></span> <span data-ttu-id="ebaa4-112">El objeto puede estar reteniendo en interfaces que son específicas de un apartamento o un contexto.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-112">The object may be holding on to interfaces that are specific to an apartment or context.</span></span> <span data-ttu-id="ebaa4-113">Por esta razón, llamar a estas interfaces desde donde se ejecuta el componente ágil podría no funcionar siempre correctamente.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-113">For this reason, calling these interfaces from wherever the agile component is executing might not always work properly.</span></span> <span data-ttu-id="ebaa4-114">La tabla de interfaz global evita este problema garantizando que se usa un proxy válido (o puntero directo) al objeto, en función de dónde se esté ejecutando el objeto Agile.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-114">The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.</span></span>

> [!Note]  
> <span data-ttu-id="ebaa4-115">La tabla de interfaz global no es portable en los límites del proceso o del equipo, por lo que no se puede utilizar en lugar del mecanismo normal de paso de parámetros.</span><span class="sxs-lookup"><span data-stu-id="ebaa4-115">The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.</span></span>

 

<span data-ttu-id="ebaa4-116">Para obtener información sobre la creación y el uso de una tabla de interfaz global, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ebaa4-116">For information about creating and using a global interface table, see the following topics:</span></span>

-   [<span data-ttu-id="ebaa4-117">Crear la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="ebaa4-117">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
-   [<span data-ttu-id="ebaa4-118">Cuándo usar la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="ebaa4-118">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a><span data-ttu-id="ebaa4-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebaa4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebaa4-120">Elegir el modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="ebaa4-120">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="ebaa4-121">Apartamentos multiproceso</span><span class="sxs-lookup"><span data-stu-id="ebaa4-121">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="ebaa4-122">Problemas de subprocesos de servidor en proceso</span><span class="sxs-lookup"><span data-stu-id="ebaa4-122">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="ebaa4-123">Procesos, subprocesos y apartamentos</span><span class="sxs-lookup"><span data-stu-id="ebaa4-123">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="ebaa4-124">Comunicación multiproceso y de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="ebaa4-124">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="ebaa4-125">Apartamentos de un solo subproceso</span><span class="sxs-lookup"><span data-stu-id="ebaa4-125">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




