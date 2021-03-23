---
title: Canalizaciones y sombreadores con Direct3D 12
description: La canalización programable de Direct3D 12 aumenta considerablemente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104549103"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="95fae-103">Canalizaciones y sombreadores con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="95fae-104">La canalización programable de Direct3D 12 aumenta considerablemente el rendimiento de la representación en comparación con las interfaces de programación de gráficos de generación anterior.</span><span class="sxs-lookup"><span data-stu-id="95fae-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="95fae-105">Canalización de gráficos de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="95fae-106">Objetos de estado de canalización</span><span class="sxs-lookup"><span data-stu-id="95fae-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="95fae-107">Canalización de proceso de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="95fae-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95fae-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="95fae-109">Canalización de gráficos de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="95fae-110">En el diagrama siguiente se muestra el estado y la canalización de gráficos de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="95fae-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![diagrama que ilustra el estado y la canalización de Direct3D 12](images/pipeline.png)

<span data-ttu-id="95fae-112">Una canalización de gráficos es el flujo secuencial de entradas y salidas de datos a medida que la GPU representa los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="95fae-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="95fae-113">Dado el estado y las entradas de la canalización, la GPU realiza una serie de operaciones para crear las imágenes resultantes.</span><span class="sxs-lookup"><span data-stu-id="95fae-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="95fae-114">Una canalización de gráficos contiene sombreadores, que realizan cálculos y efectos de representación programables, y operaciones de función fijas.</span><span class="sxs-lookup"><span data-stu-id="95fae-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="95fae-115">Tenga en cuenta lo siguiente al hacer referencia al diagrama de estado de la canalización:</span><span class="sxs-lookup"><span data-stu-id="95fae-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="95fae-116">Las tablas y los montones de descriptores se pueden organizar arbitrariamente: se puede hacer referencia a SRVs, CBVs y UAVs y se pueden asignar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="95fae-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="95fae-117">Algunas operaciones de la canalización son configurables.</span><span class="sxs-lookup"><span data-stu-id="95fae-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="95fae-118">Por ejemplo, la fusión de salida actúa normalmente en una base de lectura-modificación y escritura con las vistas de estarcido de profundidad y de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="95fae-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="95fae-119">Sin embargo, se puede configurar la canalización para que cualquiera de estas vistas sea de solo lectura o de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="95fae-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="95fae-120">Los muestreadores estáticos no forman parte de los argumentos raíz, ya que son estáticos.</span><span class="sxs-lookup"><span data-stu-id="95fae-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="95fae-121">Objetos de estado de canalización</span><span class="sxs-lookup"><span data-stu-id="95fae-121">Pipeline state objects</span></span>

<span data-ttu-id="95fae-122">Direct3D 12 presenta el objeto de estado de canalización (PSO).</span><span class="sxs-lookup"><span data-stu-id="95fae-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="95fae-123">En lugar de almacenar y representar el estado de canalización en un gran número de objetos de alto nivel, los Estados de los componentes de canalización como el ensamblador de entrada, el rasterizador, el sombreador de píxeles y la fusión de salida se almacenan en un PSO.</span><span class="sxs-lookup"><span data-stu-id="95fae-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="95fae-124">Un PSO es un objeto de estado de canalización unificado que es inmutable después de la creación.</span><span class="sxs-lookup"><span data-stu-id="95fae-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="95fae-125">Actualmente se puede cambiar el PSO seleccionado de forma rápida y dinámica, y el hardware y los controladores pueden convertir directamente un PSO en instrucciones y Estados de hardware nativo y preparar la GPU para el procesamiento de gráficos.</span><span class="sxs-lookup"><span data-stu-id="95fae-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="95fae-126">Para aplicar un PSO, el hardware copia una cantidad mínima de estado calculado previamente directamente en los registros de hardware.</span><span class="sxs-lookup"><span data-stu-id="95fae-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="95fae-127">Esto elimina la sobrecarga causada por que el controlador de gráficos recalcule continuamente el estado del hardware en función de todas las opciones de representación y de canalización aplicables actualmente.</span><span class="sxs-lookup"><span data-stu-id="95fae-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="95fae-128">El resultado se reduce significativamente la sobrecarga de la llamada a Draw, el aumento del rendimiento y más llamadas a Draw por fotograma.</span><span class="sxs-lookup"><span data-stu-id="95fae-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="95fae-129">El PSO aplicado actualmente define y conecta todos los sombreadores que se usan en la canalización de representación.</span><span class="sxs-lookup"><span data-stu-id="95fae-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="95fae-130">El [lenguaje HLSL (Microsoft High Level Shader Language)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) se compila previamente en objetos de sombreador que, a continuación, se usan en tiempo de ejecución como entrada para los objetos de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="95fae-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="95fae-131">Para obtener más información sobre cómo funciona el PSO dentro de la canalización de gráficos, vea [administrar el estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="95fae-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="95fae-132">Canalización de proceso de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="95fae-133">En el diagrama siguiente se ilustra el estado y la canalización de proceso de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="95fae-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Diagrama que muestra la canalización de proceso de Direct3D 12.](images/compute-pipeline.png)

<span data-ttu-id="95fae-135">No hay unidades de función fijas en esta canalización; sin embargo, los montones de descriptores, los montones de muestra y los muestreadores estáticos siguen estando disponibles en Compute.</span><span class="sxs-lookup"><span data-stu-id="95fae-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95fae-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95fae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95fae-137">Envío de trabajo en Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="95fae-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 