---
description: Este tema es el paso 7 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Paso 7: Controles de transporte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8253efab566f5dc14a0d0210a26e84cb0a50113389d54b7a871d818a17296ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072419"
---
# <a name="step-7-transport-controls"></a>Paso 7: Controles de transporte

Este tema es el paso 7 del tutorial [Reproducción de audio y](audio-video-playback-in-directshow.md)vídeo en DirectShow . El código completo se muestra en el tema DirectShow [ejemplo de reproducción](directshow-playback-example.md).

El último paso es agregar controles de transporte (reproducir, pausar y detener). Para reproducir el archivo, llame a [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



Para pausar, llame [**a IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



Para detener, llame a [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Ejemplo de reproducción](directshow-playback-example.md)
</dt> <dt>

[Estados de filtro](filter-states.md)
</dt> </dl>

 

 



