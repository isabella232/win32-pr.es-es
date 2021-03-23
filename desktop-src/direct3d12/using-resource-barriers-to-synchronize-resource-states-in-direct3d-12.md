---
title: Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12
description: Para reducir el uso general de la CPU y habilitar el procesamiento previo y multithreading del controlador, Direct3D 12 mueve la responsabilidad de la administración de Estados por recurso del controlador de gráficos a la aplicación.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549173"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="7051b-103">Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7051b-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="7051b-104">Para reducir el uso general de la CPU y habilitar el procesamiento previo y multithreading del controlador, Direct3D 12 mueve la responsabilidad de la administración de Estados por recurso del controlador de gráficos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7051b-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="7051b-105">Un ejemplo de estado por recurso es si se está accediendo actualmente a un recurso de textura a través de un sombreador Vista de recursos o como una vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="7051b-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="7051b-106">En Direct3D 11, los controladores eran necesarios para realizar el seguimiento de este estado en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7051b-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="7051b-107">Esto resulta caro desde la perspectiva de la CPU y complica significativamente cualquier tipo de diseño multiproceso.</span><span class="sxs-lookup"><span data-stu-id="7051b-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="7051b-108">En Microsoft Direct3D 12, la mayoría de los Estados por recurso se administra mediante la aplicación con una sola API, [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="7051b-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="7051b-109">Uso de la API de ResourceBarrier para administrar el estado de cada recurso</span><span class="sxs-lookup"><span data-stu-id="7051b-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="7051b-110">Estados de los recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="7051b-111">Estados iniciales de los recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="7051b-112">Restricciones de estado de recursos de lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7051b-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="7051b-113">Estados de los recursos para la presentación de búferes de reserva</span><span class="sxs-lookup"><span data-stu-id="7051b-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="7051b-114">Descartar recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="7051b-115">Transiciones de estado IMPLÍCITAS</span><span class="sxs-lookup"><span data-stu-id="7051b-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="7051b-116">Promoción de Estado común</span><span class="sxs-lookup"><span data-stu-id="7051b-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="7051b-117">Caída del estado a común</span><span class="sxs-lookup"><span data-stu-id="7051b-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="7051b-118">Implicaciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="7051b-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="7051b-119">Barreras divididas</span><span class="sxs-lookup"><span data-stu-id="7051b-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="7051b-120">Escenario de ejemplo de barrera de recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="7051b-121">Ejemplo de promoción de Estado común y decadencia</span><span class="sxs-lookup"><span data-stu-id="7051b-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="7051b-122">Ejemplo de barreras divididas</span><span class="sxs-lookup"><span data-stu-id="7051b-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="7051b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7051b-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="7051b-124">Uso de la API de ResourceBarrier para administrar el estado de cada recurso</span><span class="sxs-lookup"><span data-stu-id="7051b-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="7051b-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica al controlador de gráficos las situaciones en las que el controlador puede necesitar sincronizar varios accesos a la memoria en la que se almacena un recurso.</span><span class="sxs-lookup"><span data-stu-id="7051b-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="7051b-126">Se llama al método con una o más estructuras de descripción de barrera de recursos que indican el tipo de barrera de recursos que se declara.</span><span class="sxs-lookup"><span data-stu-id="7051b-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="7051b-127">Existen tres tipos de barreras de recursos:</span><span class="sxs-lookup"><span data-stu-id="7051b-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="7051b-128">**Barrera de transición** : una barrera de transición indica que un conjunto de Subrecursos realiza una transición entre distintos usos.</span><span class="sxs-lookup"><span data-stu-id="7051b-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="7051b-129">Una estructura de [**barrera de \_ transición de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) se usa para especificar el subrecurso que está cambiando, así como los Estados *antes* y *después* del subrecurso.</span><span class="sxs-lookup"><span data-stu-id="7051b-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="7051b-130">El sistema comprueba que las transiciones de subrecurso en una lista de comandos son coherentes con las transiciones anteriores en la misma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="7051b-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="7051b-131">El nivel de depuración realiza un seguimiento adicional del estado de los Subrecursos para buscar otros errores, pero esta validación es conservadora y no es exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="7051b-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="7051b-132">Tenga en cuenta que puede usar la \_ marca de la barrera de recursos D3D12 \_ \_ todos los \_ Subrecursos para especificar que se están realizando las transiciones de todos los Subrecursos de un recurso.</span><span class="sxs-lookup"><span data-stu-id="7051b-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="7051b-133">**Barrera de alias** : una barrera de alias indica una transición entre los usos de dos recursos diferentes que tienen asignaciones que se superponen en el mismo montón.</span><span class="sxs-lookup"><span data-stu-id="7051b-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="7051b-134">Esto se aplica a los recursos reservados y colocados.</span><span class="sxs-lookup"><span data-stu-id="7051b-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="7051b-135">Se utiliza una estructura de [**barrera de \_ alias de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) para especificar el recurso *Before* y el recurso *After* .</span><span class="sxs-lookup"><span data-stu-id="7051b-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="7051b-136">Tenga en cuenta que uno o ambos recursos pueden ser NULL, lo que indica que cualquier recurso en mosaico podría provocar el alias.</span><span class="sxs-lookup"><span data-stu-id="7051b-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="7051b-137">Para obtener más información sobre el uso de recursos en mosaico [, vea recursos en mosaico y](../direct3d11/tiled-resources.md) recursos en mosaico de [volumen](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7051b-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="7051b-138">**Barrera de vista de acceso desordenado (UAV)** : una barrera UAV indica que todos los accesos de UAV, tanto de lectura como de escritura, a un recurso determinado deben completarse entre cualquier acceso de UAV futuro, tanto de lectura como de escritura.</span><span class="sxs-lookup"><span data-stu-id="7051b-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="7051b-139">No es necesario que una aplicación ponga una barrera UAV entre dos llamadas a Draw o Dispatch que solo se leen de un UAV.</span><span class="sxs-lookup"><span data-stu-id="7051b-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="7051b-140">Además, no es necesario poner una barrera UAV entre dos llamadas a Draw o Dispatch que escriben en el mismo UAV si la aplicación sabe que es seguro ejecutar el acceso UAV en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="7051b-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="7051b-141">Se utiliza una estructura de [**\_ barrera de \_ UAV \_ de recursos D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) para especificar el recurso UAV al que se aplica la barrera.</span><span class="sxs-lookup"><span data-stu-id="7051b-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="7051b-142">La aplicación puede especificar NULL para el UAV de la barrera, lo que indica que cualquier acceso a UAV podría requerir la barrera.</span><span class="sxs-lookup"><span data-stu-id="7051b-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="7051b-143">Cuando se llama a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) con una matriz de descripciones de barrera de recursos, la API se comporta como si se hubiese llamado una vez para cada elemento, en el orden en el que se proporcionaron.</span><span class="sxs-lookup"><span data-stu-id="7051b-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="7051b-144">En un momento dado, un subrecurso está en exactamente un estado, determinado por el conjunto de marcas de [**\_ \_ Estados de recursos de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) proporcionadas a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="7051b-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="7051b-145">La aplicación debe asegurarse de que los Estados *antes* y *después* de las llamadas consecutivas a **ResourceBarrier** coinciden.</span><span class="sxs-lookup"><span data-stu-id="7051b-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="7051b-146">Las aplicaciones deben procesar por lotes varias transiciones en una llamada API siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="7051b-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="7051b-147">Estados de los recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-147">Resource states</span></span>

<span data-ttu-id="7051b-148">Para obtener una lista completa de los Estados de los recursos entre los que un recurso puede realizar una transición, vea el tema de referencia de la enumeración de [**\_ \_ Estados de recursos de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="7051b-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="7051b-149">En el caso de las barreras de recursos divididos, consulte también las [**marcas de barrera de recursos de D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="7051b-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="7051b-150">Estados iniciales de los recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-150">Initial states for resources</span></span>

<span data-ttu-id="7051b-151">Los recursos se pueden crear con cualquier estado inicial especificado por el usuario (válido para la descripción del recurso), con las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="7051b-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="7051b-152">Los montones de carga deben comenzar en el estado de recurso de D3D12 de \_ \_ \_ \_ lectura Generic Read que es una combinación OR bit a bit de:</span><span class="sxs-lookup"><span data-stu-id="7051b-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="7051b-153">D3D12 \_ \_ de estado \_ \_ de recurso \_ y \_ búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="7051b-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="7051b-154">\_Búfer de \_ Índice de estado de recurso de D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="7051b-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="7051b-155">\_Origen de \_ copia de estado de recurso de D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="7051b-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="7051b-156">\_Recurso de \_ \_ \_ \_ sombreador de estado de recursos sin píxeles de \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="7051b-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="7051b-157">\_Recurso de \_ \_ \_ sombreador de píxeles de estado \_ de recursos de D3D12</span><span class="sxs-lookup"><span data-stu-id="7051b-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="7051b-158">D3D12 \_ \_ \_ argumento indirecto de estado de recurso \_</span><span class="sxs-lookup"><span data-stu-id="7051b-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="7051b-159">Los montones de Readback deben comenzar en el estado de destino de la copia de estado de recursos de D3D12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="7051b-160">Los búferes de intercambio de cadena se inician automáticamente en el \_ \_ Estado común de los recursos de D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="7051b-161">Antes de que un montón pueda ser el destino de una operación de copia de GPU, normalmente primero se debe pasar el montón al \_ Estado de destino de copia de estado de recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="7051b-162">Sin embargo, los recursos creados en montones de carga deben comenzar en y no pueden cambiar desde el \_ Estado de lectura genérico, ya que solo la CPU va a escribir.</span><span class="sxs-lookup"><span data-stu-id="7051b-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="7051b-163">Por el contrario, los recursos confirmados creados en montones de READBACK deben comenzar en y no pueden cambiar desde el estado de destino de la copia \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="7051b-164">Restricciones de estado de recursos de lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7051b-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="7051b-165">Los bits de uso de estado de recursos que se usan para describir un estado de recurso se dividen en Estados de solo lectura y de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7051b-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="7051b-166">El tema de referencia para [**los \_ \_ Estados**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) de los recursos de D3D12 indica el nivel de acceso de lectura y escritura para cada bit de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="7051b-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="7051b-167">Como máximo, solo se puede establecer un bit de lectura/escritura para cualquier recurso.</span><span class="sxs-lookup"><span data-stu-id="7051b-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="7051b-168">Si se establece un bit de escritura, no se puede establecer ningún bit de solo lectura para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="7051b-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="7051b-169">Si no se establece ningún bit de escritura, se puede establecer cualquier número de bits de lectura.</span><span class="sxs-lookup"><span data-stu-id="7051b-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="7051b-170">Estados de los recursos para la presentación de búferes de reserva</span><span class="sxs-lookup"><span data-stu-id="7051b-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="7051b-171">Antes de que se presente un búfer de reserva, debe estar en \_ el \_ Estado común de los recursos de D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="7051b-172">Tenga en cuenta que el estado del recurso D3D12 de estado del recurso \_ \_ \_ es un sinónimo del \_ Estado del recurso D3D12 \_ \_ común y ambos tienen un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="7051b-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="7051b-173">Si se llama a [**IDXGISwapChain::P reenviar**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) en un recurso que actualmente no está en este estado, se emite una advertencia de nivel de depuración.</span><span class="sxs-lookup"><span data-stu-id="7051b-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="7051b-174">Descartar recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-174">Discarding resources</span></span>

<span data-ttu-id="7051b-175">Todos los Subrecursos de un recurso deben estar en el \_ Estado de destino de representación, o \_ Estado de escritura de profundidad, para los destinos de representación y los recursos de la galería de símbolos de profundidad, cuando se llama a [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) .</span><span class="sxs-lookup"><span data-stu-id="7051b-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="7051b-176">Transiciones de estado IMPLÍCITAS</span><span class="sxs-lookup"><span data-stu-id="7051b-176">Implicit State Transitions</span></span>

<span data-ttu-id="7051b-177">Los recursos solo se pueden "promover" fuera del estado de los recursos de D3D12 \_ \_ \_ común.</span><span class="sxs-lookup"><span data-stu-id="7051b-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="7051b-178">Del mismo modo, los recursos solo determinarán el estado de los recursos de D3D12 \_ \_ \_ común.</span><span class="sxs-lookup"><span data-stu-id="7051b-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="7051b-179">Promoción de Estado común</span><span class="sxs-lookup"><span data-stu-id="7051b-179">Common state promotion</span></span>

<span data-ttu-id="7051b-180">Todos los recursos de búfer y las texturas con la \_ marca de recurso D3D12 \_ \_ permiten que el \_ \_ conjunto de marcadores de acceso simultáneos se promuevan implícitamente del \_ Estado de los recursos de D3D12 \_ \_ común al estado relevante en el primer acceso de la GPU, incluida la \_ lectura genérica para cubrir cualquier escenario de lectura.</span><span class="sxs-lookup"><span data-stu-id="7051b-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="7051b-181">Se puede tener acceso a cualquier recurso del Estado común tal y como se encontraba en un solo Estado con</span><span class="sxs-lookup"><span data-stu-id="7051b-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="7051b-182">1 marca de escritura, o</span><span class="sxs-lookup"><span data-stu-id="7051b-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="7051b-183">1 o más marcas de lectura</span><span class="sxs-lookup"><span data-stu-id="7051b-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="7051b-184">Los recursos se pueden promocionar desde el Estado común en función de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="7051b-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="7051b-185">Marca de estado</span><span class="sxs-lookup"><span data-stu-id="7051b-185">State flag</span></span>                    | <span data-ttu-id="7051b-186">Estado promocionable</span><span class="sxs-lookup"><span data-stu-id="7051b-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="7051b-187">**Búferes y texturas de Simultaneous-Access**</span><span class="sxs-lookup"><span data-stu-id="7051b-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="7051b-188">**Texturas de acceso no simultáneo**</span><span class="sxs-lookup"><span data-stu-id="7051b-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="7051b-189">\_búfer de vértices y \_ constantes \_</span><span class="sxs-lookup"><span data-stu-id="7051b-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="7051b-190">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-190">Yes</span></span>                                          | <span data-ttu-id="7051b-191">No</span><span class="sxs-lookup"><span data-stu-id="7051b-191">No</span></span>                                   |
| <span data-ttu-id="7051b-192">búfer de índice \_</span><span class="sxs-lookup"><span data-stu-id="7051b-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="7051b-193">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-193">Yes</span></span>                                          | <span data-ttu-id="7051b-194">No</span><span class="sxs-lookup"><span data-stu-id="7051b-194">No</span></span>                                   |
| <span data-ttu-id="7051b-195">destino de representación \_</span><span class="sxs-lookup"><span data-stu-id="7051b-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="7051b-196">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-196">Yes</span></span>                                          | <span data-ttu-id="7051b-197">No</span><span class="sxs-lookup"><span data-stu-id="7051b-197">No</span></span>                                   |
| <span data-ttu-id="7051b-198">acceso desordenado \_</span><span class="sxs-lookup"><span data-stu-id="7051b-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="7051b-199">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-199">Yes</span></span>                                          | <span data-ttu-id="7051b-200">No</span><span class="sxs-lookup"><span data-stu-id="7051b-200">No</span></span>                                   |
| <span data-ttu-id="7051b-201">escritura de profundidad \_</span><span class="sxs-lookup"><span data-stu-id="7051b-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="7051b-202">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7051b-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="7051b-203">No</span><span class="sxs-lookup"><span data-stu-id="7051b-203">No</span></span>                                   |
| <span data-ttu-id="7051b-204">lectura de profundidad \_</span><span class="sxs-lookup"><span data-stu-id="7051b-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="7051b-205">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7051b-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="7051b-206">No</span><span class="sxs-lookup"><span data-stu-id="7051b-206">No</span></span>                                   |
| <span data-ttu-id="7051b-207">\_recurso de \_ sombreador sin píxeles \_</span><span class="sxs-lookup"><span data-stu-id="7051b-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="7051b-208">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-208">Yes</span></span>                                          | <span data-ttu-id="7051b-209">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-209">Yes</span></span>                                  |
| <span data-ttu-id="7051b-210">\_recurso de sombreador de píxeles \_</span><span class="sxs-lookup"><span data-stu-id="7051b-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="7051b-211">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-211">Yes</span></span>                                          | <span data-ttu-id="7051b-212">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-212">Yes</span></span>                                  |
| <span data-ttu-id="7051b-213">transmisión \_ por secuencias</span><span class="sxs-lookup"><span data-stu-id="7051b-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="7051b-214">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-214">Yes</span></span>                                          | <span data-ttu-id="7051b-215">No</span><span class="sxs-lookup"><span data-stu-id="7051b-215">No</span></span>                                   |
| <span data-ttu-id="7051b-216">argumento indirecto \_</span><span class="sxs-lookup"><span data-stu-id="7051b-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="7051b-217">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-217">Yes</span></span>                                          | <span data-ttu-id="7051b-218">No</span><span class="sxs-lookup"><span data-stu-id="7051b-218">No</span></span>                                   |
| <span data-ttu-id="7051b-219">COPIAR \_ dest</span><span class="sxs-lookup"><span data-stu-id="7051b-219">COPY\_DEST</span></span>                    | <span data-ttu-id="7051b-220">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-220">Yes</span></span>                                          | <span data-ttu-id="7051b-221">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-221">Yes</span></span>                                  |
| <span data-ttu-id="7051b-222">COPIAR \_ origen</span><span class="sxs-lookup"><span data-stu-id="7051b-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="7051b-223">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-223">Yes</span></span>                                          | <span data-ttu-id="7051b-224">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-224">Yes</span></span>                                  |
| <span data-ttu-id="7051b-225">RESOLVER \_ dest</span><span class="sxs-lookup"><span data-stu-id="7051b-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="7051b-226">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-226">Yes</span></span>                                          | <span data-ttu-id="7051b-227">No</span><span class="sxs-lookup"><span data-stu-id="7051b-227">No</span></span>                                   |
| <span data-ttu-id="7051b-228">RESOLVER \_ origen</span><span class="sxs-lookup"><span data-stu-id="7051b-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="7051b-229">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-229">Yes</span></span>                                          | <span data-ttu-id="7051b-230">No</span><span class="sxs-lookup"><span data-stu-id="7051b-230">No</span></span>                                   |
| <span data-ttu-id="7051b-231">PREDICATION</span><span class="sxs-lookup"><span data-stu-id="7051b-231">PREDICATION</span></span>                   | <span data-ttu-id="7051b-232">Sí</span><span class="sxs-lookup"><span data-stu-id="7051b-232">Yes</span></span>                                          | <span data-ttu-id="7051b-233">No</span><span class="sxs-lookup"><span data-stu-id="7051b-233">No</span></span>                                   |



 

<span data-ttu-id="7051b-234"><sup>\*</sup>Los recursos de la galería de símbolos de profundidad deben ser texturas de acceso no simultáneo y, por tanto, nunca se pueden promocionar implícitamente.</span><span class="sxs-lookup"><span data-stu-id="7051b-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="7051b-235">Cuando se produce este acceso, la promoción actúa como una barrera de recursos implícita.</span><span class="sxs-lookup"><span data-stu-id="7051b-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="7051b-236">En el caso de los accesos posteriores, se requerirán barreras de recursos para cambiar el estado del recurso si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7051b-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="7051b-237">Tenga en cuenta que la promoción de un estado de lectura promocionado a varios Estados de lectura es válida, pero no es el caso de los Estados de escritura.</span><span class="sxs-lookup"><span data-stu-id="7051b-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="7051b-238">Por ejemplo, si un recurso del Estado común se promueve al recurso de \_ sombreador \_ de píxeles en una llamada a Draw, todavía se puede promover a NON_PIXEL \_ recurso de sombreador \_ | \_ \_ Recurso de sombreador de píxeles en otra llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="7051b-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="7051b-239">Sin embargo, si se usa en una operación de escritura, como un destino de copia, una barrera de transición de estado de recursos de los Estados de lectura promovidos combinados, aquí NON_PIXEL \_ recurso de sombreador \_ | \_Recurso de sombreador de píxeles \_ , \_ se necesita copiar el destino.</span><span class="sxs-lookup"><span data-stu-id="7051b-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="7051b-240">Del mismo modo, si se promovió de común a COPY \_ dest, todavía se requiere una barrera para realizar la transición de la copia de \_ destino al destino de representación \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="7051b-241">Tenga en cuenta que la promoción de Estado común es "gratis", ya que no es necesario que la GPU realice ninguna espera de sincronización.</span><span class="sxs-lookup"><span data-stu-id="7051b-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="7051b-242">La promoción representa el hecho de que los recursos del Estado común no deben requerir ningún trabajo de GPU adicional ni seguimiento de controladores para admitir determinados accesos.</span><span class="sxs-lookup"><span data-stu-id="7051b-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="7051b-243">Caída del estado a común</span><span class="sxs-lookup"><span data-stu-id="7051b-243">State decay to common</span></span>

<span data-ttu-id="7051b-244">El volteo de la promoción de Estado común es la decadencia en el estado del recurso de D3D12 \_ \_ \_ común.</span><span class="sxs-lookup"><span data-stu-id="7051b-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="7051b-245">Los recursos que cumplen determinados requisitos se consideran sin estado y, de hecho, vuelven al Estado común cuando la GPU finaliza la ejecución de una operación de [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) .</span><span class="sxs-lookup"><span data-stu-id="7051b-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="7051b-246">No se produce la caída entre las listas de comandos que se ejecutan juntas en la misma llamada **ExecuteCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="7051b-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="7051b-247">Los siguientes recursos determinarán cuando se complete una operación [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la GPU:</span><span class="sxs-lookup"><span data-stu-id="7051b-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="7051b-248">Recursos a los que se tiene acceso en una cola de copia, *o*</span><span class="sxs-lookup"><span data-stu-id="7051b-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="7051b-249">Recursos de búfer en cualquier tipo de cola, *o*</span><span class="sxs-lookup"><span data-stu-id="7051b-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="7051b-250">Los recursos de textura en cualquier tipo de cola que tienen la \_ marca de recurso D3D12 permiten el marcador de \_ \_ \_ \_ acceso simultáneo establecido, *o bien*</span><span class="sxs-lookup"><span data-stu-id="7051b-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="7051b-251">Cualquier recurso promovido implícitamente a un estado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7051b-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="7051b-252">Al igual que la promoción de Estado común, la caída es gratuita porque no se necesita ninguna sincronización adicional.</span><span class="sxs-lookup"><span data-stu-id="7051b-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="7051b-253">La combinación de la promoción de Estado común y la caída puede ayudar a eliminar muchas transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) innecesarias.</span><span class="sxs-lookup"><span data-stu-id="7051b-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="7051b-254">En algunos casos, esto puede proporcionar mejoras significativas en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7051b-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="7051b-255">Los búferes y los recursos de Simultaneous-Access se determinarán en el Estado común, independientemente de si se han transferido explícitamente mediante barreras de recursos o se han promocionado implícitamente.</span><span class="sxs-lookup"><span data-stu-id="7051b-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="7051b-256">Implicaciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="7051b-256">Performance implications</span></span>

<span data-ttu-id="7051b-257">Al grabar transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas en los recursos en el Estado común, es correcto usar el \_ Estado de recurso D3D12 \_ \_ común o cualquier estado promocionable como valor *BeforeState* en la estructura de la barrera de transición de recursos de D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7051b-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="7051b-258">Esto permite la administración de estado tradicional que omite la caída automática de los búferes y las texturas de acceso simultáneo.</span><span class="sxs-lookup"><span data-stu-id="7051b-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="7051b-259">Sin embargo, esto puede no ser conveniente, ya que evitar las llamadas de transición **ResourceBarrier** con los recursos que se sabe que están en el Estado común puede mejorar significativamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7051b-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="7051b-260">Las barreras de recursos pueden ser costosas.</span><span class="sxs-lookup"><span data-stu-id="7051b-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="7051b-261">Están diseñados para forzar vaciados de caché, cambios de diseño de memoria y otra sincronización que puede que no sean necesarios para los recursos que ya están en el Estado común.</span><span class="sxs-lookup"><span data-stu-id="7051b-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="7051b-262">Una lista de comandos que usa una barrera de recursos de un estado no común a otro Estado no común en un recurso que se encuentra actualmente en estado común puede introducir una sobrecarga innecesaria.</span><span class="sxs-lookup"><span data-stu-id="7051b-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="7051b-263">Además, evite las transiciones de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas al \_ Estado de los recursos de D3D12 \_ \_ común a menos que sea absolutamente necesario (por ejemplo, el siguiente acceso se encuentra en una cola de comandos de copia que requiere que los recursos comiencen en el Estado común).</span><span class="sxs-lookup"><span data-stu-id="7051b-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="7051b-264">Las transiciones excesivas al Estado común pueden reducir drásticamente el rendimiento de la GPU.</span><span class="sxs-lookup"><span data-stu-id="7051b-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="7051b-265">En Resumen, intente basarse en la promoción de Estado común y en la decadencia siempre que su semántica le permita salir sin emitir llamadas a [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="7051b-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="7051b-266">Barreras divididas</span><span class="sxs-lookup"><span data-stu-id="7051b-266">Split Barriers</span></span>

<span data-ttu-id="7051b-267">Una barrera de transición de recursos con la marca de la barrera de recurso de D3D12 \_ \_ \_ \_ \_ solo comienza una barrera de división y se dice que la barrera de transición está pendiente.</span><span class="sxs-lookup"><span data-stu-id="7051b-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="7051b-268">Mientras la barrera está pendiente, la GPU no puede leer ni escribir el recurso (sub).</span><span class="sxs-lookup"><span data-stu-id="7051b-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="7051b-269">La única barrera de transición válida que se puede aplicar a un recurso (sub) con una barrera pendiente es la misma con los mismos Estados *antes* y *después* y la marca de fin de la marca de barrera de los recursos de D3D12 \_ , la \_ \_ \_ \_ barrera que completa la transición pendiente.</span><span class="sxs-lookup"><span data-stu-id="7051b-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="7051b-270">Las barreras divididas proporcionan sugerencias a la GPU de que un recurso en *el estado a* se usará a continuación en el estado *B* posteriormente.</span><span class="sxs-lookup"><span data-stu-id="7051b-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="7051b-271">Esto proporciona a la GPU la opción de optimizar la carga de trabajo de transición, lo que podría reducir o eliminar las paradas de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7051b-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="7051b-272">La emisión de la barrera solo final garantiza que todo el trabajo de transición de la GPU finalice antes de pasar al siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7051b-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="7051b-273">El uso de barreras divididas puede ayudar a mejorar el rendimiento, especialmente en escenarios con varios motores o en los que los recursos se transfieran de forma dispersa en una o varias listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="7051b-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="7051b-274">Escenario de ejemplo de barrera de recursos</span><span class="sxs-lookup"><span data-stu-id="7051b-274">Resource barrier example scenario</span></span>

<span data-ttu-id="7051b-275">En los fragmentos de código siguientes se muestra el uso del método [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) en un ejemplo de subprocesamiento múltiple.</span><span class="sxs-lookup"><span data-stu-id="7051b-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="7051b-276">Crear la vista de galería de símbolos de profundidad, en la que se realiza la transición a un estado grabable.</span><span class="sxs-lookup"><span data-stu-id="7051b-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="7051b-277">Crear la vista de búfer de vértices y cambiarla primero de un Estado común a un destino y, a continuación, de un destino a un estado legible genérico.</span><span class="sxs-lookup"><span data-stu-id="7051b-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="7051b-278">Crear la vista del búfer de índice, cambiando primero de un Estado común a un destino y, a continuación, de un destino a un estado legible genérico.</span><span class="sxs-lookup"><span data-stu-id="7051b-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="7051b-279">Creación de texturas y vistas de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7051b-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="7051b-280">La textura se cambia de un Estado común a un destino y, a continuación, de un destino a un recurso de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="7051b-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="7051b-281">Inicio de un fotograma; Esto no solo usa [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para indicar que el búfer de reserva se va a usar como destino de representación, sino que también inicializa el recurso de marco (que llama a **ResourceBarrier** en el búfer de estarcido de profundidad).</span><span class="sxs-lookup"><span data-stu-id="7051b-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="7051b-282">Finalización de un fotograma, que indica que el búfer de reserva ahora se usa para presentar.</span><span class="sxs-lookup"><span data-stu-id="7051b-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="7051b-283">Al inicializar un recurso de marco, llamado al iniciar un fotograma, se pasa el búfer de estarcido de profundidad a grabable.</span><span class="sxs-lookup"><span data-stu-id="7051b-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="7051b-284">Las barreras se intercambian de trama intermedia y se realiza la transición de la asignación de instantáneas de escritura a legible.</span><span class="sxs-lookup"><span data-stu-id="7051b-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="7051b-285">Se llama a Finish cuando finaliza un fotograma, pasando el mapa de instantáneas a un Estado común.</span><span class="sxs-lookup"><span data-stu-id="7051b-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="7051b-286">Ejemplo de promoción de Estado común y decadencia</span><span class="sxs-lookup"><span data-stu-id="7051b-286">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="7051b-287">Ejemplo de barreras divididas</span><span class="sxs-lookup"><span data-stu-id="7051b-287">Example of split barriers</span></span>

<span data-ttu-id="7051b-288">En el ejemplo siguiente se muestra cómo usar una barrera dividida para reducir las paradas de canalización.</span><span class="sxs-lookup"><span data-stu-id="7051b-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="7051b-289">El código que sigue no utiliza barreras divididas:</span><span class="sxs-lookup"><span data-stu-id="7051b-289">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="7051b-290">En el código siguiente se usan barreras divididas:</span><span class="sxs-lookup"><span data-stu-id="7051b-290">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="7051b-291">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7051b-291">Related topics</span></span>

[<span data-ttu-id="7051b-292">Tutoriales de vídeo de aprendizaje avanzado de DirectX: barreras de recursos y seguimiento de estado</span><span class="sxs-lookup"><span data-stu-id="7051b-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="7051b-293">Sincronización de varios motores</span><span class="sxs-lookup"><span data-stu-id="7051b-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="7051b-294">Envío de trabajo en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7051b-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="7051b-295">Una mirada dentro de las barreras de estado de los recursos de D3D12</span><span class="sxs-lookup"><span data-stu-id="7051b-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

