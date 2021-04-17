---
description: En este tema se trata el paso 3 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Paso 3: compilar el gráfico de filtro'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678272"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="fac5b-103">Paso 3: compilar el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="fac5b-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="fac5b-104">En este tema se trata el paso 3 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="fac5b-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="fac5b-106">El siguiente paso consiste en crear un gráfico de filtro para reproducir el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="fac5b-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="fac5b-107">Abrir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="fac5b-107">Opening a Media File</span></span>

<span data-ttu-id="fac5b-108">El `DShowPlayer::OpenFile` método abre un archivo multimedia para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fac5b-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="fac5b-109">Este método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fac5b-109">This method does the following:</span></span>

1.  <span data-ttu-id="fac5b-110">Crea un nuevo gráfico de filtro (vacío).</span><span class="sxs-lookup"><span data-stu-id="fac5b-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="fac5b-111">Llama a [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar un filtro de origen para el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="fac5b-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="fac5b-112">Representa las secuencias en el filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="fac5b-112">Renders the streams on the source filter.</span></span>


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="fac5b-113">Crear el administrador de gráficos de filtro</span><span class="sxs-lookup"><span data-stu-id="fac5b-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="fac5b-114">El `DShowPlayer::InitializeGraph` método crea un nuevo gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fac5b-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="fac5b-115">Este método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fac5b-115">This method does the following:</span></span>

1.  <span data-ttu-id="fac5b-116">Llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una nueva instancia del [Administrador de gráficos de filtro](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="fac5b-117">Consulta el administrador de gráficos de filtro para las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="fac5b-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="fac5b-118">Llama a [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) para configurar la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="fac5b-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="fac5b-119">Para obtener más información, vea [notificación de eventos en DirectShow](event-notification-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a><span data-ttu-id="fac5b-120">Representar las secuencias</span><span class="sxs-lookup"><span data-stu-id="fac5b-120">Rendering the Streams</span></span>

<span data-ttu-id="fac5b-121">El siguiente paso consiste en conectar el filtro de origen a uno o varios filtros de representación.</span><span class="sxs-lookup"><span data-stu-id="fac5b-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="fac5b-122">El `DShowPlayer::RenderStreams` método realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="fac5b-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="fac5b-123">Consulta el administrador de gráficos de filtro para la interfaz [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .</span><span class="sxs-lookup"><span data-stu-id="fac5b-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="fac5b-124">Agrega un filtro de representador de vídeo al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="fac5b-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="fac5b-125">Agrega el [filtro de representador de DirectSound](directsound-renderer-filter.md) al gráfico de filtros para admitir la reproducción de audio.</span><span class="sxs-lookup"><span data-stu-id="fac5b-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="fac5b-126">Para obtener más información sobre cómo agregar filtros al gráfico de filtros, vea [Agregar un filtro por CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="fac5b-127">Enumera los clavijas de salida en el filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="fac5b-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="fac5b-128">Para obtener más información sobre la enumeración de PIN, consulte [enumeración de PIN](enumerating-pins.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="fac5b-129">Para cada pin, llama al método [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) .</span><span class="sxs-lookup"><span data-stu-id="fac5b-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="fac5b-130">Este método conecta el PIN de salida a un filtro de representador, agregando filtros intermedios si es necesario (como descodificadores).</span><span class="sxs-lookup"><span data-stu-id="fac5b-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="fac5b-131">Llamadas `CVideoRenderer::FinalizeGraph` para finalizar la inicialización del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fac5b-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="fac5b-132">Quita el filtro de [representador de DirectSound](directsound-renderer-filter.md) si ese filtro no está conectado a otro filtro.</span><span class="sxs-lookup"><span data-stu-id="fac5b-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="fac5b-133">Esto puede ocurrir si el archivo de origen no contiene una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="fac5b-133">This can occur if the source file does not contain an audio stream.</span></span>


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



<span data-ttu-id="fac5b-134">Este es el código de la `RemoveUnconnectedRenderer` función, que se usa en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="fac5b-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="fac5b-135">Liberar el gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="fac5b-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="fac5b-136">Cuando se cierra la aplicación, debe liberar el gráfico de filtro, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="fac5b-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



<span data-ttu-id="fac5b-137">Siguiente: [paso 4: agregar el representador de vídeo](step-4--add-the-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="fac5b-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fac5b-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fac5b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac5b-139">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fac5b-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="fac5b-140">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="fac5b-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="fac5b-141">Compilar el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="fac5b-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="fac5b-142">Técnicas generales de Graph-Building</span><span class="sxs-lookup"><span data-stu-id="fac5b-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
