---
description: Información general sobre la creación de gráficos
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Información general sobre la creación de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152284"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="e85fd-103">Información general sobre la creación de gráficos</span><span class="sxs-lookup"><span data-stu-id="e85fd-103">Overview of Graph Building</span></span>

<span data-ttu-id="e85fd-104">Para crear un gráfico de filtro, empiece por crear una instancia de Filter Graph Manager:</span><span class="sxs-lookup"><span data-stu-id="e85fd-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="e85fd-105">Filter Graph Manager admite los siguientes métodos de creación de gráficos:</span><span class="sxs-lookup"><span data-stu-id="e85fd-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="e85fd-106">[**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) intenta establecer una conexión directa entre dos clavijas.</span><span class="sxs-lookup"><span data-stu-id="e85fd-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="e85fd-107">Si los PIN no se pueden conectar, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="e85fd-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="e85fd-108">[**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta dos clavijas.</span><span class="sxs-lookup"><span data-stu-id="e85fd-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="e85fd-109">Si es posible, realiza una conexión directa.</span><span class="sxs-lookup"><span data-stu-id="e85fd-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="e85fd-110">De lo contrario, utiliza filtros intermedios para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="e85fd-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="e85fd-111">[**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) comienza en un terminal de salida y compila el resto del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="e85fd-112">Estos métodos agregan filtros según sea necesario, trabajando de forma descendente hasta que alcanzan un filtro de representador.</span><span class="sxs-lookup"><span data-stu-id="e85fd-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="e85fd-113">[**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de reproducción de archivos completo.</span><span class="sxs-lookup"><span data-stu-id="e85fd-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="e85fd-114">[**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) agrega un filtro al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="e85fd-115">No conecta el filtro.</span><span class="sxs-lookup"><span data-stu-id="e85fd-115">It does not connect the filter.</span></span> <span data-ttu-id="e85fd-116">Debe crear el filtro antes de llamar a este método, ya sea mediante una llamada a **CoCreateInstance** o mediante el enumerador de filtros o de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="e85fd-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="e85fd-117">Estos métodos proporcionan tres enfoques básicos para crear el gráfico:</span><span class="sxs-lookup"><span data-stu-id="e85fd-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="e85fd-118">El administrador de gráficos de filtro compila todo el gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="e85fd-119">El administrador de gráficos de filtro compila parte del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="e85fd-120">La aplicación crea el gráfico completo.</span><span class="sxs-lookup"><span data-stu-id="e85fd-120">The application builds the entire graph.</span></span>

<span data-ttu-id="e85fd-121">**El administrador de gráficos de filtro compila todo el gráfico**</span><span class="sxs-lookup"><span data-stu-id="e85fd-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="e85fd-122">Si simplemente desea reproducir un archivo que se creó en un formato reconocido, como AVI, MPEG, WAV o MP3, use el método **RenderFile** .</span><span class="sxs-lookup"><span data-stu-id="e85fd-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="e85fd-123">En el artículo [Cómo reproducir un archivo](how-to-play-a-file.md) se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e85fd-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="e85fd-124">El método **RenderFile** se inicia buscando en el registro un filtro de origen que puede analizar el archivo.</span><span class="sxs-lookup"><span data-stu-id="e85fd-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="e85fd-125">Usa el protocolo (como " `https://` " en la dirección URL), la extensión de archivo o los patrones de bytes predefinidos en el archivo para determinar el filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="e85fd-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="e85fd-126">Para obtener más información, consulte [registrar un tipo de archivo personalizado](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="e85fd-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="e85fd-127">Para compilar el resto del gráfico, el administrador de gráficos de filtro utiliza un proceso iterativo en el que toma los tipos de medios que admite un filtro en sus clavijas de salida y busca en el registro filtros que acepten ese tipo de medio como entrada.</span><span class="sxs-lookup"><span data-stu-id="e85fd-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="e85fd-128">Usa varios criterios para restringir los filtros de búsqueda y priorización:</span><span class="sxs-lookup"><span data-stu-id="e85fd-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="e85fd-129">La *categoría de filtro* identifica la funcionalidad general del filtro.</span><span class="sxs-lookup"><span data-stu-id="e85fd-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="e85fd-130">El tipo de medio describe el tipo de datos que el filtro puede aceptar como entrada o entrega como salida.</span><span class="sxs-lookup"><span data-stu-id="e85fd-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="e85fd-131">El *mérito* determina el orden en el que se intentan los filtros.</span><span class="sxs-lookup"><span data-stu-id="e85fd-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="e85fd-132">Si dos filtros de la misma categoría de filtro admiten los mismos tipos de entrada, el administrador de gráficos de filtro selecciona el que tiene el valor de mérito más alto.</span><span class="sxs-lookup"><span data-stu-id="e85fd-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="e85fd-133">A algunos filtros se les asigna intencionadamente un valor de mérito bajo porque están diseñados para fines especializados y la aplicación solo debe agregarlos al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="e85fd-134">Filter Graph Manager usa el objeto de [asignador de filtros](filter-mapper.md) para buscar en el registro.</span><span class="sxs-lookup"><span data-stu-id="e85fd-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="e85fd-135">A medida que se agrega cada filtro, el administrador de gráficos de filtros intenta conectarlo al código PIN de salida del filtro anterior.</span><span class="sxs-lookup"><span data-stu-id="e85fd-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="e85fd-136">Los filtros negocian para determinar si se pueden conectar y, si es así, el tipo de medio que se utilizará para la conexión.</span><span class="sxs-lookup"><span data-stu-id="e85fd-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="e85fd-137">Si el nuevo filtro no se puede conectar, el administrador de gráficos de filtros lo descarta e intenta otro filtro.</span><span class="sxs-lookup"><span data-stu-id="e85fd-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="e85fd-138">Este proceso continúa hasta que se representan todos los flujos.</span><span class="sxs-lookup"><span data-stu-id="e85fd-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="e85fd-139">**El administrador de gráficos de filtro compila parte del gráfico**</span><span class="sxs-lookup"><span data-stu-id="e85fd-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="e85fd-140">Para hacer algo más allá de simplemente reproducir un archivo, la aplicación debe realizar al menos algunos de los trabajos de creación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e85fd-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="e85fd-141">Por ejemplo, una aplicación de captura de vídeo debe seleccionar un filtro de origen de captura y agregarlo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="e85fd-142">Si va a escribir datos en un archivo AVI, debe agregar los filtros AVI MUX y escritor de archivos al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="e85fd-143">Sin embargo, a menudo es posible permitir que el administrador de gráficos de filtro complete el gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="e85fd-144">Por ejemplo, puede representar un PIN para la vista previa llamando al método **Render** .</span><span class="sxs-lookup"><span data-stu-id="e85fd-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="e85fd-145">**La aplicación crea el gráfico completo**</span><span class="sxs-lookup"><span data-stu-id="e85fd-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="e85fd-146">En algunos escenarios, es posible que la aplicación necesite crear el gráfico agregando y conectando cada filtro.</span><span class="sxs-lookup"><span data-stu-id="e85fd-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="e85fd-147">En este caso, probablemente sepa específicamente qué filtros se deben agregar al gráfico.</span><span class="sxs-lookup"><span data-stu-id="e85fd-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="e85fd-148">Con este enfoque, la aplicación agrega cada filtro llamando a **addFilter**, enumera los pin de los filtros y los conecta llamando a **Connect** o **ConnectDirect**.</span><span class="sxs-lookup"><span data-stu-id="e85fd-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e85fd-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e85fd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e85fd-150">Generar gráficos con el generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="e85fd-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="e85fd-151">Enumerar dispositivos y filtros</span><span class="sxs-lookup"><span data-stu-id="e85fd-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="e85fd-152">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="e85fd-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="e85fd-153">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="e85fd-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="e85fd-154">Compilar el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="e85fd-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



