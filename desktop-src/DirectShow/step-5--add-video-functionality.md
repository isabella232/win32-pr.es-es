---
description: En este tema se trata el paso 5 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Paso 5: agregar funcionalidad de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278288"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="2a62c-103">Paso 5: agregar funcionalidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a62c-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="2a62c-104">En este tema se trata el paso 5 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="2a62c-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="2a62c-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="2a62c-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="2a62c-106">Para asegurarse de que el vídeo se muestra correctamente, la aplicación debe responder a los mensajes [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)y [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="2a62c-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="2a62c-107">Administrar \_ mensajes de Paint Paint</span><span class="sxs-lookup"><span data-stu-id="2a62c-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="2a62c-108">Cuando la aplicación recibe un mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) , es posible que el representador de vídeo tenga que volver a dibujar el último fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2a62c-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="2a62c-109">Para el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR), llame a [**IMFVideoDisplayControl:: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="2a62c-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="2a62c-110">Para el [filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9), llame a [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="2a62c-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="2a62c-111">Para el [filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), llame a [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="2a62c-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a><span data-ttu-id="2a62c-112">Administrar mensajes de tamaño de WM \_</span><span class="sxs-lookup"><span data-stu-id="2a62c-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="2a62c-113">Si cambia el tamaño de la ventana de vídeo, notifique al representador de vídeo que cambie el tamaño del vídeo.</span><span class="sxs-lookup"><span data-stu-id="2a62c-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="2a62c-114">En el caso de EVR, llame a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="2a62c-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="2a62c-115">Para la VMR-9, llame a [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="2a62c-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



<span data-ttu-id="2a62c-116">Para la VMR-7, llame a [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="2a62c-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="2a62c-117">Administrar \_ mensajes DISPLAYCHANGE de WM</span><span class="sxs-lookup"><span data-stu-id="2a62c-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="2a62c-118">Si cambia el modo de presentación, debe notificar al filtro VMR-9 o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="2a62c-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="2a62c-119">En el caso de VMR-9, llame a [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="2a62c-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="2a62c-120">En el caso de VMR-7, llame a [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="2a62c-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="2a62c-121">No es necesario notificar a EVR cuando cambia el modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="2a62c-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="2a62c-122">Siguiente: [paso 6: controlar eventos de gráfico](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="2a62c-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a62c-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a62c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a62c-124">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a62c-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="2a62c-125">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a62c-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="2a62c-126">Usar el filtro EVR de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a62c-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="2a62c-127">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a62c-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
