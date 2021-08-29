---
description: Este tema es el paso 6 del tutorial Reproducción de audio y vídeo en DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Paso 6: Controlar eventos Graph eventos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100d9fa4fab3b72144bcd18cafca1626d44f4868abef1a6d25e777f46749d707
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928175"
---
# <a name="step-6-handle-graph-events"></a>Paso 6: Controlar eventos Graph eventos

Este tema es el paso 6 del tutorial Reproducción de audio y [vídeo en DirectShow](audio-video-playback-in-directshow.md). El código completo se muestra en el tema DirectShow [ejemplo de reproducción](directshow-playback-example.md).

Cuando la aplicación crea una nueva instancia de Filter Graph Manager, la aplicación llama a [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Este método registra la ventana de la aplicación para recibir eventos del gráfico de filtro.


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



El valor `WM_GRAPH_EVENT` es un mensaje de ventana privada. Cada vez que la aplicación recibe este mensaje, llama al `DShowPlayer::HandleGraphEvent` método .


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



El método `DShowPlayer::HandleGraphEvent` hace lo siguiente:

1.  Llama [**a IMediaEvent::GetEvent en**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) un bucle para obtener todos los eventos en cola.
2.  Invoca una función de devolución de llamada (*pfnOnGraphEvent*).
3.  Llama [**a IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar los datos asociados a cada evento.


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



El código siguiente muestra la función de devolución de llamada que se pasa a `DShowPlayer::HandleGraphEvent` . La función controla el número mínimo de eventos de grafo [**(EC \_ COMPLETE,**](ec-complete.md) [**EC \_ ERRORABORT**](ec-errorabort.md)y [**EC \_ USERABORT);**](ec-userabort.md)podría expandir la función para controlar eventos adicionales.


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

[DirectShow Ejemplo de reproducción](directshow-playback-example.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Respuesta a eventos](responding-to-events.md)
</dt> </dl>

 

 



