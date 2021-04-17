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
# <a name="step-5-add-video-functionality"></a>Paso 5: agregar funcionalidad de vídeo

En este tema se trata el paso 5 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md). El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).

Para asegurarse de que el vídeo se muestra correctamente, la aplicación debe responder a los mensajes [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)y [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md) como se indica a continuación.

### <a name="handle-wm_paint-messages"></a>Administrar \_ mensajes de Paint Paint

Cuando la aplicación recibe un mensaje de [**\_ dibujo de WM**](../gdi/wm-paint.md) , es posible que el representador de vídeo tenga que volver a dibujar el último fotograma de vídeo. Para el filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR), llame a [**IMFVideoDisplayControl:: RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


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



Para el [filtro de representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9), llame a [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


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



Para el [filtro de representador de mezcla de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), llame a [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


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



### <a name="handle-wm_size-messages"></a>Administrar mensajes de tamaño de WM \_

Si cambia el tamaño de la ventana de vídeo, notifique al representador de vídeo que cambie el tamaño del vídeo. En el caso de EVR, llame a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


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



Para la VMR-9, llame a [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


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



Para la VMR-7, llame a [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


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



### <a name="handle-wm_displaychange-messages"></a>Administrar \_ mensajes DISPLAYCHANGE de WM

Si cambia el modo de presentación, debe notificar al filtro VMR-9 o VMR-7. En el caso de VMR-9, llame a [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


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



En el caso de VMR-7, llame a [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


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



No es necesario notificar a EVR cuando cambia el modo de presentación.

Siguiente: [paso 6: controlar eventos de gráfico](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Ejemplo de reproducción de DirectShow](directshow-playback-example.md)
</dt> <dt>

[Usar el filtro EVR de DirectShow](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
