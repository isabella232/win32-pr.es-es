---
title: Sincronización de varios motores
description: En este tema se describe la sincronización del acceso a varios motores independientes que se encuentran en la mayoría de las GPU modernas.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2020
ms.locfileid: "104549065"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="e8081-103">Sincronización de varios motores</span><span class="sxs-lookup"><span data-stu-id="e8081-103">Multi-engine synchronization</span></span>

<span data-ttu-id="e8081-104">La mayoría de las GPU modernas contienen varios motores independientes que proporcionan una funcionalidad especializada.</span><span class="sxs-lookup"><span data-stu-id="e8081-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="e8081-105">Muchos tienen uno o más motores de copia dedicados y un motor de proceso, que normalmente es distinto del motor 3D.</span><span class="sxs-lookup"><span data-stu-id="e8081-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="e8081-106">Cada uno de estos motores puede ejecutar comandos en paralelo entre sí.</span><span class="sxs-lookup"><span data-stu-id="e8081-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="e8081-107">Direct3D 12 proporciona acceso específico a los motores 3D, de proceso y de copia mediante colas y listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="e8081-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="e8081-108">Motores de GPU</span><span class="sxs-lookup"><span data-stu-id="e8081-108">GPU engines</span></span>

<span data-ttu-id="e8081-109">En el diagrama siguiente se muestran los subprocesos de la CPU de un título, cada uno de los cuales rellena una o varias colas de copia, proceso y 3D.</span><span class="sxs-lookup"><span data-stu-id="e8081-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="e8081-110">La cola 3D puede impulsar los tres motores de GPU; la cola de proceso puede impulsar los motores de proceso y de copia; y la cola de copia simplemente el motor de copia.</span><span class="sxs-lookup"><span data-stu-id="e8081-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="e8081-111">A medida que los distintos subprocesos rellenan las colas, no puede haber ninguna garantía sencilla del orden de ejecución, por lo tanto, la necesidad de mecanismos de sincronización &mdash; cuando el título los requiere.</span><span class="sxs-lookup"><span data-stu-id="e8081-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![cuatro subprocesos que envían comandos a tres colas](images/gpu-engines.png)

<span data-ttu-id="e8081-113">En la imagen siguiente se muestra cómo un título puede programar el trabajo en varios motores de GPU, incluida la sincronización entre motores cuando sea necesario: muestra las cargas de trabajo por motor con dependencias entre motores.</span><span class="sxs-lookup"><span data-stu-id="e8081-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="e8081-114">En este ejemplo, el motor de copia copia primero parte de la geometría necesaria para la representación.</span><span class="sxs-lookup"><span data-stu-id="e8081-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="e8081-115">El motor 3D espera a que se completen estas copias y representa un paso previo de la geometría.</span><span class="sxs-lookup"><span data-stu-id="e8081-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="e8081-116">Después, el motor de proceso lo usa.</span><span class="sxs-lookup"><span data-stu-id="e8081-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="e8081-117">Los resultados de la [**distribución**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motor de proceso, junto con varias operaciones de copia de textura en el motor de copia, se consumen en el motor 3D para la llamada de [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.</span><span class="sxs-lookup"><span data-stu-id="e8081-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![copia, gráficos y motores de proceso que se comunican](images/gpu-sync.png)

<span data-ttu-id="e8081-119">En el siguiente pseudocódigo se muestra cómo un título puede enviar este tipo de carga de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e8081-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

<span data-ttu-id="e8081-120">En el siguiente pseudocódigo se muestra la sincronización entre los motores de copia y 3D para realizar la asignación de memoria de tipo montón a través de un búfer en anillo.</span><span class="sxs-lookup"><span data-stu-id="e8081-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="e8081-121">Los títulos tienen la flexibilidad de elegir el equilibrio adecuado entre maximizar el paralelismo (a través de un búfer grande) y reducir el consumo de memoria y la latencia (a través de un búfer pequeño).</span><span class="sxs-lookup"><span data-stu-id="e8081-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a><span data-ttu-id="e8081-122">Escenarios de varios motores</span><span class="sxs-lookup"><span data-stu-id="e8081-122">Multi-engine scenarios</span></span>

<span data-ttu-id="e8081-123">Direct3D 12 le permite evitar la ejecución accidental de ineficiencias producidas por retrasos inesperados en la sincronización.</span><span class="sxs-lookup"><span data-stu-id="e8081-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="e8081-124">También permite introducir la sincronización en un nivel superior en el que se puede determinar la sincronización necesaria con mayor certeza.</span><span class="sxs-lookup"><span data-stu-id="e8081-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="e8081-125">Un segundo problema que trata las direcciones de varios motores es hacer que las operaciones costosas sean más explícitas, lo que incluye las transiciones entre el vídeo y el 3D que tradicionalmente eran costosas debido a la sincronización entre varios contextos de kernel.</span><span class="sxs-lookup"><span data-stu-id="e8081-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="e8081-126">En concreto, se pueden solucionar los siguientes escenarios con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e8081-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="e8081-127">Trabajo de GPU asincrónica y de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="e8081-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="e8081-128">Esto permite la ejecución simultánea de trabajo de GPU de baja prioridad y operaciones atómicas que permiten que un subproceso de GPU consuma los resultados de otro subproceso no sincronizado sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="e8081-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="e8081-129">Trabajo de proceso de alta prioridad.</span><span class="sxs-lookup"><span data-stu-id="e8081-129">High priority compute work.</span></span> <span data-ttu-id="e8081-130">Con el proceso en segundo plano es posible interrumpir la representación en 3D para realizar una pequeña cantidad de trabajo de proceso de alta prioridad.</span><span class="sxs-lookup"><span data-stu-id="e8081-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="e8081-131">Los resultados de este trabajo pueden obtenerse pronto para el procesamiento adicional de la CPU.</span><span class="sxs-lookup"><span data-stu-id="e8081-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="e8081-132">Trabajo de proceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e8081-132">Background compute work.</span></span> <span data-ttu-id="e8081-133">Una cola de baja prioridad independiente para cargas de trabajo de proceso permite que una aplicación Use ciclos de GPU de reserva para realizar el cálculo en segundo plano sin un impacto negativo en las tareas de representación principal (u otras).</span><span class="sxs-lookup"><span data-stu-id="e8081-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="e8081-134">Las tareas en segundo plano pueden incluir la descompresión de recursos o la actualización de simulaciones o estructuras de aceleración.</span><span class="sxs-lookup"><span data-stu-id="e8081-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="e8081-135">Las tareas en segundo plano deben sincronizarse en la CPU con poca frecuencia (aproximadamente una vez por fotograma) para evitar la detención o la ralentización del trabajo en primer plano.</span><span class="sxs-lookup"><span data-stu-id="e8081-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="e8081-136">Transmisión por secuencias y carga de datos.</span><span class="sxs-lookup"><span data-stu-id="e8081-136">Streaming and uploading data.</span></span> <span data-ttu-id="e8081-137">Una cola de copia independiente reemplaza los conceptos de D3D11 de los datos iniciales y los recursos de actualización.</span><span class="sxs-lookup"><span data-stu-id="e8081-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="e8081-138">Aunque la aplicación es responsable de obtener más detalles en el modelo de Direct3D 12, esta responsabilidad se refiere a la eficacia.</span><span class="sxs-lookup"><span data-stu-id="e8081-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="e8081-139">La aplicación puede controlar la cantidad de memoria del sistema dedicada a almacenar en búfer los datos de carga.</span><span class="sxs-lookup"><span data-stu-id="e8081-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="e8081-140">La aplicación puede elegir cuándo y cómo (CPU frente a GPU, bloqueo frente a no bloqueo) sincronizar y puede realizar un seguimiento del progreso y controlar la cantidad de trabajo en cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="e8081-141">Mayor paralelismo.</span><span class="sxs-lookup"><span data-stu-id="e8081-141">Increased parallelism.</span></span> <span data-ttu-id="e8081-142">Las aplicaciones pueden usar colas más profundas para cargas de trabajo en segundo plano (por ejemplo, descodificación de vídeo) cuando tienen colas independientes para el trabajo en primer plano.</span><span class="sxs-lookup"><span data-stu-id="e8081-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="e8081-143">En Direct3D 12, el concepto de una cola de comandos es la representación de la API de una secuencia de trabajo de serie de aproximadamente que envía la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e8081-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="e8081-144">Las barreras y otras técnicas permiten que este trabajo se ejecute en una canalización o desordenado, pero la aplicación solo ve una escala de tiempo de finalización única.</span><span class="sxs-lookup"><span data-stu-id="e8081-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="e8081-145">Esto corresponde al contexto inmediato en D3D11.</span><span class="sxs-lookup"><span data-stu-id="e8081-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="e8081-146">API de sincronización</span><span class="sxs-lookup"><span data-stu-id="e8081-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="e8081-147">Dispositivos y colas</span><span class="sxs-lookup"><span data-stu-id="e8081-147">Devices and queues</span></span>

<span data-ttu-id="e8081-148">El dispositivo Direct3D 12 tiene métodos para crear y recuperar colas de comandos de diferentes tipos y prioridades.</span><span class="sxs-lookup"><span data-stu-id="e8081-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="e8081-149">La mayoría de las aplicaciones deben usar las colas de comandos predeterminadas porque permiten el uso compartido por parte de otros componentes.</span><span class="sxs-lookup"><span data-stu-id="e8081-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="e8081-150">Las aplicaciones con requisitos de simultaneidad adicionales pueden crear colas adicionales.</span><span class="sxs-lookup"><span data-stu-id="e8081-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="e8081-151">Las colas se especifican mediante el tipo de lista de comandos que consumen.</span><span class="sxs-lookup"><span data-stu-id="e8081-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="e8081-152">Consulte los siguientes métodos de creación de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="e8081-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="e8081-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una cola de comandos basada en información en una estructura de DESC de la [**cola de comandos de Direct3D 12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="e8081-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="e8081-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crea una lista de comandos del tipo de [**lista de comandos de Direct3D 12 \_ \_ \_**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="e8081-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="e8081-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crea una barrera, anotando las marcas en las [**marcas de \_ barrera \_ de Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span><span class="sxs-lookup"><span data-stu-id="e8081-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="e8081-156">Las barreras se utilizan para sincronizar las colas.</span><span class="sxs-lookup"><span data-stu-id="e8081-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="e8081-157">Las colas de todos los tipos (3D, Compute y Copy) comparten la misma interfaz y están basadas en todas las listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="e8081-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="e8081-158">Consulte los siguientes métodos de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="e8081-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="e8081-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : envía una matriz de listas de comandos para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="e8081-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="e8081-160">Cada lista de comandos definida por [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="e8081-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="e8081-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : establece un valor de barrera cuando la cola (que se ejecuta en la GPU) alcanza un punto determinado.</span><span class="sxs-lookup"><span data-stu-id="e8081-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="e8081-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la cola espera hasta que la barrera especificada alcance el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e8081-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="e8081-163">Tenga en cuenta que los conjuntos no se consumen en ninguna cola y, por lo tanto, este tipo no se puede usar para crear una cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="e8081-164">Barreras</span><span class="sxs-lookup"><span data-stu-id="e8081-164">Fences</span></span>

<span data-ttu-id="e8081-165">La API de varios motores proporciona API explícitas para crear y sincronizar mediante barreras.</span><span class="sxs-lookup"><span data-stu-id="e8081-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="e8081-166">Una barrera es una construcción de sincronización controlada por un valor UINT64.</span><span class="sxs-lookup"><span data-stu-id="e8081-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="e8081-167">La aplicación establece los valores de barrera.</span><span class="sxs-lookup"><span data-stu-id="e8081-167">Fence values are set by the application.</span></span> <span data-ttu-id="e8081-168">Una operación Signal modifica el valor de barrera y una operación de espera se bloquea hasta que la barrera alcanza el valor solicitado o mayor.</span><span class="sxs-lookup"><span data-stu-id="e8081-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="e8081-169">Se puede desencadenar un evento cuando una barrera alcanza un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="e8081-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="e8081-170">Consulte los métodos de la interfaz [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .</span><span class="sxs-lookup"><span data-stu-id="e8081-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="e8081-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : devuelve el valor actual de la barrera.</span><span class="sxs-lookup"><span data-stu-id="e8081-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="e8081-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : hace que se desencadene un evento cuando la barrera alcanza un valor determinado.</span><span class="sxs-lookup"><span data-stu-id="e8081-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="e8081-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : establece la barrera en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="e8081-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="e8081-174">Las barreras permiten el acceso de CPU al valor de barrera actual y esperas y señales de CPU.</span><span class="sxs-lookup"><span data-stu-id="e8081-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="e8081-175">El método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) de la interfaz [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) actualiza una barrera del lado de la CPU.</span><span class="sxs-lookup"><span data-stu-id="e8081-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="e8081-176">Esta actualización se produce inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e8081-176">This update occurs immediately.</span></span> <span data-ttu-id="e8081-177">El método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) actualiza una barrera del lado de la GPU.</span><span class="sxs-lookup"><span data-stu-id="e8081-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="e8081-178">Esta actualización se produce cuando se han completado todas las demás operaciones en la cola de comandos.</span><span class="sxs-lookup"><span data-stu-id="e8081-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="e8081-179">Todos los nodos de una configuración de varios motores pueden leer y reaccionar a cualquier barrera que alcance el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="e8081-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="e8081-180">Las aplicaciones establecen sus propios valores de barrera, un buen punto de partida puede estar aumentando una barrera una vez por fotograma.</span><span class="sxs-lookup"><span data-stu-id="e8081-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="e8081-181">Se *puede* *rebobinar* una barrera.</span><span class="sxs-lookup"><span data-stu-id="e8081-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="e8081-182">Esto significa que no es necesario que el valor de barrera se incremente únicamente.</span><span class="sxs-lookup"><span data-stu-id="e8081-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="e8081-183">Si una operación de **señal** se pone en cola en dos colas de comandos diferentes, o si dos subprocesos de CPU están llamando a **señal** en una barrera, puede haber una carrera para determinar qué **señal** se completa en último lugar y, por lo tanto, qué valor de barrera es el que permanecerá.</span><span class="sxs-lookup"><span data-stu-id="e8081-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="e8081-184">Si se rebobina una barrera, las nuevas esperas (incluidas las solicitudes de **SetEventOnCompletion** ) se compararán con el nuevo valor de barrera inferior y, por lo tanto, no se cumplirán, incluso si el valor de barrera hubiera sido lo suficientemente alto como para satisfacerlos.</span><span class="sxs-lookup"><span data-stu-id="e8081-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="e8081-185">Si se produce una carrera, entre un valor que satisfará una espera pendiente y un valor inferior no *, se cumplirá la espera independientemente* del valor que quede después.</span><span class="sxs-lookup"><span data-stu-id="e8081-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="e8081-186">Las API de barrera proporcionan una eficaz funcionalidad de sincronización, pero pueden provocar problemas de depuración.</span><span class="sxs-lookup"><span data-stu-id="e8081-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="e8081-187">Se recomienda usar cada barrera para indicar el progreso en una escala de tiempo con el fin de evitar carreras entre señalizadores.</span><span class="sxs-lookup"><span data-stu-id="e8081-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="e8081-188">Copiar y calcular listas de comandos</span><span class="sxs-lookup"><span data-stu-id="e8081-188">Copy and compute command lists</span></span>

<span data-ttu-id="e8081-189">Los tres tipos de lista de comandos usan la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , pero solo se admite un subconjunto de los métodos para copiar y calcular.</span><span class="sxs-lookup"><span data-stu-id="e8081-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="e8081-190">Las listas de comandos de copia y cálculo pueden usar los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8081-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="e8081-191">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="e8081-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="e8081-192">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="e8081-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="e8081-193">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="e8081-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="e8081-194">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="e8081-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="e8081-195">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="e8081-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="e8081-196">**Determinado**</span><span class="sxs-lookup"><span data-stu-id="e8081-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="e8081-197">**ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="e8081-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="e8081-198">Las listas de comandos de Compute también pueden usar los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8081-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="e8081-199">**ClearState**</span><span class="sxs-lookup"><span data-stu-id="e8081-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="e8081-200">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="e8081-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="e8081-201">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="e8081-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="e8081-202">**DiscardResource**</span><span class="sxs-lookup"><span data-stu-id="e8081-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="e8081-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="e8081-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="e8081-204">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="e8081-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="e8081-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="e8081-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="e8081-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="e8081-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="e8081-207">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="e8081-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="e8081-208">**SetComputeRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="e8081-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="e8081-209">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="e8081-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="e8081-210">**SetComputeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e8081-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="e8081-211">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="e8081-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="e8081-212">**SetDescriptorHeaps**</span><span class="sxs-lookup"><span data-stu-id="e8081-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="e8081-213">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="e8081-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="e8081-214">**SetPredication**</span><span class="sxs-lookup"><span data-stu-id="e8081-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="e8081-215">Las listas de comandos de Compute deben establecer un valor de Compute PSO al llamar a [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span><span class="sxs-lookup"><span data-stu-id="e8081-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="e8081-216">Los paquetes no se pueden usar con las listas o colas de comandos de proceso o copia.</span><span class="sxs-lookup"><span data-stu-id="e8081-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="e8081-217">Ejemplo de proceso y gráficos de canalización</span><span class="sxs-lookup"><span data-stu-id="e8081-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="e8081-218">En este ejemplo se muestra cómo se puede usar la sincronización de barrera para crear una canalización de trabajo de proceso en una cola (a la que hace referencia `pComputeQueue` ) que se usa en el trabajo de gráficos en la cola `pGraphicsQueue` .</span><span class="sxs-lookup"><span data-stu-id="e8081-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="e8081-219">El trabajo de cálculo y gráficos se canaliza con la cola de gráficos que consume el resultado del trabajo de proceso de varios fotogramas, y se utiliza un evento de CPU para limitar el trabajo total en cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

<span data-ttu-id="e8081-220">Para admitir esta canalización, debe haber un búfer de `ComputeGraphicsLatency+1` diferentes copias de los datos que pasan de la cola de proceso a la cola de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e8081-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="e8081-221">Las listas de comandos deben usar UAVs e direccionamiento indirecto para leer y escribir desde la "versión" adecuada de los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="e8081-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="e8081-222">La cola de proceso debe esperar hasta que la cola de gráficos haya terminado de leer los datos del marco N para poder escribir el marco `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="e8081-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="e8081-223">Tenga en cuenta que la cantidad de la cola de proceso que funcionaba con respecto a la CPU no depende directamente de la cantidad de almacenamiento en búfer requerida. sin embargo, el trabajo de GPU de cola más allá de la cantidad de espacio en búfer disponible es menos valioso.</span><span class="sxs-lookup"><span data-stu-id="e8081-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="e8081-224">Un mecanismo alternativo para evitar el direccionamiento indirecto sería crear varias listas de comandos correspondientes a cada una de las versiones "cambiadas de nombre" de los datos.</span><span class="sxs-lookup"><span data-stu-id="e8081-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="e8081-225">En el ejemplo siguiente se usa esta técnica mientras se amplía el ejemplo anterior para permitir que las colas de proceso y de gráficos se ejecuten de forma más asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e8081-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="e8081-226">Ejemplo de cálculo y gráficos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="e8081-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="e8081-227">En el ejemplo siguiente, los gráficos se pueden representar de forma asincrónica desde la cola de proceso.</span><span class="sxs-lookup"><span data-stu-id="e8081-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="e8081-228">Todavía existe una cantidad fija de datos almacenados en búfer entre las dos fases; sin embargo, ahora el trabajo de gráficos se realiza de forma independiente y usa el resultado más actualizado de la fase de proceso como se conoce en la CPU cuando el trabajo de gráficos se pone en cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="e8081-229">Esto sería útil si otro origen estaba actualizando el trabajo de gráficos, por ejemplo, datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e8081-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="e8081-230">Debe haber varias listas de comandos para permitir `ComputeGraphicsLatency` que los fotogramas de los gráficos funcionen al mismo tiempo, y la función `UpdateGraphicsCommandList` representa la actualización de la lista de comandos para incluir los datos de entrada más recientes y leer los datos de proceso del búfer adecuado.</span><span class="sxs-lookup"><span data-stu-id="e8081-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="e8081-231">La cola de proceso debe esperar a que la cola de gráficos finalice con los búferes de canalización, pero se ha introducido una tercera barrera ( `pGraphicsComputeFence` ) para que se pueda realizar un seguimiento del progreso de los gráficos que leen el trabajo de cálculo y el progreso de gráficos en general.</span><span class="sxs-lookup"><span data-stu-id="e8081-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="e8081-232">Esto refleja el hecho de que los fotogramas de gráficos consecutivos podrían leer el mismo resultado de proceso u omitir un resultado de proceso.</span><span class="sxs-lookup"><span data-stu-id="e8081-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="e8081-233">Un diseño más eficaz pero ligeramente más complicado usaría solo la barrera de gráficos única y almacenaría una asignación a las tramas de proceso utilizadas por cada fotograma gráfico.</span><span class="sxs-lookup"><span data-stu-id="e8081-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a><span data-ttu-id="e8081-234">Acceso a recursos de varias colas</span><span class="sxs-lookup"><span data-stu-id="e8081-234">Multi-queue resource access</span></span>

<span data-ttu-id="e8081-235">Para tener acceso a un recurso de más de una cola, una aplicación debe cumplir las siguientes reglas.</span><span class="sxs-lookup"><span data-stu-id="e8081-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="e8081-236">El acceso a los recursos (consulte [**\_ \_ Estados de recursos de Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) viene determinado por la clase de tipo de cola no es un objeto de cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="e8081-237">Hay dos clases de tipo de cola: Compute/3D Queue es una clase de tipo, Copy es una segunda clase de tipo.</span><span class="sxs-lookup"><span data-stu-id="e8081-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="e8081-238">Por lo tanto, un recurso que tiene una barrera para el \_ \_ Estado del recurso de sombreador que no es de píxeles \_ en una cola 3D se puede usar en ese estado en cualquier cola 3D o de proceso, en función de los requisitos de sincronización que requieren la mayoría de las escrituras que se van a serializar.</span><span class="sxs-lookup"><span data-stu-id="e8081-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="e8081-239">Los Estados de los recursos que se comparten entre las dos clases de tipo (copia de \_ origen y \_ destino de copia) se consideran Estados diferentes para cada clase de tipo.</span><span class="sxs-lookup"><span data-stu-id="e8081-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="e8081-240">De modo que si un recurso realiza la transición al destino \_ de copia en una cola de copia, no se puede acceder a él como destino de copia de las colas 3D o de proceso, y viceversa.</span><span class="sxs-lookup"><span data-stu-id="e8081-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="e8081-241">En resumen.</span><span class="sxs-lookup"><span data-stu-id="e8081-241">To summarize.</span></span>

    -   <span data-ttu-id="e8081-242">Un "objeto" de la cola es una sola cola.</span><span class="sxs-lookup"><span data-stu-id="e8081-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="e8081-243">Una cola "tipo" es cualquiera de estas tres: compute, 3D y Copy.</span><span class="sxs-lookup"><span data-stu-id="e8081-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="e8081-244">Una cola "clase de tipo" es cualquiera de estas dos: Compute/3D y Copy.</span><span class="sxs-lookup"><span data-stu-id="e8081-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="e8081-245">Las marcas de copia (copia del destino y el origen de la copia \_ \_ ) utilizadas como Estados iniciales representan los Estados de la clase de tipo de proceso o 3D.</span><span class="sxs-lookup"><span data-stu-id="e8081-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="e8081-246">Para usar un recurso inicialmente en una cola de copia, debe comenzar en el Estado común.</span><span class="sxs-lookup"><span data-stu-id="e8081-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="e8081-247">El Estado común se puede usar para todos los usos de una cola de copia mediante las transiciones de estado implícitas.</span><span class="sxs-lookup"><span data-stu-id="e8081-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="e8081-248">Aunque el estado del recurso se comparte entre todas las colas de proceso y 3D, no se permite escribir en el recurso simultáneamente en diferentes colas.</span><span class="sxs-lookup"><span data-stu-id="e8081-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="e8081-249">"Simultáneamente" significa que no está sincronizado. la ejecución no sincronizada no es posible en algún hardware.</span><span class="sxs-lookup"><span data-stu-id="e8081-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="e8081-250">Se aplican las siguientes reglas.</span><span class="sxs-lookup"><span data-stu-id="e8081-250">The following rules apply.</span></span>

    -   <span data-ttu-id="e8081-251">Solo una cola puede escribir en un recurso a la vez.</span><span class="sxs-lookup"><span data-stu-id="e8081-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="e8081-252">Varias colas pueden leer desde el recurso siempre que no lean los bytes modificados por el escritor (la lectura de bytes que se escriben simultáneamente genera resultados no definidos).</span><span class="sxs-lookup"><span data-stu-id="e8081-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="e8081-253">Una barrera debe usarse para sincronizar después de la escritura antes de que otra cola pueda leer los bytes escritos o realizar un acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="e8081-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="e8081-254">Los búferes de reserva que se presentan deben estar en \_ el \_ Estado común de estado de los recursos de Direct3D 12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e8081-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="e8081-255">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8081-255">Related topics</span></span>

[<span data-ttu-id="e8081-256">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e8081-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="e8081-257">Usar barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e8081-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="e8081-258">Administración de la memoria en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e8081-258">Memory management in Direct3D 12</span></span>](memory-management.md)
