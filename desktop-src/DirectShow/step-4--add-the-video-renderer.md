---
description: Este tema es el paso 4 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Paso 4: Agregar el representador de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2d73dce5bba34f92c8df59cd9730ef1e25b57b9757039d9bda5c2e4432d734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051415"
---
# <a name="step-4-add-the-video-renderer"></a>Paso 4: Agregar el representador de vídeo

Este tema es el paso 4 del tutorial [Reproducción de audio y](audio-video-playback-in-directshow.md)vídeo en DirectShow . El código completo se muestra en el tema DirectShow [ejemplo de reproducción.](directshow-playback-example.md)

DirectShow proporciona varios filtros diferentes que representan vídeo:

-   [**Filtro de representador de vídeo**](enhanced-video-renderer-filter.md) mejorado (EVR)
-   [Filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)

Para obtener más información sobre las diferencias entre estos filtros, vea [Elección del representador de vídeo correcto.](choosing-the-right-renderer.md)

En este tutorial, cada filtro de representador de vídeo está encapsulado por una clase que abstrae algunas de las diferencias entre ellos. Todas estas clases derivan de una clase base abstracta denominada `CVideoRenderer` . La declaración de `CVideoRenderer` se muestra en Paso [2: Declarar CVideoRenderer y Clases derivadas](step-2--declare-cvideorenderer-and-derived-classes.md).

El método siguiente intenta crear cada representador de vídeo a su vez, empezando por evr, vmr-9 y, por último, VMR-7.


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



### <a name="evr-filter"></a>Filtro EVR

El código siguiente crea el filtro EVR y lo agrega al gráfico de filtros. La función `AddFilterByCLSID` utilizada en este ejemplo se muestra en el tema Agregar un filtro por [CLSID](add-a-filter-by-clsid.md).


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



La `InitializeEVR` función inicializa el filtro EVR. Esta función realiza los pasos siguientes.

1.  Consulta el filtro para la [**interfaz IMFGetService.**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)
2.  Llama [**a IMFGetService::GetService para**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) obtener un puntero a la interfaz [**IMFVideoDisplayControl.**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol)
3.  Llama [**a IMFVideoDisplayControl::SetVideoWindow para**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) establecer la ventana de vídeo.
4.  Llama [**a IMFVideoDisplayControl::SetAspectRatioMode para**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) configurar la EVR a fin de conservar la relación de aspecto del vídeo.

En el código siguiente se muestra la `InitializeEVR` función .


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



Una vez creado el gráfico, llama `DShowPlayer::RenderStreams` a `CVideoRenderer::FinalizeGraph` . Este método realiza cualquier inicialización o limpieza final. El código siguiente muestra la `CEVR` implementación de este método.


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



Si el EVR no está conectado a ningún otro filtro, este método quita el EVR del gráfico. Esto puede ocurrir si el archivo multimedia no contiene una secuencia de vídeo.

### <a name="vmr-9-filter"></a>Filtro VMR-9

El código siguiente crea el filtro VMR-9 y lo agrega al gráfico de filtros.


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



La `InitWindowlessVMR9` función inicializa VMR-9 para el modo sin ventana. (Para obtener más información sobre el modo sin ventanas, vea [Modo sin ventanas de VMR).](vmr-windowless-mode.md) Esta función realiza los pasos siguientes.

1.  Consulta el filtro VMR-9 para la [**interfaz IVMRFilterConfig9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)
2.  Llama al [**método IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) para establecer el modo sin ventanas.
3.  Consulta el filtro VMR-9 para la [**interfaz IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)
4.  Llama al [**método IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) para establecer la ventana de vídeo.
5.  Llama al [**método IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) para conservar la relación de aspecto del vídeo.

En el código siguiente se muestra la `InitWindowlessVMR9` función .


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



El `CVMR9::FinalizeGraph` método comprueba si el filtro VMR-9 está conectado y, si no, lo quita del gráfico de filtros.


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



### <a name="vmr-7-filter"></a>Filtro VMR-7

Los pasos para el filtro VMR-7 son casi idénticos a los de VMR-9, salvo que se usan las interfaces VMR-7 en su lugar. El código siguiente crea el filtro VMR-7 y lo agrega al gráfico de filtros.


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



La `InitWindowlessVMR` función inicializa VMR-7 para el modo sin ventana. Esta función realiza los pasos siguientes.

1.  Consulta el filtro VMR-7 para la [**interfaz IVMRFilterConfig.**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig)
2.  Llama al [**método IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) para establecer el modo sin ventanas.
3.  Consulta el filtro VMR-7 para la [**interfaz IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)
4.  Llama al [**método IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) para establecer la ventana de vídeo.
5.  Llama al [**método IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) para conservar la relación de aspecto del vídeo.

En el código siguiente se muestra la `InitWindowlessVMR` función .


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



El `CVMR7::FinalizeGraph` método comprueba si el filtro VMR-7 está conectado y, si no, lo quita del gráfico de filtros.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Ejemplo de reproducción](directshow-playback-example.md)
</dt> <dt>

[Uso del DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
