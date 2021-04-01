---
description: Creación de un gráfico de filtros VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Creación de un gráfico de filtros VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906741"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="52c54-103">Creación de un gráfico de filtros VMR-9</span><span class="sxs-lookup"><span data-stu-id="52c54-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="52c54-104">Dado que el filtro de representador de mezcla de vídeo 9 (VMR-9) no es el representador de vídeo predeterminado, una aplicación que use VMR-9 debe agregarlo explícitamente al gráfico y conectarlo.</span><span class="sxs-lookup"><span data-stu-id="52c54-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="52c54-105">En esta sección se presentan dos enfoques diferentes para crear gráficos de filtros con VMR-9.</span><span class="sxs-lookup"><span data-stu-id="52c54-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="52c54-106">Usar el generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="52c54-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="52c54-107">El generador de gráficos de captura es un objeto auxiliar para crear gráficos de filtros personalizados.</span><span class="sxs-lookup"><span data-stu-id="52c54-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="52c54-108">Puede usarlo para compilar gráficos VMR-9 como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="52c54-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="52c54-109">Cree e inicialice el generador de gráficos de captura, tal y como se describe en el tema [sobre el generador de gráficos de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="52c54-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="52c54-110">Llame a CoCreateInstance para crear el método VMR-9:</span><span class="sxs-lookup"><span data-stu-id="52c54-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="52c54-111">Llame a [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) en el administrador de gráficos de filtro para agregar el VMR-9 al gráfico de filtros:</span><span class="sxs-lookup"><span data-stu-id="52c54-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="52c54-112">Llame a [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar un filtro de origen para el archivo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="52c54-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="52c54-113">Llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para representar la secuencia de vídeo en la VMR:</span><span class="sxs-lookup"><span data-stu-id="52c54-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="52c54-114">Opcionalmente, vuelva a llamar a RenderStream para representar la secuencia de audio:</span><span class="sxs-lookup"><span data-stu-id="52c54-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="52c54-115">Puede mezclar varias secuencias de vídeo llamando a AddSourceFilter y RenderStream para cada archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="52c54-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="52c54-116">Usar el administrador de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="52c54-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="52c54-117">Si prefiere no usar el generador de gráficos de captura, puede crear un grafo de VMR-9 simplemente mediante métodos en el administrador de gráficos de filtro, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="52c54-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="52c54-118">Cree el VMR-9 y agréguelo al gráfico, tal como se muestra en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="52c54-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="52c54-119">Use AddSourceFilter para agregar un filtro de origen para el archivo de vídeo, tal como se muestra en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="52c54-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="52c54-120">Si desea representar el audio, cree una instancia del filtro de [representador de DirectSound](directsound-renderer-filter.md) y agréguela al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="52c54-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="52c54-121">Use el método IBaseFilter:: EnumPins para buscar un PIN de salida en el filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="52c54-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="52c54-122">Consulte [enumeración de PIN](enumerating-pins.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="52c54-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="52c54-123">Consulte el administrador de gráficos de filtro para la interfaz IFilterGraph2.</span><span class="sxs-lookup"><span data-stu-id="52c54-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="52c54-124">Llame a [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) con la \_ marca AM RenderEx \_ RENDERTOEXISTINGRENDERERS.</span><span class="sxs-lookup"><span data-stu-id="52c54-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="52c54-125">Esta llamada representa el PIN de salida, usando solo los filtros de representador que ya están en el gráfico, en este caso, VMR-9 y el representador de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="52c54-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="52c54-126">De esta forma, se evita que la lógica de conexión inteligente agregue el representador de vídeo predeterminado al gráfico, lo que dejaría que VMR-9 estuviera sin conexión.</span><span class="sxs-lookup"><span data-stu-id="52c54-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52c54-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52c54-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c54-128">Generar gráficos con el generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="52c54-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



