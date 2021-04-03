---
description: Generar gráficos con el generador de gráficos de captura
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Generar gráficos con el generador de gráficos de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906822"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="dacc4-103">Generar gráficos con el generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="dacc4-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="dacc4-104">A pesar de su nombre, el generador de gráficos de captura es útil para crear muchos tipos de gráficos de filtros personalizados, no solo para capturar gráficos.</span><span class="sxs-lookup"><span data-stu-id="dacc4-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="dacc4-105">En este artículo se proporciona una breve descripción de cómo utilizar este objeto.</span><span class="sxs-lookup"><span data-stu-id="dacc4-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="dacc4-106">El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="dacc4-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="dacc4-107">Empiece por llamar a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el generador de gráficos de captura y el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="dacc4-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="dacc4-108">A continuación, inicialice el generador de gráficos de captura mediante una llamada a [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero al administrador de gráficos de filtro, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="dacc4-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="dacc4-109">Conexión de filtros</span><span class="sxs-lookup"><span data-stu-id="dacc4-109">Connecting Filters</span></span>

<span data-ttu-id="dacc4-110">El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conecta dos o tres filtros juntos en una cadena.</span><span class="sxs-lookup"><span data-stu-id="dacc4-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="dacc4-111">Por lo general, el método funciona mejor cuando cada filtro no tiene más de un PIN de entrada o de salida del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="dacc4-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="dacc4-112">Este debate comienza omitiendo los dos primeros parámetros de **RenderStream** y centrándose en los tres últimos parámetros.</span><span class="sxs-lookup"><span data-stu-id="dacc4-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="dacc4-113">El tercer parámetro es un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que puede especificar un filtro (como un puntero de interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ) o un PIN de salida (como un puntero de interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) ).</span><span class="sxs-lookup"><span data-stu-id="dacc4-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="dacc4-114">Los parámetros cuarto y quinto especifican punteros **IBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="dacc4-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="dacc4-115">El método **RenderStream** conecta los tres filtros de una cadena.</span><span class="sxs-lookup"><span data-stu-id="dacc4-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="dacc4-116">Por ejemplo, suponga que *A*, *B* y *C* son filtros.</span><span class="sxs-lookup"><span data-stu-id="dacc4-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="dacc4-117">Supongamos por ahora que cada filtro tiene exactamente un PIN de entrada y uno de salida.</span><span class="sxs-lookup"><span data-stu-id="dacc4-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="dacc4-118">La siguiente llamada conecta a a B y, a continuación, B a C:</span><span class="sxs-lookup"><span data-stu-id="dacc4-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="dacc4-119">Todas las conexiones son "inteligentes", lo que significa que los filtros adicionales se agregan al gráfico según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dacc4-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="dacc4-120">Para obtener más información, consulte [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="dacc4-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="dacc4-121">Para conectar solo dos filtros, establezca el valor intermedio en **null**.</span><span class="sxs-lookup"><span data-stu-id="dacc4-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="dacc4-122">Por ejemplo, esta llamada conecta a a C:</span><span class="sxs-lookup"><span data-stu-id="dacc4-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="dacc4-123">Puede crear cadenas más largas llamando al método dos veces:</span><span class="sxs-lookup"><span data-stu-id="dacc4-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="dacc4-124">Si el último parámetro es **null**, el método busca automáticamente un representador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dacc4-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="dacc4-125">Usa el [representador de vídeo](video-renderer-filter.md) para vídeo y el [representador de DirectSound](directsound-renderer-filter.md) para audio.</span><span class="sxs-lookup"><span data-stu-id="dacc4-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="dacc4-126">Modo</span><span class="sxs-lookup"><span data-stu-id="dacc4-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="dacc4-127">es equivalente a</span><span class="sxs-lookup"><span data-stu-id="dacc4-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="dacc4-128">donde *R* es el representador adecuado.</span><span class="sxs-lookup"><span data-stu-id="dacc4-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="dacc4-129">Sin embargo, para conectar el filtro de representador de mezcla de vídeo en lugar del representador de vídeo, debe especificarlo explícitamente.</span><span class="sxs-lookup"><span data-stu-id="dacc4-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="dacc4-130">Si especifica un filtro en el tercer parámetro, en lugar de un PIN, es posible que deba indicar qué PIN de salida se debe usar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="dacc4-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="dacc4-131">Este es el propósito de los dos primeros parámetros del método.</span><span class="sxs-lookup"><span data-stu-id="dacc4-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="dacc4-132">El primer parámetro solo se aplica a los filtros de captura.</span><span class="sxs-lookup"><span data-stu-id="dacc4-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="dacc4-133">Especifica un GUID que indica una categoría de PIN.</span><span class="sxs-lookup"><span data-stu-id="dacc4-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="dacc4-134">Para obtener una lista completa de las categorías, vea [conjunto de propiedades del PIN](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="dacc4-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="dacc4-135">Dos de las categorías son válidas para todos los filtros de captura:</span><span class="sxs-lookup"><span data-stu-id="dacc4-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="dacc4-136">**\_captura de categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="dacc4-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="dacc4-137">**\_vista previa de categoría de PIN \_**</span><span class="sxs-lookup"><span data-stu-id="dacc4-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="dacc4-138">Si un filtro de captura no proporciona clavijas independientes para la captura y la vista previa, el método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta un filtro de forma [inteligente](smart-tee-filter.md) , que divide la secuencia en una secuencia de captura y una secuencia de vista previa.</span><span class="sxs-lookup"><span data-stu-id="dacc4-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="dacc4-139">Desde el punto de vista de la aplicación, puede tratar simplemente todos los filtros de captura como si tuvieran PIN independientes y omitir la topología subyacente del gráfico.</span><span class="sxs-lookup"><span data-stu-id="dacc4-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="dacc4-140">Para la captura de archivos, conecte el PIN de captura a un filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="dacc4-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="dacc4-141">Para la vista previa dinámica, conecte el PIN de vista previa a un representador.</span><span class="sxs-lookup"><span data-stu-id="dacc4-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="dacc4-142">Si cambia las dos categorías, el gráfico podría quitar un número excesivo de fotogramas durante la captura de archivos. pero si el gráfico está conectado correctamente, quita los fotogramas de vista previa según sea necesario para mantener el rendimiento en la secuencia de captura.</span><span class="sxs-lookup"><span data-stu-id="dacc4-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="dacc4-143">En el ejemplo siguiente se muestra cómo conectar ambos flujos:</span><span class="sxs-lookup"><span data-stu-id="dacc4-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="dacc4-144">Algunos filtros de captura también admiten subtítulos (CC), que se indican mediante la **categoría de PIN \_ \_ VBI**.</span><span class="sxs-lookup"><span data-stu-id="dacc4-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="dacc4-145">Para capturar los subtítulos cerrados en un archivo, represente esta categoría al filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="dacc4-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="dacc4-146">Para ver los subtítulos cerrados en la ventana de vista previa, conéctese al representador:</span><span class="sxs-lookup"><span data-stu-id="dacc4-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="dacc4-147">El segundo parámetro de [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifica el tipo de medio y suele ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dacc4-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="dacc4-148">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="dacc4-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="dacc4-149">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="dacc4-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="dacc4-150">MEDIATYPE \_ intercalado (DV)</span><span class="sxs-lookup"><span data-stu-id="dacc4-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="dacc4-151">Puede usar este parámetro siempre que los pin de salida del filtro admitan la enumeración de los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="dacc4-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="dacc4-152">En el caso de los orígenes de archivos, el generador de gráficos de captura agrega automáticamente un filtro de analizador si es necesario y, a continuación, consulta los tipos de medios en el analizador.</span><span class="sxs-lookup"><span data-stu-id="dacc4-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="dacc4-153">(Para obtener un ejemplo, vea [recomprimir un archivo AVI](recompressing-an-avi-file.md)). Además, si el último filtro de la cadena tiene varios PIN de entrada, el método intenta enumerar sus tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="dacc4-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="dacc4-154">Sin embargo, no todos los filtros admiten esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="dacc4-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="dacc4-155">Buscar interfaces en filtros y PIN</span><span class="sxs-lookup"><span data-stu-id="dacc4-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="dacc4-156">Después de compilar un gráfico, normalmente necesitará encontrar varias interfaces expuestas por filtros y clavijas en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="dacc4-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="dacc4-157">Por ejemplo, un filtro de captura podría exponer la interfaz [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , mientras que los pin de salida del filtro podrían exponer la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="dacc4-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="dacc4-158">La manera más sencilla de encontrar una interfaz es usar el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="dacc4-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="dacc4-159">Este método recorre el gráfico (filtros y clavijas) hasta que encuentra la interfaz deseada.</span><span class="sxs-lookup"><span data-stu-id="dacc4-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="dacc4-160">Puede especificar el punto de partida de la búsqueda y puede limitar la búsqueda a los filtros que se encadenan hacia arriba o hacia abajo desde el punto de partida.</span><span class="sxs-lookup"><span data-stu-id="dacc4-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="dacc4-161">En el ejemplo siguiente se busca la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en un PIN de vista previa de vídeo:</span><span class="sxs-lookup"><span data-stu-id="dacc4-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="dacc4-162">En el tema [buscar una interfaz en un filtro o un PIN](find-an-interface-on-a-filter-or-pin.md) se muestra un enfoque alternativo que usa la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) en lugar de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span><span class="sxs-lookup"><span data-stu-id="dacc4-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="dacc4-163">El enfoque que se debe usar depende de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dacc4-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="dacc4-164">Si la aplicación ya usa **ICaptureGraphBuilder2** para compilar el gráfico, [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) es un buen enfoque.</span><span class="sxs-lookup"><span data-stu-id="dacc4-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="dacc4-165">En caso contrario, considere la posibilidad de usar los métodos **IGraphBuilder** .</span><span class="sxs-lookup"><span data-stu-id="dacc4-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="dacc4-166">Buscar PIN</span><span class="sxs-lookup"><span data-stu-id="dacc4-166">Finding Pins</span></span>

<span data-ttu-id="dacc4-167">Con menos frecuencia, es posible que necesite buscar un PIN individual en un filtro, aunque en la mayoría de los casos los métodos [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) y [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) le ahorrarán el problema.</span><span class="sxs-lookup"><span data-stu-id="dacc4-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="dacc4-168">Si necesita buscar un PIN determinado en un filtro, el método auxiliar [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) es útil.</span><span class="sxs-lookup"><span data-stu-id="dacc4-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="dacc4-169">Especifique la categoría, el tipo de medio (vídeo o audio), la dirección y si el PIN debe estar desconectado.</span><span class="sxs-lookup"><span data-stu-id="dacc4-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="dacc4-170">Por ejemplo, el código siguiente busca un PIN de vista previa de vídeo no conectado en un filtro de captura:</span><span class="sxs-lookup"><span data-stu-id="dacc4-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="dacc4-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dacc4-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dacc4-172">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="dacc4-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
