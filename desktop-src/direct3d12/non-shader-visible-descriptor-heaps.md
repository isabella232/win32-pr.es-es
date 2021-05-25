---
title: Montones de descriptores no visibles por el sombreador
description: Los sombreadores no pueden hacer referencia a algunos montones de descriptores a través de tablas de descriptores, pero existen para ayudar a la aplicación a almacenamiento provisional de los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343460"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="fb72e-103">Montones de descriptores no visibles por el sombreador</span><span class="sxs-lookup"><span data-stu-id="fb72e-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="fb72e-104">Los sombreadores no pueden hacer referencia a algunos montones de descriptores a través de tablas de descriptores, pero existen para ayudar a la aplicación a almacenamiento provisional de los descriptores antes de grabar una lista de comandos o porque no se requiere ningún montón visible del sombreador.</span><span class="sxs-lookup"><span data-stu-id="fb72e-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="fb72e-105">Vistas no visibles</span><span class="sxs-lookup"><span data-stu-id="fb72e-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="fb72e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="fb72e-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="fb72e-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb72e-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="fb72e-108">Vistas no visibles</span><span class="sxs-lookup"><span data-stu-id="fb72e-108">Non-visible views</span></span>

<span data-ttu-id="fb72e-109">Todos los montones de descriptores, incluidos los montones de descriptores accesibles del sombreador descritos anteriormente, se pueden manipular mediante la CPU o las listas de comandos en función del grupo de memoria y las propiedades de acceso a la CPU que la aplicación seleccione para un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="fb72e-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="fb72e-110">En el caso de los [montones de descriptores visibles del](shader-visible-descriptor-heaps.md)sombreador, la razón obvia para denegar el acceso del sombreador a estos montones de descriptores es mientras se están montados.</span><span class="sxs-lookup"><span data-stu-id="fb72e-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="fb72e-111">A continuación, estos montones se hacen visibles para el sombreador y se accede a ellos a través de tablas de descriptores en la ejecución de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="fb72e-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="fb72e-112">Sin embargo, no hay ningún requisito para la fase de los montones visibles del sombreador, ya que se pueden rellenar directamente.</span><span class="sxs-lookup"><span data-stu-id="fb72e-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="fb72e-113">Otros descriptores se enlazan a la canalización haciendo que su contenido se grabe directamente en la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="fb72e-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="fb72e-114">Estos descriptores solo sirven para traducir los parámetros de vista en el tiempo de registro de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="fb72e-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="fb72e-115">Estos montones siempre son visibles sin sombreador y contienen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="fb72e-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="fb72e-116">Representar vistas de destino (RTV)</span><span class="sxs-lookup"><span data-stu-id="fb72e-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="fb72e-117">Vistas de galería de símbolos de profundidad (DSV)</span><span class="sxs-lookup"><span data-stu-id="fb72e-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="fb72e-118">Las vistas de búfer de índice (IBV), las vistas de búfer de vértice (VBV) y las vistas de salida de flujo (SOV) se pasan directamente a los métodos de API, no tienen tipos de montón específicos.</span><span class="sxs-lookup"><span data-stu-id="fb72e-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="fb72e-119">Después de grabar en la lista de comandos (con una llamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por ejemplo), la memoria usada para contener los descriptores de esta llamada está disponible inmediatamente para volver a usarse después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="fb72e-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="fb72e-120">Incluso las tablas de descriptores tienen opciones en las que una aplicación puede permitir que la implementación elija registrar el contenido de la tabla en la grabación de la lista de comandos (en lugar de desreferenciar el puntero de tabla en la ejecución).</span><span class="sxs-lookup"><span data-stu-id="fb72e-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="fb72e-121">Resumen</span><span class="sxs-lookup"><span data-stu-id="fb72e-121">Summary</span></span>



|                   | <span data-ttu-id="fb72e-122">Sombreador visible, solo escritura de CPU</span><span class="sxs-lookup"><span data-stu-id="fb72e-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="fb72e-123">No visible el sombreador, lectura y escritura de CPU</span><span class="sxs-lookup"><span data-stu-id="fb72e-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="fb72e-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="fb72e-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="fb72e-125">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-125">yes</span></span>                                | <span data-ttu-id="fb72e-126">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-126">yes</span></span>                                    |
| <span data-ttu-id="fb72e-127">**Sampler**</span><span class="sxs-lookup"><span data-stu-id="fb72e-127">**SAMPLER**</span></span>       | <span data-ttu-id="fb72e-128">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-128">yes</span></span>                                | <span data-ttu-id="fb72e-129">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-129">yes</span></span>                                    |
| <span data-ttu-id="fb72e-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="fb72e-130">**RTV**</span></span>           | <span data-ttu-id="fb72e-131">No</span><span class="sxs-lookup"><span data-stu-id="fb72e-131">no</span></span>                                 | <span data-ttu-id="fb72e-132">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-132">yes</span></span>                                    |
| <span data-ttu-id="fb72e-133">**Dsv**</span><span class="sxs-lookup"><span data-stu-id="fb72e-133">**DSV**</span></span>           | <span data-ttu-id="fb72e-134">No</span><span class="sxs-lookup"><span data-stu-id="fb72e-134">no</span></span>                                 | <span data-ttu-id="fb72e-135">sí</span><span class="sxs-lookup"><span data-stu-id="fb72e-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="fb72e-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb72e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb72e-137">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="fb72e-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




