---
description: En este tema se trata el paso 4 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Paso 4: agregar el representador de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689596"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="41583-103">Paso 4: agregar el representador de vídeo</span><span class="sxs-lookup"><span data-stu-id="41583-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="41583-104">En este tema se trata el paso 4 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="41583-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="41583-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="41583-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="41583-106">DirectShow proporciona varios filtros diferentes que representan vídeo:</span><span class="sxs-lookup"><span data-stu-id="41583-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="41583-107">[**Filtro de representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="41583-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="41583-108">[Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="41583-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="41583-109">[Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="41583-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="41583-110">Para obtener más información sobre las diferencias entre estos filtros, consulte [elección del representador de vídeo adecuado](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="41583-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="41583-111">En este tutorial, cada filtro de representador de vídeo está incluido en una clase que abstrae algunas de las diferencias entre ellos.</span><span class="sxs-lookup"><span data-stu-id="41583-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="41583-112">Todas estas clases derivan de una clase base abstracta denominada `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="41583-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="41583-113">La declaración de `CVideoRenderer` se muestra en el [paso 2: declarar CVideoRenderer y las clases derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="41583-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="41583-114">El método siguiente intenta crear cada representador de vídeo, a su vez, a partir de los EVR, VMR-9 y, por último, VMR-7.</span><span class="sxs-lookup"><span data-stu-id="41583-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="41583-115">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="41583-115">EVR Filter</span></span>

<span data-ttu-id="41583-116">En el código siguiente se crea el filtro EVR y se agrega al gráfico filtro.</span><span class="sxs-lookup"><span data-stu-id="41583-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="41583-117">La función `AddFilterByCLSID` que se usa en este ejemplo se muestra en el tema [Agregar un filtro por CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="41583-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="41583-118">La `InitializeEVR` función inicializa el filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="41583-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="41583-119">Esta función realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="41583-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="41583-120">Consulta el filtro de la interfaz [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="41583-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="41583-121">Llama a [**IMFGetService:: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="41583-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="41583-122">Llama a [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para establecer la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="41583-123">Llama a [**IMFVideoDisplayControl:: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) para configurar el EVR para conservar la relación de aspecto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="41583-124">En el código siguiente se muestra la `InitializeEVR` función.</span><span class="sxs-lookup"><span data-stu-id="41583-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="41583-125">Después de compilar el gráfico, `DShowPlayer::RenderStreams` llama a `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="41583-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="41583-126">Este método realiza cualquier inicialización o limpieza final.</span><span class="sxs-lookup"><span data-stu-id="41583-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="41583-127">En el código siguiente se muestra la `CEVR` implementación de este método.</span><span class="sxs-lookup"><span data-stu-id="41583-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="41583-128">Si el EVR no está conectado a ningún otro filtro, este método quita el EVR del gráfico.</span><span class="sxs-lookup"><span data-stu-id="41583-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="41583-129">Esto puede ocurrir si el archivo multimedia no contiene una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="41583-130">Filtro VMR-9</span><span class="sxs-lookup"><span data-stu-id="41583-130">VMR-9 Filter</span></span>

<span data-ttu-id="41583-131">En el código siguiente se crea el filtro VMR-9 y se agrega al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="41583-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="41583-132">La `InitWindowlessVMR9` función inicializa la VMR-9 para el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="41583-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="41583-133">(Para obtener más información sobre el modo sin ventanas, vea [modo sin ventanas de VMR](vmr-windowless-mode.md)). Esta función realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="41583-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="41583-134">Consulta el filtro VMR-9 para la interfaz [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .</span><span class="sxs-lookup"><span data-stu-id="41583-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="41583-135">Llama al método [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) para establecer el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="41583-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="41583-136">Consulta el filtro VMR-9 para la interfaz [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="41583-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="41583-137">Llama al método [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) para establecer la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="41583-138">Llama al método [**IVMRWindowlessControl9:: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) para conservar la relación de aspecto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="41583-139">En el código siguiente se muestra la `InitWindowlessVMR9` función.</span><span class="sxs-lookup"><span data-stu-id="41583-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="41583-140">El `CVMR9::FinalizeGraph` método comprueba si el filtro VMR-9 está conectado y, si no es así, lo quita del gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="41583-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="41583-141">Filtro VMR-7</span><span class="sxs-lookup"><span data-stu-id="41583-141">VMR-7 Filter</span></span>

<span data-ttu-id="41583-142">Los pasos del filtro VMR-7 son casi idénticos a los de VMR-9, excepto en que se usan las interfaces VMR-7.</span><span class="sxs-lookup"><span data-stu-id="41583-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="41583-143">En el código siguiente se crea el filtro VMR-7 y se agrega al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="41583-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="41583-144">La `InitWindowlessVMR` función inicializa la VMR-7 para el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="41583-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="41583-145">Esta función realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="41583-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="41583-146">Consulta el filtro VMR-7 para la interfaz [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .</span><span class="sxs-lookup"><span data-stu-id="41583-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="41583-147">Llama al método [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) para establecer el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="41583-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="41583-148">Consulta el filtro VMR-7 para la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="41583-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="41583-149">Llama al método [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para establecer la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="41583-150">Llama al método [**IVMRWindowlessControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) para conservar la relación de aspecto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="41583-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="41583-151">En el código siguiente se muestra la `InitWindowlessVMR` función.</span><span class="sxs-lookup"><span data-stu-id="41583-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="41583-152">El `CVMR7::FinalizeGraph` método comprueba si el filtro VMR-7 está conectado y, si no es así, lo quita del gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="41583-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="41583-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41583-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41583-154">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="41583-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="41583-155">Usar el filtro EVR de DirectShow</span><span class="sxs-lookup"><span data-stu-id="41583-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="41583-156">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="41583-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
