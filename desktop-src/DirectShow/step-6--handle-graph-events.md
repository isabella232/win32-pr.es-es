---
description: Este tema es el paso 6 del tutorial reproducción de audio y vídeo en DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Paso 6: control de eventos de gráfico'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678267"
---
# <a name="step-6-handle-graph-events"></a>Paso 6: control de eventos de gráfico

Este tema es el paso 6 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md). El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).

Cuando la aplicación crea una nueva instancia del administrador de gráficos de filtros, la aplicación llama a [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Este método registra la ventana de la aplicación para recibir los eventos del gráfico de filtro.


```C++
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
```



El valor `WM_GRAPH_EVENT` es un mensaje de ventana privada. Cada vez que la aplicación recibe este mensaje, llama al `DShowPlayer::HandleGraphEvent` método.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



El método `DShowPlayer::HandleGraphEvent` hace lo siguiente:

1.  Llama a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en un bucle para obtener todos los eventos en cola.
2.  Invoca una función de devolución de llamada (*pfnOnGraphEvent*).
3.  Llama a [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar los datos asociados a cada evento.


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



En el código siguiente se muestra la función de devolución de llamada que se pasa a `DShowPlayer::HandleGraphEvent` . La función controla el número mínimo de eventos de gráfico ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)y [**EC \_ USERABORT**](ec-userabort.md)); puede expandir la función para controlar eventos adicionales.


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Ejemplo de reproducción de DirectShow](directshow-playback-example.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Respuesta a eventos](responding-to-events.md)
</dt> </dl>

 

 



