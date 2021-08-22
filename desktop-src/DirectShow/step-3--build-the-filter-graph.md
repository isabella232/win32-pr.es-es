---
description: Este tema es el paso 3 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Paso 3: Compilar el filtro Graph'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4903e08b19e15721c8b62f130261bb4d05fcd94d544380b2e501f56d60704d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072509"
---
# <a name="step-3-build-the-filter-graph"></a>Paso 3: Compilar el filtro Graph

Este tema es el paso 3 del tutorial [Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md). El código completo se muestra en el tema DirectShow [ejemplo de reproducción.](directshow-playback-example.md)

El siguiente paso consiste en crear un gráfico de filtro para reproducir el archivo multimedia.

### <a name="opening-a-media-file"></a>Abrir un archivo multimedia

El `DShowPlayer::OpenFile` método abre un archivo multimedia para la reproducción. Este método hace lo siguiente:

1.  Crea un nuevo gráfico de filtros (vacío).
2.  Llama [**a IGraphBuilder::AddSourceFilter para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) agregar un filtro de origen para el archivo especificado.
3.  Representa las secuencias en el filtro de origen.


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



### <a name="creating-the-filter-graph-manager"></a>Crear el Administrador de Graph filtros

El `DShowPlayer::InitializeGraph` método crea un nuevo gráfico de filtro. Este método hace lo siguiente:

1.  Llama [**a CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una nueva instancia de [Filter Graph Manager](filter-graph-manager.md).
2.  Consulta el Administrador de Graph para las interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**e IMediaEventEx.**](/windows/desktop/api/Control/nn-control-imediaeventex)
3.  Llama [**a IMediaEventEx::SetNotifyWindow para**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) configurar la notificación de eventos. Para obtener más información, vea [Notificación de eventos en DirectShow](event-notification-in-directshow.md).


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



### <a name="rendering-the-streams"></a>Representación de la Secuencias

El siguiente paso consiste en conectar el filtro de origen a uno o varios filtros de representador.

El `DShowPlayer::RenderStreams` método realiza los pasos siguientes.

1.  Consulta el Administrador de Graph filtros para la [**interfaz IFilterGraph2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
2.  Agrega un filtro de representador de vídeo al gráfico de filtros.
3.  Agrega el [filtro de representador de Direct Sound](directsound-renderer-filter.md) al gráfico de filtros para admitir la reproducción de audio. Para obtener más información sobre cómo agregar filtros al gráfico de filtros, vea [Agregar un filtro por CLSID.](add-a-filter-by-clsid.md)
4.  Enumera los pines de salida en el filtro de origen. Para obtener más información sobre cómo enumerar los pins, [vea Enumerating Pins](enumerating-pins.md).
5.  Para cada pin, llama al [**método IFilterGraph2::RenderEx.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) Este método conecta el pin de salida a un filtro de representador y agrega filtros intermedios si es necesario (por ejemplo, descodificadores).
6.  Llama `CVideoRenderer::FinalizeGraph` a para terminar de inicializar el representador de vídeo.
7.  Quita el filtro [Representador de Direct Sound](directsound-renderer-filter.md) si ese filtro no está conectado a otro filtro. Esto puede ocurrir si el archivo de origen no contiene una secuencia de audio.


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



Este es el código de la `RemoveUnconnectedRenderer` función , que se usa en el ejemplo anterior.


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



### <a name="releasing-the-filter-graph"></a>Liberar el filtro Graph

Cuando se cierra la aplicación, debe liberar el gráfico de filtro, como se muestra en el código siguiente.


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



Siguiente: [Paso 4: Agregar el representador de vídeo](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Ejemplo de reproducción](directshow-playback-example.md)
</dt> <dt>

[Compilar el filtro Graph](building-the-filter-graph.md)
</dt> <dt>

[Técnicas Graph-Building general](general-graph-building-techniques.md)
</dt> </dl>

 

 
