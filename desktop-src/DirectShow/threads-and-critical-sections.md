---
description: Subprocesos y secciones críticas
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Subprocesos y secciones críticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361666"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="e8c16-103">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="e8c16-103">Threads and Critical Sections</span></span>

<span data-ttu-id="e8c16-104">En esta sección se describen los subprocesos de los filtros de DirectShow y los pasos que debe seguir para evitar bloqueos o interbloqueos en un filtro personalizado.</span><span class="sxs-lookup"><span data-stu-id="e8c16-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="e8c16-105">En los ejemplos de esta sección se usa pseudocódigo para ilustrar el código que se debe escribir.</span><span class="sxs-lookup"><span data-stu-id="e8c16-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="e8c16-106">Suponen que un filtro personalizado usa clases derivadas de las clases base de DirectShow, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e8c16-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="e8c16-107">CMyInputPin: se deriva de [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="e8c16-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="e8c16-108">CMyOutputPin: se deriva de [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="e8c16-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="e8c16-109">CMyFilter: se deriva de [**CBaseFilter**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="e8c16-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="e8c16-110">CMyInputAllocator: asignador del PIN de entrada, derivado de [**CMemAllocator**](cmemallocator.md).</span><span class="sxs-lookup"><span data-stu-id="e8c16-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="e8c16-111">No todos los filtros necesitan un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="e8c16-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="e8c16-112">Para muchos filtros, la clase **CMemAllocator** es suficiente.</span><span class="sxs-lookup"><span data-stu-id="e8c16-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="e8c16-113">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e8c16-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="e8c16-114">Los subprocesos streaming y Application</span><span class="sxs-lookup"><span data-stu-id="e8c16-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="e8c16-115">Pausando</span><span class="sxs-lookup"><span data-stu-id="e8c16-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="e8c16-116">Recibir y entregar ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8c16-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="e8c16-117">Entrega del final de la secuencia</span><span class="sxs-lookup"><span data-stu-id="e8c16-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="e8c16-118">Vaciar datos</span><span class="sxs-lookup"><span data-stu-id="e8c16-118">Flushing Data</span></span>](flushing-data.md)
-   <span data-ttu-id="e8c16-119">[Stopping](stopping.md) (Deteniéndose)</span><span class="sxs-lookup"><span data-stu-id="e8c16-119">[Stopping](stopping.md)</span></span>
-   [<span data-ttu-id="e8c16-120">Obtener búferes</span><span class="sxs-lookup"><span data-stu-id="e8c16-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="e8c16-121">Streaming de subprocesos y Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="e8c16-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="e8c16-122">Resumen de subprocesos de filtro</span><span class="sxs-lookup"><span data-stu-id="e8c16-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="e8c16-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8c16-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8c16-124">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="e8c16-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="e8c16-125">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8c16-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



