---
description: Acerca de los ejemplos y asignadores de medios
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Acerca de los ejemplos y asignadores de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689623"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="53387-103">Acerca de los ejemplos y asignadores de medios</span><span class="sxs-lookup"><span data-stu-id="53387-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="53387-104">Los filtros entregan datos a través de conexiones de PIN.</span><span class="sxs-lookup"><span data-stu-id="53387-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="53387-105">Los datos se mueven desde el terminal de salida de un filtro hasta el PIN de entrada de otro filtro.</span><span class="sxs-lookup"><span data-stu-id="53387-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="53387-106">La forma más común de que el PIN de salida entregue los datos es mediante una llamada al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) en la entrada, aunque también existen algunos mecanismos.</span><span class="sxs-lookup"><span data-stu-id="53387-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="53387-107">Dependiendo del filtro, la memoria de los datos multimedia se puede asignar de varias maneras: en el montón, en una superficie de DirectDraw, utilizando la memoria de GDI compartida o usando algún otro mecanismo de asignación.</span><span class="sxs-lookup"><span data-stu-id="53387-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="53387-108">El objeto responsable de la asignación de la memoria se denomina *allocator*, que es un objeto com que expone la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="53387-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="53387-109">Cuando dos patillas se conectan, uno de los pin debe proporcionar un asignador.</span><span class="sxs-lookup"><span data-stu-id="53387-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="53387-110">DirectShow define una secuencia de llamadas de método que se usa para establecer qué PIN proporciona el asignador.</span><span class="sxs-lookup"><span data-stu-id="53387-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="53387-111">Los pin también aceptan el número de búferes que va a crear el asignador y el tamaño de los búferes.</span><span class="sxs-lookup"><span data-stu-id="53387-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="53387-112">Antes de que comience el streaming, el asignador crea un grupo de búferes.</span><span class="sxs-lookup"><span data-stu-id="53387-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="53387-113">Durante el streaming, el filtro de nivel superior rellena los búferes con datos y los entrega al filtro de bajada.</span><span class="sxs-lookup"><span data-stu-id="53387-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="53387-114">Pero el filtro de nivel superior no proporciona los punteros sin formato de filtro de bajada a los búferes.</span><span class="sxs-lookup"><span data-stu-id="53387-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="53387-115">En su lugar, utiliza objetos COM denominados *ejemplos de medios*, que el asignador crea para administrar los búferes.</span><span class="sxs-lookup"><span data-stu-id="53387-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="53387-116">Los ejemplos de medios exponen la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="53387-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="53387-117">Un ejemplo multimedia contiene:</span><span class="sxs-lookup"><span data-stu-id="53387-117">A media sample contains:</span></span>

-   <span data-ttu-id="53387-118">puntero al búfer subyacente.</span><span class="sxs-lookup"><span data-stu-id="53387-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="53387-119">una marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="53387-119">a time stamp</span></span>
-   <span data-ttu-id="53387-120">varias marcas</span><span class="sxs-lookup"><span data-stu-id="53387-120">various flags</span></span>
-   <span data-ttu-id="53387-121">Opcionalmente, un tipo de medio</span><span class="sxs-lookup"><span data-stu-id="53387-121">optionally, a media type</span></span>

<span data-ttu-id="53387-122">La marca de tiempo define el tiempo de presentación, que el filtro de representador utiliza para programar la representación.</span><span class="sxs-lookup"><span data-stu-id="53387-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="53387-123">Las marcas indican aspectos como si hubiera una interrupción en los datos desde el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="53387-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="53387-124">El tipo de medio proporciona una manera de que los filtros cambien los formatos a la secuencia intermedia.</span><span class="sxs-lookup"><span data-stu-id="53387-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="53387-125">Normalmente, el ejemplo no tiene ningún tipo de medio, lo que indica que el formato no ha cambiado desde el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="53387-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="53387-126">Mientras un filtro está utilizando un búfer, contiene el recuento de referencias en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="53387-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="53387-127">El asignador utiliza el recuento de referencias para determinar cuándo puede volver a usar el búfer.</span><span class="sxs-lookup"><span data-stu-id="53387-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="53387-128">Esto evita que un filtro sobrescriba un búfer que sigue usando otro filtro.</span><span class="sxs-lookup"><span data-stu-id="53387-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="53387-129">Un ejemplo no vuelve al grupo del asignador de muestras disponibles hasta que todos los filtros lo han liberado.</span><span class="sxs-lookup"><span data-stu-id="53387-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="53387-130">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="53387-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="53387-131">En el tema [ejemplos y asignadores](samples-and-allocators.md) se proporciona una descripción más detallada de cómo funcionan los asignadores.</span><span class="sxs-lookup"><span data-stu-id="53387-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="53387-132">El [flujo de datos del tema en el gráfico de filtros](data-flow-in-the-filter-graph.md) proporciona una introducción general del flujo de datos en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="53387-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="53387-133">Los temas siguientes están destinados a los desarrolladores que escriben sus propios filtros personalizados:</span><span class="sxs-lookup"><span data-stu-id="53387-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="53387-134">Flujo de datos para desarrolladores de filtros</span><span class="sxs-lookup"><span data-stu-id="53387-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="53387-135">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="53387-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="53387-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53387-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53387-137">El gráfico de filtro y sus componentes</span><span class="sxs-lookup"><span data-stu-id="53387-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



