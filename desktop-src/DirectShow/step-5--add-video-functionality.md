---
description: Este tema es el paso 5 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: 'Paso 5: Agregar funcionalidad de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951784"
---
# <a name="step-5-add-video-functionality"></a>Paso 5: Agregar funcionalidad de vídeo

Este tema es el paso 5 del tutorial [Reproducción de audio y](audio-video-playback-in-directshow.md)vídeo en DirectShow . El código completo se muestra en el tema DirectShow [ejemplo de reproducción](directshow-playback-example.md).

Para asegurarse de que el vídeo se muestra correctamente, la aplicación debe responder a los mensajes [**\_ WM PAINT,**](../gdi/wm-paint.md) [**WM \_ SIZE**](../winmsg/wm-size.md)y [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) como se indica a continuación.

### <a name="handle-wm_paint-messages"></a>Controlar mensajes \_ WM PAINT

Cuando la aplicación recibe un [**mensaje \_ WM PAINT,**](../gdi/wm-paint.md) es posible que el representador de vídeo tenga que volver a dibujar el último fotograma de vídeo. Para el [**filtro Representador de**](enhanced-video-renderer-filter.md) vídeo mejorado (EVR), llame [**a IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


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



Para el [filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9), llame a [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


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



Para el [filtro de representador de](video-mixing-renderer-filter-7.md) mezcla de vídeo 7 (VMR-7), llame a [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


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



### <a name="handle-wm_size-messages"></a>Controlar mensajes WM \_ SIZE

Si cambia el tamaño de la ventana de vídeo, notifique al representador de vídeo que cambie el tamaño del vídeo. En el caso de EVR, llame [**a IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


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



Para VMR-9, llame a [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


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



Para VMR-7, llame a [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


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



### <a name="handle-wm_displaychange-messages"></a>Controlar mensajes \_ DISPLAYCHANGE de WM

Si cambia el modo de presentación, debe notificar al filtro VMR-9 o VMR-7. Para VMR-9, llame a [**IVMRWindowlessControl9::D isplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


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



Para VMR-7, llame a [**IVMRWindowlessControl::D isplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


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



No es necesario notificar al EVR cuando cambia el modo de presentación.

Siguiente: [Paso 6: Controlar Graph eventos](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Ejemplo de reproducción](directshow-playback-example.md)
</dt> <dt>

[Uso del DirectShow EVR](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Uso del representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
