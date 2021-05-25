---
title: Uso de barreras de recursos para sincronizar los estados de los recursos en Direct3D 12
description: Para reducir el uso general de LA CPU y habilitar el procesamiento previo y multiproceso de controladores, Direct3D 12 traslada la responsabilidad de la administración del estado por recurso del controlador de gráficos a la aplicación.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343480"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="89862-103">Uso de barreras de recursos para sincronizar los estados de los recursos en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="89862-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="89862-104">Para reducir el uso general de LA CPU y habilitar el procesamiento previo y multiproceso de controladores, Direct3D 12 traslada la responsabilidad de la administración del estado por recurso del controlador de gráficos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89862-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="89862-105">Un ejemplo de estado por recurso es si actualmente se tiene acceso a un recurso de textura como a través de un objeto Shader Vista de recursos o como una vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="89862-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="89862-106">En Direct3D 11, los controladores eran necesarios para realizar un seguimiento de este estado en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="89862-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="89862-107">Esto es costoso desde la perspectiva de la CPU y complica significativamente cualquier tipo de diseño multiproceso.</span><span class="sxs-lookup"><span data-stu-id="89862-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="89862-108">En Microsoft Direct3D 12, la mayoría del estado por recurso se administra mediante la aplicación con una sola API, [**ID3D12GraphicsCommandList::ResourceBartero**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="89862-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="89862-109">Uso de ResourceBar php API para administrar el estado por recurso</span><span class="sxs-lookup"><span data-stu-id="89862-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="89862-110">Estados de recursos</span><span class="sxs-lookup"><span data-stu-id="89862-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="89862-111">Estados iniciales de los recursos</span><span class="sxs-lookup"><span data-stu-id="89862-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="89862-112">Restricciones de estado de recursos de lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="89862-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="89862-113">Estados de recursos para presentar búferes de reserva</span><span class="sxs-lookup"><span data-stu-id="89862-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="89862-114">Descarte de recursos</span><span class="sxs-lookup"><span data-stu-id="89862-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="89862-115">Transiciones de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="89862-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="89862-116">Promoción de estado común</span><span class="sxs-lookup"><span data-stu-id="89862-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="89862-117">Decadencia del estado a común</span><span class="sxs-lookup"><span data-stu-id="89862-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="89862-118">Implicaciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="89862-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="89862-119">Barreras divididas</span><span class="sxs-lookup"><span data-stu-id="89862-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="89862-120">Escenario de ejemplo de barrera de recursos</span><span class="sxs-lookup"><span data-stu-id="89862-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="89862-121">Ejemplo común de promoción de estado y decadencia</span><span class="sxs-lookup"><span data-stu-id="89862-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="89862-122">Ejemplo de barreras divididas</span><span class="sxs-lookup"><span data-stu-id="89862-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="89862-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89862-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="89862-124">Uso de ResourceBar php API para administrar el estado por recurso</span><span class="sxs-lookup"><span data-stu-id="89862-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="89862-125">[**ResourceBar odbc notifica**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) al controlador de gráficos las situaciones en las que el controlador puede necesitar sincronizar varios accesos a la memoria en la que se almacena un recurso.</span><span class="sxs-lookup"><span data-stu-id="89862-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="89862-126">Se llama al método con una o varias estructuras de descripción de barrera de recursos que indican el tipo de barrera de recursos que se declara.</span><span class="sxs-lookup"><span data-stu-id="89862-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="89862-127">Hay tres tipos de barreras de recursos:</span><span class="sxs-lookup"><span data-stu-id="89862-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="89862-128">**Barrera de transición:** una barrera de transición indica que un conjunto de subrecursos pasa entre distintos usos.</span><span class="sxs-lookup"><span data-stu-id="89862-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="89862-129">Se [**usa una estructura D3D12 \_ RESOURCE TRANSITION \_ \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) para especificar el subrecurso que está en transición, así como los estados *antes* y después del subrecurso. </span><span class="sxs-lookup"><span data-stu-id="89862-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="89862-130">El sistema comprueba que las transiciones de subrecursos de una lista de comandos son coherentes con las transiciones anteriores de la misma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="89862-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="89862-131">La capa de depuración realiza un seguimiento adicional del estado del subrecurso para encontrar otros errores, pero esta validación es conservadora y no exhaustiva.</span><span class="sxs-lookup"><span data-stu-id="89862-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="89862-132">Tenga en cuenta que puede usar la marca D3D12 RESOURCE BARRIER ALL SUBRESOURCES para especificar que todos los subrecursos de un recurso se están \_ \_ \_ \_ transimendo.</span><span class="sxs-lookup"><span data-stu-id="89862-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="89862-133">**Barrera de alias:** una barrera de alias indica una transición entre los usos de dos recursos diferentes que tienen asignaciones superpuestas en el mismo montón.</span><span class="sxs-lookup"><span data-stu-id="89862-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="89862-134">Esto se aplica a los recursos reservados y colocados.</span><span class="sxs-lookup"><span data-stu-id="89862-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="89862-135">Se [**usa una estructura D3D12 RESOURCE \_ \_ ALIASING \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) para especificar tanto el recurso *anterior* como *el recurso* after.</span><span class="sxs-lookup"><span data-stu-id="89862-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="89862-136">Tenga en cuenta que uno o ambos recursos pueden ser NULL, lo que indica que cualquier recurso en mosaico podría provocar alias.</span><span class="sxs-lookup"><span data-stu-id="89862-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="89862-137">Para obtener más información sobre el uso de recursos en mosaico, vea [Recursos en mosaico y](../direct3d11/tiled-resources.md) Recursos en mosaico por [volumen.](volume-tiled-resources.md)</span><span class="sxs-lookup"><span data-stu-id="89862-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="89862-138">Barrera de la vista de acceso desordenado **(UAV):** una barrera UAV indica que todos los accesos UAV, tanto de lectura como de escritura, a un recurso determinado deben completarse entre cualquier acceso UAV futuro, tanto de lectura como de escritura.</span><span class="sxs-lookup"><span data-stu-id="89862-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="89862-139">No es necesario que una aplicación coloque una barrera UAV entre dos llamadas a draw o dispatch que solo se leen desde un UAV.</span><span class="sxs-lookup"><span data-stu-id="89862-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="89862-140">Además, no es necesario colocar una barrera UAV entre dos llamadas a draw o dispatch que escriben en el mismo UAV si la aplicación sabe que es seguro ejecutar el acceso UAV en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="89862-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="89862-141">Se [**usa una estructura D3D12 RESOURCE \_ \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) para especificar el recurso UAV al que se aplica la barrera.</span><span class="sxs-lookup"><span data-stu-id="89862-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="89862-142">La aplicación puede especificar NULL para el UAV de la barrera, lo que indica que cualquier acceso UAV podría requerir la barrera.</span><span class="sxs-lookup"><span data-stu-id="89862-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="89862-143">Cuando se llama a [**ResourceBartero**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) con una matriz de descripciones de barrera de recursos, la API se comporta como si se llamara una vez para cada elemento, en el orden en que se proporcionaron.</span><span class="sxs-lookup"><span data-stu-id="89862-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="89862-144">En un momento dado, un subrecurso está exactamente en un estado, determinado por el conjunto de marcas [**\_ RESOURCE \_ STATES de D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) proporcionadas a [**ResourceBarander**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="89862-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="89862-145">La aplicación debe asegurarse de que los *estados antes* y *después* de las llamadas consecutivas a **ResourceBarlda están de acuerdo.**</span><span class="sxs-lookup"><span data-stu-id="89862-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="89862-146">Las aplicaciones deben procesar por lotes varias transiciones en una llamada API siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="89862-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="89862-147">Estados de recursos</span><span class="sxs-lookup"><span data-stu-id="89862-147">Resource states</span></span>

<span data-ttu-id="89862-148">Para obtener la lista completa de estados de recursos entre los que un recurso puede realizar la transición, consulte el tema de referencia de la [**enumeración \_ RESOURCE STATES \_ de D3D12.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="89862-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="89862-149">Para las barreras de recursos divididos, consulte también [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="89862-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="89862-150">Estados iniciales de los recursos</span><span class="sxs-lookup"><span data-stu-id="89862-150">Initial states for resources</span></span>

<span data-ttu-id="89862-151">Los recursos se pueden crear con cualquier estado inicial especificado por el usuario (válido para la descripción del recurso), con las siguientes excepciones:</span><span class="sxs-lookup"><span data-stu-id="89862-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="89862-152">Los montones de carga deben comenzar en el estado D3D12 RESOURCE STATE GENERIC READ, que es \_ una combinación or bit a bit \_ \_ \_ de:</span><span class="sxs-lookup"><span data-stu-id="89862-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="89862-153">VÉRTICE DE ESTADO DE RECURSO D3D12 \_ \_ Y BÚFER \_ \_ \_ \_ CONSTANTE</span><span class="sxs-lookup"><span data-stu-id="89862-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="89862-154">BÚFER DE ÍNDICE DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="89862-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="89862-155">ORIGEN DE COPIA DEL ESTADO DEL RECURSO D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="89862-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="89862-156">RECURSO DE SOMBREADOR \_ DE PÍXELES DE ESTADO \_ DE RECURSO \_ \_ \_ \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="89862-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="89862-157">RECURSO SOMBREADOR DE \_ PÍXELES DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="89862-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="89862-158">ARGUMENTO INDIRECTO DE ESTADO DE RECURSO D3D12 \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="89862-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="89862-159">Los montones de readback deben iniciarse en el estado D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="89862-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="89862-160">Los búferes de reserva de cadena de intercambio se inician automáticamente en el estado RESOURCE STATE COMMON de D3D12. \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="89862-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="89862-161">Para que un montón pueda ser el destino de una operación de copia de GPU, normalmente el montón debe pasar primero al estado D3D12 \_ RESOURCE \_ STATE COPY \_ \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="89862-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="89862-162">Sin embargo, los recursos creados en los montones DE CARGA deben iniciarse en y no pueden cambiar desde el estado DE LECTURA GENÉRICA, ya que solo la CPU realizará \_ la escritura.</span><span class="sxs-lookup"><span data-stu-id="89862-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="89862-163">Por el contrario, los recursos confirmados creados en montones READBACK deben iniciarse en y no pueden cambiar desde el estado COPY \_ DEST.</span><span class="sxs-lookup"><span data-stu-id="89862-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="89862-164">Restricciones de estado de recursos de lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="89862-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="89862-165">Los bits de uso del estado de recurso que se usan para describir un estado de recurso se dividen en estados de solo lectura y de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="89862-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="89862-166">El tema de referencia para [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica el nivel de acceso de lectura y escritura para cada bit de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="89862-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="89862-167">Como máximo, solo se puede establecer un bit de lectura/escritura para cualquier recurso.</span><span class="sxs-lookup"><span data-stu-id="89862-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="89862-168">Si se establece un bit de escritura, no se puede establecer ningún bit de solo lectura para ese recurso.</span><span class="sxs-lookup"><span data-stu-id="89862-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="89862-169">Si no se establece ningún bit de escritura, se puede establecer cualquier número de bits de lectura.</span><span class="sxs-lookup"><span data-stu-id="89862-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="89862-170">Estados de recursos para presentar búferes de reserva</span><span class="sxs-lookup"><span data-stu-id="89862-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="89862-171">Antes de que se presente un búfer de reserva, debe estar en el estado D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="89862-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="89862-172">Tenga en cuenta que el estado del recurso D3D12 RESOURCE STATE PRESENT es un sinónimo de \_ \_ \_ D3D12 RESOURCE STATE COMMON y ambos tienen un \_ \_ valor de \_ 0.</span><span class="sxs-lookup"><span data-stu-id="89862-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="89862-173">Si se llama a [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (o [**IDXGISwapChain1::P resent1)**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)en un recurso que no está actualmente en este estado, se emite una advertencia de capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="89862-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="89862-174">Descartar recursos</span><span class="sxs-lookup"><span data-stu-id="89862-174">Discarding resources</span></span>

<span data-ttu-id="89862-175">Todos los subrecursos de un recurso deben estar en el estado RENDER TARGET o DEPTH WRITE para los destinos de representación y los recursos de galería de símbolos de profundidad, respectivamente, cuando se llama a \_ \_ [**ID3D12GraphicsCommandList::D iscardResource.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)</span><span class="sxs-lookup"><span data-stu-id="89862-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="89862-176">Transiciones de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="89862-176">Implicit State Transitions</span></span>

<span data-ttu-id="89862-177">Los recursos solo se pueden "promover" fuera de D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="89862-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="89862-178">Del mismo modo, los recursos solo se "degradarán" a D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="89862-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="89862-179">Promoción de estado común</span><span class="sxs-lookup"><span data-stu-id="89862-179">Common state promotion</span></span>

<span data-ttu-id="89862-180">Todos los recursos de búfer, así como las texturas con el conjunto de marcas D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS, se promueven implícitamente de \_ \_ \_ \_ \_ D3D12 \_ RESOURCE STATE \_ \_ COMMON \_ al estado pertinente en el primer acceso de GPU, incluida LA LECTURA GENÉRICA para cubrir cualquier escenario de lectura.</span><span class="sxs-lookup"><span data-stu-id="89862-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="89862-181">Se puede acceder a cualquier recurso en el estado COMMON como a través de él en un solo estado con</span><span class="sxs-lookup"><span data-stu-id="89862-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="89862-182">1 marca WRITE o</span><span class="sxs-lookup"><span data-stu-id="89862-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="89862-183">1 o más marcas DE LECTURA</span><span class="sxs-lookup"><span data-stu-id="89862-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="89862-184">Los recursos se pueden promover desde el estado COMMON en función de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="89862-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="89862-185">Marca de estado</span><span class="sxs-lookup"><span data-stu-id="89862-185">State flag</span></span>                    | <span data-ttu-id="89862-186">Búferes y Simultaneous-Access texturas</span><span class="sxs-lookup"><span data-stu-id="89862-186">Buffers and Simultaneous-Access Textures</span></span>                             | <span data-ttu-id="89862-187">Texturas de acceso no simultáneo</span><span class="sxs-lookup"><span data-stu-id="89862-187">Non-Simultaneous-Access Textures</span></span>                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| <span data-ttu-id="89862-188">VÉRTICE \_ Y \_ BÚFER \_ CONSTANTE</span><span class="sxs-lookup"><span data-stu-id="89862-188">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="89862-189">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-189">Yes</span></span>                                          | <span data-ttu-id="89862-190">No</span><span class="sxs-lookup"><span data-stu-id="89862-190">No</span></span>                                   |
| <span data-ttu-id="89862-191">BÚFER DE \_ ÍNDICE</span><span class="sxs-lookup"><span data-stu-id="89862-191">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="89862-192">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-192">Yes</span></span>                                          | <span data-ttu-id="89862-193">No</span><span class="sxs-lookup"><span data-stu-id="89862-193">No</span></span>                                   |
| <span data-ttu-id="89862-194">DESTINO DE \_ REPRESENTACIÓN</span><span class="sxs-lookup"><span data-stu-id="89862-194">RENDER\_TARGET</span></span>                | <span data-ttu-id="89862-195">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-195">Yes</span></span>                                          | <span data-ttu-id="89862-196">No</span><span class="sxs-lookup"><span data-stu-id="89862-196">No</span></span>                                   |
| <span data-ttu-id="89862-197">ACCESO \_ DESORDENADO</span><span class="sxs-lookup"><span data-stu-id="89862-197">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="89862-198">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-198">Yes</span></span>                                          | <span data-ttu-id="89862-199">No</span><span class="sxs-lookup"><span data-stu-id="89862-199">No</span></span>                                   |
| <span data-ttu-id="89862-200">ESCRITURA EN \_ PROFUNDIDAD</span><span class="sxs-lookup"><span data-stu-id="89862-200">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="89862-201">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="89862-201">No<sup>\*</sup></span></span>                              | <span data-ttu-id="89862-202">No</span><span class="sxs-lookup"><span data-stu-id="89862-202">No</span></span>                                   |
| <span data-ttu-id="89862-203">LECTURA DE \_ PROFUNDIDAD</span><span class="sxs-lookup"><span data-stu-id="89862-203">DEPTH\_READ</span></span>                   | <span data-ttu-id="89862-204">No<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="89862-204">No<sup>\*</sup></span></span>                              | <span data-ttu-id="89862-205">No</span><span class="sxs-lookup"><span data-stu-id="89862-205">No</span></span>                                   |
| <span data-ttu-id="89862-206">RECURSO DE \_ \_ SOMBREADOR SIN \_ PÍXELES</span><span class="sxs-lookup"><span data-stu-id="89862-206">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="89862-207">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-207">Yes</span></span>                                          | <span data-ttu-id="89862-208">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-208">Yes</span></span>                                  |
| <span data-ttu-id="89862-209">RECURSO \_ SOMBREADOR DE \_ PÍXELES</span><span class="sxs-lookup"><span data-stu-id="89862-209">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="89862-210">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-210">Yes</span></span>                                          | <span data-ttu-id="89862-211">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-211">Yes</span></span>                                  |
| <span data-ttu-id="89862-212">STREAM \_ OUT</span><span class="sxs-lookup"><span data-stu-id="89862-212">STREAM\_OUT</span></span>                   | <span data-ttu-id="89862-213">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-213">Yes</span></span>                                          | <span data-ttu-id="89862-214">No</span><span class="sxs-lookup"><span data-stu-id="89862-214">No</span></span>                                   |
| <span data-ttu-id="89862-215">ARGUMENTO \_ INDIRECTO</span><span class="sxs-lookup"><span data-stu-id="89862-215">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="89862-216">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-216">Yes</span></span>                                          | <span data-ttu-id="89862-217">No</span><span class="sxs-lookup"><span data-stu-id="89862-217">No</span></span>                                   |
| <span data-ttu-id="89862-218">COPY \_ DEST</span><span class="sxs-lookup"><span data-stu-id="89862-218">COPY\_DEST</span></span>                    | <span data-ttu-id="89862-219">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-219">Yes</span></span>                                          | <span data-ttu-id="89862-220">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-220">Yes</span></span>                                  |
| <span data-ttu-id="89862-221">COPY \_ SOURCE</span><span class="sxs-lookup"><span data-stu-id="89862-221">COPY\_SOURCE</span></span>                  | <span data-ttu-id="89862-222">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-222">Yes</span></span>                                          | <span data-ttu-id="89862-223">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-223">Yes</span></span>                                  |
| <span data-ttu-id="89862-224">RESOLVE \_ DEST</span><span class="sxs-lookup"><span data-stu-id="89862-224">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="89862-225">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-225">Yes</span></span>                                          | <span data-ttu-id="89862-226">No</span><span class="sxs-lookup"><span data-stu-id="89862-226">No</span></span>                                   |
| <span data-ttu-id="89862-227">RESOLVER \_ ORIGEN</span><span class="sxs-lookup"><span data-stu-id="89862-227">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="89862-228">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-228">Yes</span></span>                                          | <span data-ttu-id="89862-229">No</span><span class="sxs-lookup"><span data-stu-id="89862-229">No</span></span>                                   |
| <span data-ttu-id="89862-230">Predicación</span><span class="sxs-lookup"><span data-stu-id="89862-230">PREDICATION</span></span>                   | <span data-ttu-id="89862-231">Sí</span><span class="sxs-lookup"><span data-stu-id="89862-231">Yes</span></span>                                          | <span data-ttu-id="89862-232">No</span><span class="sxs-lookup"><span data-stu-id="89862-232">No</span></span>                                   |



 

<span data-ttu-id="89862-233"><sup>\*</sup>Los recursos de galería de símbolos de profundidad deben ser texturas de acceso no simultáneo y, por tanto, nunca se pueden promover implícitamente.</span><span class="sxs-lookup"><span data-stu-id="89862-233"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="89862-234">Cuando se produce este acceso, la promoción actúa como una barrera implícita de recursos.</span><span class="sxs-lookup"><span data-stu-id="89862-234">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="89862-235">Para los accesos posteriores, se requieren barreras de recursos para cambiar el estado del recurso si es necesario.</span><span class="sxs-lookup"><span data-stu-id="89862-235">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="89862-236">Tenga en cuenta que la promoción de un estado de lectura promocionado a varios estados de lectura es válida, pero este no es el caso de los estados de escritura.</span><span class="sxs-lookup"><span data-stu-id="89862-236">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="89862-237">Por ejemplo, si un recurso en estado común se promueve a PIXEL SHADER RESOURCE en una llamada a Draw, todavía se puede promover a NON_PIXEL \_ \_ RECURSO SHADER \_ \_ | RECURSO \_ \_ SOMBREADOR DE PÍXELes en otra llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="89862-237">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="89862-238">Sin embargo, si se usa en una operación de escritura, como un destino de copia, una barrera de transición de estado de recurso de los estados de lectura promocionados combinados, NON_PIXEL \_ SHADER \_ RESOURCE | SE \_ NECESITA EL RECURSO \_ SOMBREADOR DE PÍXELES \_ PARA COPIAR DEST.</span><span class="sxs-lookup"><span data-stu-id="89862-238">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="89862-239">De forma similar, si se promueve de COMMON a COPY DEST, todavía se requiere una barrera para realizar la transición de \_ COPY \_ DEST a RENDER \_ TARGET.</span><span class="sxs-lookup"><span data-stu-id="89862-239">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="89862-240">Tenga en cuenta que la promoción de estado común es "gratuita", ya que no es necesario que la GPU realice ninguna espera de sincronización.</span><span class="sxs-lookup"><span data-stu-id="89862-240">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="89862-241">La promoción representa el hecho de que los recursos en el estado COMMON no deben requerir trabajo adicional de GPU ni seguimiento de controladores para admitir determinados accesos.</span><span class="sxs-lookup"><span data-stu-id="89862-241">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="89862-242">Decadencia del estado a común</span><span class="sxs-lookup"><span data-stu-id="89862-242">State decay to common</span></span>

<span data-ttu-id="89862-243">El otro lado de la promoción de estado común es volver a decadencia a D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="89862-243">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="89862-244">Los recursos que cumplen determinados requisitos se consideran sin estado y vuelven eficazmente al estado común cuando la GPU finaliza la ejecución de una [**operación ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)</span><span class="sxs-lookup"><span data-stu-id="89862-244">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="89862-245">La decadencia no se produce entre las listas de comandos ejecutadas juntas en la misma **llamada ExecuteCommandLists.**</span><span class="sxs-lookup"><span data-stu-id="89862-245">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="89862-246">Los siguientes recursos se degradarán cuando se complete una operación [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la GPU:</span><span class="sxs-lookup"><span data-stu-id="89862-246">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="89862-247">Recursos a los que se accede en una cola de copia *o*</span><span class="sxs-lookup"><span data-stu-id="89862-247">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="89862-248">Recursos de búfer en cualquier tipo de cola *o*</span><span class="sxs-lookup"><span data-stu-id="89862-248">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="89862-249">Recursos de textura en cualquier tipo de cola que tenga establecida la marca DE RECURSOS D3D12 \_ \_ ALLOW SIMULTANEOUS ACCESS \_ \_ \_ o </span><span class="sxs-lookup"><span data-stu-id="89862-249">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="89862-250">Cualquier recurso promovido implícitamente a un estado de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="89862-250">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="89862-251">Al igual que la promoción de estado común, la decadencia es libre en el sentido de que no se necesita ninguna sincronización adicional.</span><span class="sxs-lookup"><span data-stu-id="89862-251">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="89862-252">Combinar la promoción de estado común y la decadencia puede ayudar a eliminar muchas transiciones [**innecesarias de ResourceBarcomposición.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="89862-252">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="89862-253">En algunos casos, esto puede proporcionar mejoras de rendimiento significativas.</span><span class="sxs-lookup"><span data-stu-id="89862-253">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="89862-254">Los búferes y Simultaneous-Access recursos se degradarán al estado común, independientemente de si se han pasado explícitamente mediante barreras de recursos o se han promocionado implícitamente.</span><span class="sxs-lookup"><span data-stu-id="89862-254">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="89862-255">Implicaciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="89862-255">Performance implications</span></span>

<span data-ttu-id="89862-256">Al registrar transiciones [**de ResourceBargida**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas en recursos en el estado común, es correcto usar D3D12 RESOURCE STATE COMMON o cualquier estado promocionable como valor BeforeState en la estructura \_ \_ \_ D3D12  RESOURCE TRANSITION \_ \_ \_ BARRIER.</span><span class="sxs-lookup"><span data-stu-id="89862-256">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="89862-257">Esto permite la administración de estado tradicional que omite la decadencia automática de búferes y texturas de acceso simultáneo.</span><span class="sxs-lookup"><span data-stu-id="89862-257">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="89862-258">Sin embargo, puede que esto no sea deseable, ya que evitar la transición de llamadas **ResourceBartero** con recursos que se sabe que están en el estado común puede mejorar significativamente el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="89862-258">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="89862-259">Las barreras de recursos pueden ser costosas.</span><span class="sxs-lookup"><span data-stu-id="89862-259">Resource barriers can be expensive.</span></span> <span data-ttu-id="89862-260">Están diseñados para forzar vaciados de caché, cambios en el diseño de memoria y otra sincronización que pueden no ser necesarias para los recursos que ya están en el estado común.</span><span class="sxs-lookup"><span data-stu-id="89862-260">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="89862-261">Una lista de comandos que usa una barrera de recursos de un estado no común a otro estado no común en un recurso actualmente en el estado común puede introducir una gran sobrecarga innecesario.</span><span class="sxs-lookup"><span data-stu-id="89862-261">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="89862-262">Además, evite las transiciones explícitas de [**ResourceBarunda**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) a D3D12 RESOURCE STATE COMMON a menos que sea absolutamente necesario (por ejemplo, el siguiente acceso se encuentra en una cola de comandos COPY que requiere que los recursos comiencen en el estado \_ \_ \_ común).</span><span class="sxs-lookup"><span data-stu-id="89862-262">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="89862-263">Las transiciones excesivas al estado común pueden ralentizar drásticamente el rendimiento de GPU.</span><span class="sxs-lookup"><span data-stu-id="89862-263">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="89862-264">En resumen, intente confiar en la promoción de estado común y la degradación cada vez que su semántica le permita salir sin emitir [**llamadas a ResourceBarcomposición.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="89862-264">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="89862-265">Dividir barreras</span><span class="sxs-lookup"><span data-stu-id="89862-265">Split Barriers</span></span>

<span data-ttu-id="89862-266">Una barrera de transición de recursos con la marca D3D12 RESOURCE BARRIER FLAG BEGIN ONLY comienza una barrera de división y se dice que la barrera de transición \_ \_ está \_ \_ \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="89862-266">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="89862-267">Mientras la barrera está pendiente, la GPU no puede leer ni escribir el recurso (sub) .</span><span class="sxs-lookup"><span data-stu-id="89862-267">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="89862-268">La única barrera de transición legal que se puede aplicar a un  recurso  (sub)resource con una barrera pendiente es una con los mismos estados antes y después y la marca D3D12 RESOURCE BARRIER FLAG END ONLY, que completa la transición \_ \_ \_ \_ \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="89862-268">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="89862-269">Las barreras divididas proporcionan sugerencias a la GPU de que un recurso en el estado *A* se usará más adelante en el estado *B.*</span><span class="sxs-lookup"><span data-stu-id="89862-269">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="89862-270">Esto ofrece a la GPU la opción de optimizar la carga de trabajo de transición, lo que posiblemente reduce o elimina los puestos de ejecución.</span><span class="sxs-lookup"><span data-stu-id="89862-270">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="89862-271">La emisión de la barrera de solo fin garantiza que todo el trabajo de transición de GPU haya finalizado antes de pasar al siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="89862-271">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="89862-272">El uso de barreras divididas puede ayudar a mejorar el rendimiento, especialmente en escenarios de varios motores o en los que los recursos se han pasado de lectura y escritura de forma dispersa a lo largo de una o varias listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="89862-272">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="89862-273">Escenario de ejemplo de barrera de recursos</span><span class="sxs-lookup"><span data-stu-id="89862-273">Resource barrier example scenario</span></span>

<span data-ttu-id="89862-274">Los fragmentos de código siguientes muestran el uso del [**método ResourceBarproceso**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) en un ejemplo de varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="89862-274">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="89862-275">Crear la vista de galería de símbolos de profundidad y pasarla a un estado que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="89862-275">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


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



<span data-ttu-id="89862-276">Crear la vista de búfer de vértices, cambiarla primero de un estado común a un destino y, a continuación, de un destino a un estado legible genérico.</span><span class="sxs-lookup"><span data-stu-id="89862-276">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="89862-277">Crear la vista de búfer de índice, cambiarla primero de un estado común a un destino y, a continuación, de un destino a un estado legible genérico.</span><span class="sxs-lookup"><span data-stu-id="89862-277">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="89862-278">Crear texturas y vistas de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="89862-278">Creating textures and shader resource views.</span></span> <span data-ttu-id="89862-279">La textura cambia de un estado común a un destino y, a continuación, de un destino a un recurso de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="89862-279">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


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



<span data-ttu-id="89862-280">Inicio de un marco; Esto no solo usa [**ResourceBarbuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para indicar que el búfer de reserva se va a usar como destino de representación, sino que también inicializa el recurso de marco (que llama a **ResourceBarbuffer** en el búfer de la galería de símbolos de profundidad).</span><span class="sxs-lookup"><span data-stu-id="89862-280">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


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



<span data-ttu-id="89862-281">Finalizando un marco, lo que indica que el búfer de reserva ahora se usa para presentarse.</span><span class="sxs-lookup"><span data-stu-id="89862-281">Ending a frame, indicating the back buffer is now used to present.</span></span>


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



<span data-ttu-id="89862-282">Al inicializar un recurso de marco, al que se llama al iniciar un marco, se pasa el búfer de la galería de símbolos de profundidad a writeable.</span><span class="sxs-lookup"><span data-stu-id="89862-282">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


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



<span data-ttu-id="89862-283">Las barreras se intercambian a mitad del marco, lo que hace que el mapa de sombras se cambie de fácil de escribir a legible.</span><span class="sxs-lookup"><span data-stu-id="89862-283">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="89862-284">Se llama a Finish cuando finaliza un marco, con lo que se pasa el mapa de sombras a un estado común.</span><span class="sxs-lookup"><span data-stu-id="89862-284">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="89862-285">Ejemplo común de promoción de estado y decadencia</span><span class="sxs-lookup"><span data-stu-id="89862-285">Common state promotion and decay sample</span></span>

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

## <a name="example-of-split-barriers"></a><span data-ttu-id="89862-286">Ejemplo de barreras divididas</span><span class="sxs-lookup"><span data-stu-id="89862-286">Example of split barriers</span></span>

<span data-ttu-id="89862-287">En el ejemplo siguiente se muestra cómo usar una barrera de división para reducir los puestos de canalización.</span><span class="sxs-lookup"><span data-stu-id="89862-287">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="89862-288">El código siguiente no usa barreras divididas:</span><span class="sxs-lookup"><span data-stu-id="89862-288">The code that follows does not use split barriers:</span></span>

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

<span data-ttu-id="89862-289">En el código siguiente se usan barreras divididas:</span><span class="sxs-lookup"><span data-stu-id="89862-289">The following code uses split barriers:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="89862-290">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89862-290">Related topics</span></span>

[<span data-ttu-id="89862-291">Tutoriales de vídeo de aprendizaje avanzado de DirectX: Barreras de recursos y seguimiento de estado</span><span class="sxs-lookup"><span data-stu-id="89862-291">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="89862-292">Sincronización de varios motores</span><span class="sxs-lookup"><span data-stu-id="89862-292">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="89862-293">Envío de trabajo en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="89862-293">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="89862-294">Una mirada dentro de las barreras de estado de recursos D3D12</span><span class="sxs-lookup"><span data-stu-id="89862-294">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

