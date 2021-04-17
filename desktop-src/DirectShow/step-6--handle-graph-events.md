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
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="3e0f0-103">Paso 6: control de eventos de gráfico</span><span class="sxs-lookup"><span data-stu-id="3e0f0-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="3e0f0-104">Este tema es el paso 6 del tutorial [reproducción de audio y vídeo en DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="3e0f0-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="3e0f0-105">El código completo se muestra en el tema [ejemplo de reproducción de DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="3e0f0-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="3e0f0-106">Cuando la aplicación crea una nueva instancia del administrador de gráficos de filtros, la aplicación llama a [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="3e0f0-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="3e0f0-107">Este método registra la ventana de la aplicación para recibir los eventos del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-107">This method registers the application window to receive events from the filter graph.</span></span>


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



<span data-ttu-id="3e0f0-108">El valor `WM_GRAPH_EVENT` es un mensaje de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="3e0f0-109">Cada vez que la aplicación recibe este mensaje, llama al `DShowPlayer::HandleGraphEvent` método.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="3e0f0-110">El método `DShowPlayer::HandleGraphEvent` hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e0f0-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="3e0f0-111">Llama a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) en un bucle para obtener todos los eventos en cola.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="3e0f0-112">Invoca una función de devolución de llamada (*pfnOnGraphEvent*).</span><span class="sxs-lookup"><span data-stu-id="3e0f0-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="3e0f0-113">Llama a [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para liberar los datos asociados a cada evento.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


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



<span data-ttu-id="3e0f0-114">En el código siguiente se muestra la función de devolución de llamada que se pasa a `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="3e0f0-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="3e0f0-115">La función controla el número mínimo de eventos de gráfico ([**EC \_ Complete**](ec-complete.md), [**EC \_ ERRORABORT**](ec-errorabort.md)y [**EC \_ USERABORT**](ec-userabort.md)); puede expandir la función para controlar eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="3e0f0-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3e0f0-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e0f0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e0f0-117">Reproducción de audio y vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e0f0-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="3e0f0-118">Ejemplo de reproducción de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e0f0-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="3e0f0-119">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e0f0-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="3e0f0-120">Respuesta a eventos</span><span class="sxs-lookup"><span data-stu-id="3e0f0-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



