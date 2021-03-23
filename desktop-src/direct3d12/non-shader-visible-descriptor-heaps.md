---
title: Montones de descriptor visibles sin sombreador
description: Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104549097"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="59078-103">Montones de descriptor visibles sin sombreador</span><span class="sxs-lookup"><span data-stu-id="59078-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="59078-104">Los sombreadores no pueden hacer referencia a algunos montones de descriptor a través de tablas de descriptores, pero existen para ayudar a la aplicación a ensayar los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.</span><span class="sxs-lookup"><span data-stu-id="59078-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="59078-105">Vistas no visibles</span><span class="sxs-lookup"><span data-stu-id="59078-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="59078-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="59078-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="59078-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59078-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="59078-108">Vistas no visibles</span><span class="sxs-lookup"><span data-stu-id="59078-108">Non-visible views</span></span>

<span data-ttu-id="59078-109">Todos los montones de descriptor, incluidos los montones de descriptor accesible del sombreador descritos anteriormente, se pueden manipular mediante las listas de comandos y de CPU en función de las propiedades del bloque de memoria y el acceso a la CPU que la aplicación selecciona para un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="59078-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="59078-110">En el caso de los [montones de descriptor visibles del sombreador](shader-visible-descriptor-heaps.md), el motivo obvio para denegar el acceso del sombreador a estos montones descriptores es mientras se almacenan provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="59078-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="59078-111">Después, estos montones se hacen visibles para el sombreador y se obtiene acceso a ellos a través de las tablas de descriptor en la ejecución de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="59078-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="59078-112">Sin embargo, no hay ningún requisito para almacenar en fases los montones visibles del sombreador, sino que se pueden rellenar directamente.</span><span class="sxs-lookup"><span data-stu-id="59078-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="59078-113">Otros descriptores se enlazan a la canalización haciendo que su contenido se grabe directamente en la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="59078-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="59078-114">Estos descriptores solo sirven para traducir los parámetros de la vista en la hora del registro de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="59078-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="59078-115">Estos montones siempre son visibles sin sombreador y contienen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="59078-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="59078-116">Vistas de destino de representación (RTVs)</span><span class="sxs-lookup"><span data-stu-id="59078-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="59078-117">Vistas de estarcido de profundidad (DSV)</span><span class="sxs-lookup"><span data-stu-id="59078-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="59078-118">Las vistas de búfer de índice (IBVs), las vistas de búfer de vértices (VBVs) y las vistas de salida de secuencias (SOVs) se pasan directamente a los métodos de la API, no tienen tipos de montón concretos.</span><span class="sxs-lookup"><span data-stu-id="59078-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="59078-119">Después de grabar en la lista de comandos (con una llamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por ejemplo) la memoria usada para contener los descriptores de esta llamada está disponible inmediatamente para su reutilización después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="59078-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="59078-120">Incluso las tablas de descriptores tienen opciones donde una aplicación puede permitir que la implementación elija registrar el contenido de la tabla en la grabación de la lista de comandos (en lugar de desreferenciar el puntero de tabla en ejecución).</span><span class="sxs-lookup"><span data-stu-id="59078-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="59078-121">Resumen</span><span class="sxs-lookup"><span data-stu-id="59078-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="59078-122">**sombreador visible, solo escritura de CPU**</span><span class="sxs-lookup"><span data-stu-id="59078-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="59078-123">**sin sombreador visible, lectura de CPU/escritura**</span><span class="sxs-lookup"><span data-stu-id="59078-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="59078-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="59078-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="59078-125">sí</span><span class="sxs-lookup"><span data-stu-id="59078-125">yes</span></span>                                | <span data-ttu-id="59078-126">sí</span><span class="sxs-lookup"><span data-stu-id="59078-126">yes</span></span>                                    |
| <span data-ttu-id="59078-127">**MUESTRAS**</span><span class="sxs-lookup"><span data-stu-id="59078-127">**SAMPLER**</span></span>       | <span data-ttu-id="59078-128">sí</span><span class="sxs-lookup"><span data-stu-id="59078-128">yes</span></span>                                | <span data-ttu-id="59078-129">sí</span><span class="sxs-lookup"><span data-stu-id="59078-129">yes</span></span>                                    |
| <span data-ttu-id="59078-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="59078-130">**RTV**</span></span>           | <span data-ttu-id="59078-131">no</span><span class="sxs-lookup"><span data-stu-id="59078-131">no</span></span>                                 | <span data-ttu-id="59078-132">sí</span><span class="sxs-lookup"><span data-stu-id="59078-132">yes</span></span>                                    |
| <span data-ttu-id="59078-133">**VISTA**</span><span class="sxs-lookup"><span data-stu-id="59078-133">**DSV**</span></span>           | <span data-ttu-id="59078-134">no</span><span class="sxs-lookup"><span data-stu-id="59078-134">no</span></span>                                 | <span data-ttu-id="59078-135">sí</span><span class="sxs-lookup"><span data-stu-id="59078-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="59078-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59078-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59078-137">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="59078-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




