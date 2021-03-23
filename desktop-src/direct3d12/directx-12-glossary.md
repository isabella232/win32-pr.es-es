---
title: Glosario de Direct3D 12
description: Estos términos son distintivos de Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549167"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="61edf-103">Glosario de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="61edf-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="61edf-104">Estos términos son distintivos de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="61edf-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="61edf-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**enlace**</span><span class="sxs-lookup"><span data-stu-id="61edf-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-106">Proceso de adjuntar memoria a la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="61edf-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="61edf-107">Por ejemplo, el enlace de recursos implica el enlace de un recurso, como una textura a la canalización, para su uso en la representación de un objeto.</span><span class="sxs-lookup"><span data-stu-id="61edf-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**búfer**</span><span class="sxs-lookup"><span data-stu-id="61edf-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-109">Un tipo de recurso D3D que es sinónimo de una asignación de memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="61edf-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**lotes**</span><span class="sxs-lookup"><span data-stu-id="61edf-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-111">Un búfer de comandos que la unidad de procesamiento de gráficos (GPU) puede ejecutar solo directamente a través de una *lista de comandos directa*.</span><span class="sxs-lookup"><span data-stu-id="61edf-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="61edf-112">Una agrupación hereda todo el estado de la GPU (excepto el *objeto de estado de la canalización* establecido actualmente y la topología primitiva).</span><span class="sxs-lookup"><span data-stu-id="61edf-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**Asignador de comandos**</span><span class="sxs-lookup"><span data-stu-id="61edf-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-114">Las asignaciones de memoria subyacentes en las que se almacenan los comandos de GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="61edf-115">El objeto de asignador de comandos se aplica tanto a *las listas de comandos directas* como a las *agrupaciones*.</span><span class="sxs-lookup"><span data-stu-id="61edf-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="61edf-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-117">Una lista de comandos corresponde a un conjunto de comandos que se ejecutan en la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="61edf-118">Estos incluyen comandos como para establecer el estado, dibujar, borrar y copiar.</span><span class="sxs-lookup"><span data-stu-id="61edf-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="61edf-119">La interfaz de la lista de comandos D3D12 es significativamente diferente de la interfaz de la lista de comandos de D3D11.</span><span class="sxs-lookup"><span data-stu-id="61edf-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="61edf-120">La interfaz de la lista de comandos de D3D12 contiene API similares a las API de representación de contexto de dispositivo D3D11.</span><span class="sxs-lookup"><span data-stu-id="61edf-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="61edf-121">Una lista de comandos D3D12 no asigna ni anula la asignación de recursos, cambia las asignaciones de iconos, cambia el tamaño de los grupos de mosaicos, obtiene los datos de la consulta ni envía implícitamente comandos a la GPU para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="61edf-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="61edf-122">A diferencia de los contextos diferidos de D3D11, las listas de comandos de D3D12 solo admiten dos niveles de direccionamiento indirecto.</span><span class="sxs-lookup"><span data-stu-id="61edf-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="61edf-123">Una *lista de comandos directa* corresponde a un búfer de comandos que la GPU puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="61edf-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="61edf-124">Un *paquete* solo puede ejecutarse directamente a través de una lista de comandos directa.</span><span class="sxs-lookup"><span data-stu-id="61edf-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="61edf-125">Una lista de comandos directa no hereda ningún estado de GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="61edf-126">Una agrupación hereda todo el estado de la GPU (excepto el objeto de estado de la canalización establecido actualmente y la topología primitiva).</span><span class="sxs-lookup"><span data-stu-id="61edf-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="61edf-127">El *asignador de comandos* establece la memoria para una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="61edf-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="61edf-128">El propósito de las listas de comandos es que se pueden enviar a una GPU como una única solicitud de representación.</span><span class="sxs-lookup"><span data-stu-id="61edf-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**cola de comandos**</span><span class="sxs-lookup"><span data-stu-id="61edf-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-130">Una cola de *comandos enumera* que la GPU se ejecuta sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="61edf-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="61edf-131">Las aplicaciones deben enviar explícitamente *listas de comandos* a una cola de comandos para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="61edf-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="61edf-132">Normalmente hay tres colas de comandos: gráficos 3D, proceso y copia, que se corresponden con la canalización de gráficos 3D, el motor de proceso y uno o varios motores de copia, en la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterización conservadora**</span><span class="sxs-lookup"><span data-stu-id="61edf-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-134">La rasterización conservadora es un modo de funcionamiento para la fase de rasterización de la canalización de gráficos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="61edf-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="61edf-135">Deshabilita la rasterización estándar basada en muestras y, en su lugar, rasteriza un píxel que está incluido en cualquier cantidad por parte de una primitiva.</span><span class="sxs-lookup"><span data-stu-id="61edf-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="61edf-136">Una diferencia importante es que, mientras que cualquier cobertura produce un píxel rasterizado, esa cobertura no se puede caracterizar por el hardware, por lo que la cobertura siempre aparece como binario en un sombreador de píxeles: totalmente cubierto o no cubierto.</span><span class="sxs-lookup"><span data-stu-id="61edf-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="61edf-137">Se deja en el código del sombreador de píxeles para determinar de forma analítica la cobertura real.</span><span class="sxs-lookup"><span data-stu-id="61edf-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="61edf-138">La rasterización conservadora puede ayudar a resolver estos problemas como colisiones y detección de aciertos, discretización y eliminación de la oclusión, donde el color de un píxel es más cierto y se pueden eliminar los casos extremos.</span><span class="sxs-lookup"><span data-stu-id="61edf-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="61edf-139">Vea [rasterización conservadora](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="61edf-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Vista de búfer de constantes (CBV)**</span><span class="sxs-lookup"><span data-stu-id="61edf-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-141">Los búferes de constantes contienen datos de constantes del sombreador, como una vista de cámara, matrices de proyección y matrices mundiales.</span><span class="sxs-lookup"><span data-stu-id="61edf-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="61edf-142">Una "vista de búfer de constantes" es la vista específica del formato del búfer tal como la muestra la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="61edf-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**montón predeterminado**</span><span class="sxs-lookup"><span data-stu-id="61edf-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-144">Un montón de modo de usuario que se centra en admitir tipos de recursos de GPU persistentes, incluidos los recursos escritos por GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**scripto**</span><span class="sxs-lookup"><span data-stu-id="61edf-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-146">Los descriptores son la unidad principal de enlace para un único recurso de D3D12.</span><span class="sxs-lookup"><span data-stu-id="61edf-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="61edf-147">Un descriptor es un bloque de datos relativamente pequeño que describe por completo un objeto para la GPU, en un formato específico de GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="61edf-148">Hay muchos tipos diferentes de descriptores: las vistas de recursos del sombreador (SRVs), las vistas de acceso desordenado (UAVs), las vistas de búfer de constantes (CBVs) y los muestreadores son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="61edf-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**montón de descriptores**</span><span class="sxs-lookup"><span data-stu-id="61edf-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-150">Un montón de descriptores es una colección de asignaciones contiguas de descriptores, una asignación para cada descriptor.</span><span class="sxs-lookup"><span data-stu-id="61edf-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="61edf-151">El punto principal de un montón de descriptores consiste en abarcar la mayor parte de la asignación de memoria necesaria para almacenar las especificaciones de descriptor de tipos de objeto a los que los sombreadores hacen referencia para el tamaño de una ventana de representación lo más grande posible (lo ideal es un marco completo de representación o más).</span><span class="sxs-lookup"><span data-stu-id="61edf-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabla de descriptores**</span><span class="sxs-lookup"><span data-stu-id="61edf-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-153">Una tabla de descriptores es lógicamente una matriz de descriptores.</span><span class="sxs-lookup"><span data-stu-id="61edf-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="61edf-154">Cada tabla de descriptores almacena descriptores de uno o varios tipos, incluidos SRVs, UAVe, CBVs y muestreadores.</span><span class="sxs-lookup"><span data-stu-id="61edf-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="61edf-155">Una tabla de descriptores no es una asignación de memoria, sino simplemente un desplazamiento y una longitud en un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="61edf-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**lista de comandos directos**</span><span class="sxs-lookup"><span data-stu-id="61edf-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-157">Un búfer de comandos que la GPU puede ejecutar.</span><span class="sxs-lookup"><span data-stu-id="61edf-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="61edf-158">Una lista de comandos directa no hereda ningún estado de GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**barrera**</span><span class="sxs-lookup"><span data-stu-id="61edf-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-160">Un mecanismo para sincronizar la GPU y la CPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="61edf-161">Se puede indicar a la GPU y la CPU que esperen a una barrera, esperando en vigor para que el otro procesador se ponga al día.</span><span class="sxs-lookup"><span data-stu-id="61edf-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="61edf-162">Consulte [sincronización de varios motores](./user-mode-heap-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="61edf-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**riesgo, seguimiento de peligros**</span><span class="sxs-lookup"><span data-stu-id="61edf-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-164">Se produce un riesgo cuando se ha usado un recurso para un propósito y la aplicación intenta volver a usarlo para otro propósito.</span><span class="sxs-lookup"><span data-stu-id="61edf-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="61edf-165">Para poder usar el recurso de nuevo, es necesario vaciar o invalidar las memorias caché intermedias, los requisitos de compresión deben ser coherentes con el segundo uso y el recurso debe estar en el Estado requerido para evitar la lectura del recurso una vez que se ha escrito e invalidado para el propósito previsto.</span><span class="sxs-lookup"><span data-stu-id="61edf-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="61edf-166">El proceso de mantenimiento de los recursos y la prevención de estos problemas de sincronización se conoce como seguimiento de peligros.</span><span class="sxs-lookup"><span data-stu-id="61edf-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="61edf-167">Si el controlador no realiza ningún seguimiento de los peligros, la aplicación es responsable de ello.</span><span class="sxs-lookup"><span data-stu-id="61edf-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="61edf-168">En la mayoría de las versiones anteriores de DirectX, el seguimiento del riesgo lo controlaba el controlador.</span><span class="sxs-lookup"><span data-stu-id="61edf-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="61edf-169">Para mejorar el rendimiento, los métodos sin seguimiento de peligros están disponibles en DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="61edf-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Lenguaje de sombreador de alto nivel (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="61edf-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-171">Un lenguaje informático, similar pero distinto en muchas formas de C, que se usa para escribir código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="61edf-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="61edf-172">Todos los sombreadores de vértices, píxeles, Geometry, compute, Domain y casco se escriben con HLSL.</span><span class="sxs-lookup"><span data-stu-id="61edf-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="61edf-173">Un compilador convierte el origen de HLSL en un formato binario para que lo consuma la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimotor**</span><span class="sxs-lookup"><span data-stu-id="61edf-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-175">Las distintas instancias y tipos de motores en una sola GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="61edf-176">Los tipos de motores incluyen: gráficos, proceso y copia.</span><span class="sxs-lookup"><span data-stu-id="61edf-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span><span class="sxs-lookup"><span data-stu-id="61edf-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-178">Una configuración de hardware donde hay más de un adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="61edf-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="61edf-179">A veces, a los adaptadores independientes se les denomina nodos.</span><span class="sxs-lookup"><span data-stu-id="61edf-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="61edf-180">El hecho de tener varias GPU puede hacer que la tarea de sincronizarlas con la CPU y entre ellas sea considerablemente más compleja que con una sola GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objeto de estado de canalización (PSO)**</span><span class="sxs-lookup"><span data-stu-id="61edf-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-182">Una parte significativa del estado de la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="61edf-183">Este estado incluye todos los sombreadores establecidos actualmente y determinados objetos de estado de función fija.</span><span class="sxs-lookup"><span data-stu-id="61edf-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="61edf-184">La única manera de cambiar los Estados contenidos en el objeto de canalización es cambiar el objeto de canalización enlazado actualmente.</span><span class="sxs-lookup"><span data-stu-id="61edf-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span><span class="sxs-lookup"><span data-stu-id="61edf-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-186">Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.</span><span class="sxs-lookup"><span data-stu-id="61edf-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="61edf-187">Por ejemplo, si un cuadro de límite de un objeto es totalmente ocluidos por otro objeto o la perspectiva ha reducido el objeto a un tamaño menor que el de un píxel, puede que no haya ningún punto intentando dibujar el objeto oculto.</span><span class="sxs-lookup"><span data-stu-id="61edf-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="61edf-188">Vea [Predication](predication.md).</span><span class="sxs-lookup"><span data-stu-id="61edf-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Vista de orden de rasterizador (ROV)**</span><span class="sxs-lookup"><span data-stu-id="61edf-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-190">Las canalizaciones de gráficos estándar pueden tener problemas al componer varias texturas que contienen transparencias correctamente.</span><span class="sxs-lookup"><span data-stu-id="61edf-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="61edf-191">Los objetos como las barreras de alambres, humos, incendios, vegetación y vidrio en color usan transparencia para obtener el efecto deseado.</span><span class="sxs-lookup"><span data-stu-id="61edf-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="61edf-192">Surgen problemas cuando varias texturas que contienen transparencias están alineadas entre sí (humo delante de una barrera delante de un edificio de vidrio que contiene vegetación, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="61edf-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="61edf-193">Las vistas ordenadas de rasterizador (ROVs) permiten que los algoritmos subyacentes de transparencia independiente de orden (OIT) usen características del hardware para intentar resolver el orden de transparencia correctamente.</span><span class="sxs-lookup"><span data-stu-id="61edf-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="61edf-194">El sombreador de píxeles controla la transparencia.</span><span class="sxs-lookup"><span data-stu-id="61edf-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="61edf-195">Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de vista de acceso desordenado (UAV) con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.</span><span class="sxs-lookup"><span data-stu-id="61edf-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**montón readback**</span><span class="sxs-lookup"><span data-stu-id="61edf-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-197">Un montón de modo de usuario que se centra en la transferencia de datos desde la GPU de vuelta a la CPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**recurso**</span><span class="sxs-lookup"><span data-stu-id="61edf-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-199">Una entidad que proporciona datos a la canalización y define lo que se representa durante la escena.</span><span class="sxs-lookup"><span data-stu-id="61edf-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="61edf-200">Los recursos se pueden cargar desde el medio de juego o se pueden crear dinámicamente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="61edf-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="61edf-201">Normalmente, los recursos incluyen datos de textura, datos de vértices y datos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="61edf-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="61edf-202">La mayoría de las aplicaciones de Direct3D crean y destruyen los recursos mucho a lo largo de su duración.</span><span class="sxs-lookup"><span data-stu-id="61edf-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barrera de recursos**</span><span class="sxs-lookup"><span data-stu-id="61edf-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-204">Una barrera de recursos notifica al controlador que se puede requerir la sincronización de varios accesos a un único recurso, por ejemplo, para leer y escribir en la misma textura.</span><span class="sxs-lookup"><span data-stu-id="61edf-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**enlace de recursos**</span><span class="sxs-lookup"><span data-stu-id="61edf-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-206">El enlace de recursos es el proceso de vinculación de recursos (texturas, búferes de vértices, búferes de índice, etc.) a la canalización de gráficos, lo que permite a los sombreadores de la canalización procesar el recurso correcto.</span><span class="sxs-lookup"><span data-stu-id="61edf-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**montones de recursos**</span><span class="sxs-lookup"><span data-stu-id="61edf-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-208">Los montones de recursos son un término genérico para los montones que son búferes de memoria que se reservan para contener recursos a medida que se transfieren hacia y desde la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="61edf-209">Una transferencia a la GPU requiere un montón de carga, de la GPU a la CPU requiere un montón de Readback y un montón persistente para que la GPU se mantenga en varios fotogramas de representación se denomina montón predeterminado.</span><span class="sxs-lookup"><span data-stu-id="61edf-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma raíz**</span><span class="sxs-lookup"><span data-stu-id="61edf-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-211">Las signaturas raíz definen todos los recursos que se van a enlazar a las canalizaciones de gráficos o de proceso.</span><span class="sxs-lookup"><span data-stu-id="61edf-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="61edf-212">Las listas de comandos de la aplicación y de vínculos configuran una firma raíz para los recursos que los sombreadores requieren normalmente, hay un gráfico y una firma de raíz de proceso por aplicación.</span><span class="sxs-lookup"><span data-stu-id="61edf-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**muestras**</span><span class="sxs-lookup"><span data-stu-id="61edf-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-214">Una muestra es el código que lee de una textura.</span><span class="sxs-lookup"><span data-stu-id="61edf-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Sombreador Vista de recursos (SRV)**</span><span class="sxs-lookup"><span data-stu-id="61edf-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-216">Una forma específica del formato de ver los datos de un recurso de sombreador, como una textura.</span><span class="sxs-lookup"><span data-stu-id="61edf-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**montón estático**</span><span class="sxs-lookup"><span data-stu-id="61edf-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-218">Un montón de modo de usuario que se centra en varios recursos de solo lectura de GPU que se usan normalmente al mismo tiempo y que no cambian con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="61edf-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**cadena de intercambio**</span><span class="sxs-lookup"><span data-stu-id="61edf-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-220">Las cadenas de intercambio controlan la rotación del búfer de reserva, formando la base de la animación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="61edf-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="61edf-221">Las cadenas de intercambio se controlan mediante el conjunto de API de bajo nivel de DXGI (consulte [información general sobre dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="61edf-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="61edf-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span><span class="sxs-lookup"><span data-stu-id="61edf-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-223">Técnica de ubicación de datos multidimensionales en memoria de modo que los datos de la dimensionalidad cercana suelen tener direcciones cercanas.</span><span class="sxs-lookup"><span data-stu-id="61edf-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="61edf-224">En concreto, todos los datos de una fila no se colocan de forma contigua delante de los datos de la fila siguiente.</span><span class="sxs-lookup"><span data-stu-id="61edf-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="61edf-225">Un "Swizzle con parámetros" describe una forma estandarizada de describir patrones de swizzle.</span><span class="sxs-lookup"><span data-stu-id="61edf-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**degrada**</span><span class="sxs-lookup"><span data-stu-id="61edf-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-227">Un tipo de recurso D3D que es multidimensional y tiene un diseño de memoria que está optimizado para el acceso multidimensional desde la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="61edf-228">Las texturas suelen contener la imagen sin procesar necesaria para representarla en una superficie, antes de que tenga lugar la iluminación y la fusión, pero puede contener otras formas de datos, como degradados de color y colores de referencia.</span><span class="sxs-lookup"><span data-stu-id="61edf-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="61edf-229">Direct3D 12 admite texturas de una, dos y tres dimensiones.</span><span class="sxs-lookup"><span data-stu-id="61edf-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**posición**</span><span class="sxs-lookup"><span data-stu-id="61edf-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-231">Página de memoria de vídeo, similar a una página de CPU/sistema de memoria.</span><span class="sxs-lookup"><span data-stu-id="61edf-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="61edf-232">La notación de mosaico ayuda a distinguir el subsistema de memoria virtual de GPU del subsistema de memoria virtual de CPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="61edf-233">Las GPU proporcionan capacidades de memoria virtual similares como memoria virtual del sistema.</span><span class="sxs-lookup"><span data-stu-id="61edf-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="61edf-234">Algunas GPU tienen capacidades de memoria virtual compartidas, que permiten el uso compartido de algunas páginas del subsistema de memoria virtual con la CPU y la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**recursos en mosaico**</span><span class="sxs-lookup"><span data-stu-id="61edf-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-236">Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de GPU, y el hardware puede comprender cómo filtrar por los mosaicos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="61edf-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="61edf-237">Los recursos en mosaico son recursos lógicos de gran tamaño, pero requieren pequeñas cantidades de memoria física.</span><span class="sxs-lookup"><span data-stu-id="61edf-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Vista de acceso desordenado (UAV)**</span><span class="sxs-lookup"><span data-stu-id="61edf-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-239">Una vista de acceso desordenado en un recurso (que incluye búferes, texturas y matrices de texturas, sin muestreo múltiple), permite el acceso de lectura y escritura desordenado temporal desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="61edf-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="61edf-240">Esto significa que varios subprocesos pueden leer o escribir este tipo de recurso simultáneamente sin generar conflictos de memoria.</span><span class="sxs-lookup"><span data-stu-id="61edf-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**cargar montón**</span><span class="sxs-lookup"><span data-stu-id="61edf-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-242">Un montón de modo de usuario que se centra en la transferencia de datos desde la CPU a la GPU.</span><span class="sxs-lookup"><span data-stu-id="61edf-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**montón de modo de usuario**</span><span class="sxs-lookup"><span data-stu-id="61edf-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-244">Colección de asignaciones de memoria grandes y contiguas que se reciclan sin ningún conocimiento del componente kernel: los métodos de asignación y destrucción no llaman a los métodos de asignación y destrucción del kernel durante el estado estable.</span><span class="sxs-lookup"><span data-stu-id="61edf-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="61edf-245">Los montones de carga, Readback y predeterminado son variantes de montones de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="61edf-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="61edf-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**recursos en mosaico de volumen**</span><span class="sxs-lookup"><span data-stu-id="61edf-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="61edf-247">[Recursos en mosaico](/windows)tridimensionales.</span><span class="sxs-lookup"><span data-stu-id="61edf-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 