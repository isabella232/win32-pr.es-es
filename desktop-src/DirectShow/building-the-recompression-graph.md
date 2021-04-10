---
description: Compilar el gráfico de recompresión
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Compilar el gráfico de recompresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906385"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="a47da-103">Compilar el gráfico de recompresión</span><span class="sxs-lookup"><span data-stu-id="a47da-103">Building the Recompression Graph</span></span>

<span data-ttu-id="a47da-104">Un gráfico de filtro típico para la recompresión de archivos AVI tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="a47da-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![gráfico de recompresión de AVI](images/avi2avi4.png)

<span data-ttu-id="a47da-106">El [filtro de divisor de AVI](avi-splitter-filter.md) extrae datos del [filtro de origen de archivos (Async)](file-source--async--filter.md) y los analiza en secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="a47da-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="a47da-107">El descompresor de vídeo descodifica el vídeo comprimido, donde se vuelve a comprimir con el compresor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a47da-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="a47da-108">La elección de descompresores depende del archivo de código fuente; se controlará automáticamente mediante la [conexión inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="a47da-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="a47da-109">La aplicación debe elegir el compresor, normalmente presentando una lista al usuario.</span><span class="sxs-lookup"><span data-stu-id="a47da-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="a47da-110">(Vea [elegir un filtro de compresión](choosing-a-compression-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="a47da-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="a47da-111">Después, el vídeo comprimido se dirige al [filtro de AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a47da-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="a47da-112">La secuencia de audio de este ejemplo no está comprimida, por lo que va directamente desde el divisor de AVI a AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="a47da-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="a47da-113">El MUX de AVI entrelaza las dos secuencias y el filtro de [escritura de archivos](file-writer-filter.md) escribe la salida en el disco.</span><span class="sxs-lookup"><span data-stu-id="a47da-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="a47da-114">Tenga en cuenta que se requiere AVI MUX incluso si el archivo original no tiene una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="a47da-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="a47da-115">La manera más sencilla de generar este gráfico de filtro es usar el [generador de gráficos de captura](capture-graph-builder.md), que es un componente de DirectShow para crear gráficos de captura y otros gráficos de filtros personalizados.</span><span class="sxs-lookup"><span data-stu-id="a47da-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="a47da-116">Empiece por llamar a CoCreateInstance para crear el generador de gráficos de captura:</span><span class="sxs-lookup"><span data-stu-id="a47da-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="a47da-117">A continuación, use el generador de gráficos de captura para compilar el gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="a47da-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="a47da-118">Cree la sección de representación del gráfico, que incluye el filtro de AVI y el [escritor de archivos](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a47da-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="a47da-119">Agregue el filtro de origen y el filtro de compresión al gráfico.</span><span class="sxs-lookup"><span data-stu-id="a47da-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="a47da-120">Conecte el filtro de origen al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a47da-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="a47da-121">El generador de gráficos de captura inserta cualquier filtro de divisor y descodificador que se necesite para analizar el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a47da-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="a47da-122">También puede enrutar las secuencias de audio y vídeo a través de filtros de compresión.</span><span class="sxs-lookup"><span data-stu-id="a47da-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="a47da-123">En las secciones siguientes se explica cada uno de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="a47da-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="a47da-124">Crear la sección de representación</span><span class="sxs-lookup"><span data-stu-id="a47da-124">Build the Rendering Section</span></span>

<span data-ttu-id="a47da-125">Para compilar la sección de representación del gráfico, llame al método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) .</span><span class="sxs-lookup"><span data-stu-id="a47da-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="a47da-126">Este método toma parámetros de entrada que especifican el subtipo de medios para la salida y el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="a47da-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="a47da-127">Devuelve punteros al filtro MUX y al escritor de archivos.</span><span class="sxs-lookup"><span data-stu-id="a47da-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="a47da-128">El filtro MUX es necesario para la siguiente fase de creación del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a47da-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="a47da-129">El puntero al escritor de archivos no es necesario en este ejemplo, de modo que el parámetro puede ser **null**:</span><span class="sxs-lookup"><span data-stu-id="a47da-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="a47da-130">Cuando el método devuelve, el filtro MUX tiene un recuento de referencias pendiente, de modo que asegúrese de liberar el puntero más adelante.</span><span class="sxs-lookup"><span data-stu-id="a47da-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="a47da-131">En el diagrama siguiente se muestra el gráfico de filtro en este punto.</span><span class="sxs-lookup"><span data-stu-id="a47da-131">The following diagram shows the filter graph at this point.</span></span>

![sección de representación del gráfico de filtros](images/avi2avi1.png)

<span data-ttu-id="a47da-133">El filtro MUX expone dos interfaces para controlar el formato AVI:</span><span class="sxs-lookup"><span data-stu-id="a47da-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="a47da-134">[**Interfaz IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): establece el modo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="a47da-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="a47da-135">[**Interfaz IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): establece la secuencia maestra y el índice de compatibilidad AVI.</span><span class="sxs-lookup"><span data-stu-id="a47da-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="a47da-136">Agregar los filtros de origen y compresión</span><span class="sxs-lookup"><span data-stu-id="a47da-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="a47da-137">El siguiente paso consiste en agregar los filtros de origen y de compresión al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="a47da-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="a47da-138">El generador de gráficos de captura crea automáticamente una instancia del administrador de gráficos de filtro cuando se llama a SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="a47da-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="a47da-139">Obtenga un puntero a él llamando al método [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :</span><span class="sxs-lookup"><span data-stu-id="a47da-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="a47da-140">Ahora llame al método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar el filtro de origen de archivo asincrónico y el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el compresor de vídeo:</span><span class="sxs-lookup"><span data-stu-id="a47da-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="a47da-141">En este momento, el filtro de origen y el filtro de compresión no están conectados a ningún otro elemento del gráfico, tal como se muestra en la siguiente ilustración:</span><span class="sxs-lookup"><span data-stu-id="a47da-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![filtrar gráfico con filtros de origen y compresión](images/avi2avi2.png)

<span data-ttu-id="a47da-143">Conexión del origen con el MUX</span><span class="sxs-lookup"><span data-stu-id="a47da-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="a47da-144">El paso final consiste en conectar el filtro de origen al filtro de AVI, a través del compresor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a47da-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="a47da-145">Use el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , que conecta un PIN de salida en el filtro de origen con un filtro de receptor especificado, opcionalmente a través de un filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="a47da-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="a47da-146">Los dos primeros parámetros especifican cuál de los PIN del filtro de origen se conectan, mediante la designación de una categoría de PIN y un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a47da-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="a47da-147">El filtro de origen de archivo Async solo tiene un PIN de salida, por lo que estos parámetros deben ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a47da-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="a47da-148">Los tres parámetros siguientes especifican el filtro de origen, el filtro de compresión (si existe) y el filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="a47da-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="a47da-149">En el ejemplo de código siguiente se representa la secuencia de vídeo a través del compresor de vídeo:</span><span class="sxs-lookup"><span data-stu-id="a47da-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="a47da-150">En el diagrama siguiente se muestra el gráfico de filtro hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="a47da-150">The following diagram shows the filter graph so far.</span></span>

![secuencia de vídeo representada](images/avi2avi3.png)

<span data-ttu-id="a47da-152">Suponiendo que el archivo de origen tiene una secuencia de audio, el filtro de [divisor de AVI](avi-splitter-filter.md) ha creado un PIN de salida para el audio.</span><span class="sxs-lookup"><span data-stu-id="a47da-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="a47da-153">Para conectar este pin, vuelva a llamar a RenderStream:</span><span class="sxs-lookup"><span data-stu-id="a47da-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="a47da-154">Aquí no se especifica ningún filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="a47da-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="a47da-155">El PIN de salida del filtro de origen ya está conectado, por lo que el método RenderStream busca un PIN de salida no conectado en el filtro divisor.</span><span class="sxs-lookup"><span data-stu-id="a47da-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="a47da-156">Busca el PIN de audio y lo conecta directamente al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="a47da-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="a47da-157">Si el archivo de origen no tiene una secuencia de audio, se producirá un error en la segunda llamada a RenderStream.</span><span class="sxs-lookup"><span data-stu-id="a47da-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="a47da-158">Este es el comportamiento esperado.</span><span class="sxs-lookup"><span data-stu-id="a47da-158">This is expected behavior.</span></span> <span data-ttu-id="a47da-159">El gráfico se completa después de la primera llamada a RenderStream, por lo que el error en la segunda llamada es inofensivo.</span><span class="sxs-lookup"><span data-stu-id="a47da-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="a47da-160">En este ejemplo, es importante el orden de las dos llamadas a RenderStream.</span><span class="sxs-lookup"><span data-stu-id="a47da-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="a47da-161">Dado que la segunda llamada no especifica un compresor, conectará cualquier PIN no conectado desde el divisor de AVI.</span><span class="sxs-lookup"><span data-stu-id="a47da-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="a47da-162">Si realiza esta llamada antes de la otra, podría conectar la secuencia de vídeo a AVI MUX sin su compresor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a47da-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="a47da-163">Por lo tanto, la llamada más específica (con el filtro de compresión) debe aparecer en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="a47da-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="a47da-164">En la explicación anterior se supone que el archivo de código fuente es un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="a47da-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="a47da-165">Sin embargo, esta técnica también funciona con otros tipos de archivo, como los archivos MPEG.</span><span class="sxs-lookup"><span data-stu-id="a47da-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="a47da-166">El gráfico de filtros resultante será algo diferente.</span><span class="sxs-lookup"><span data-stu-id="a47da-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a47da-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a47da-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a47da-168">Volver a comprimir un archivo AVI</span><span class="sxs-lookup"><span data-stu-id="a47da-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



