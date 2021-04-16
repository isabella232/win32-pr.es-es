---
description: En este artículo se describe cómo responder a los eventos que se producen en un gráfico de filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Respuesta a eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537203"
---
# <a name="responding-to-events"></a><span data-ttu-id="ddd86-103">Respuesta a eventos</span><span class="sxs-lookup"><span data-stu-id="ddd86-103">Responding to Events</span></span>

<span data-ttu-id="ddd86-104">En este artículo se describe cómo responder a los eventos que se producen en un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ddd86-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="ddd86-105">Cómo funciona la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ddd86-105">How Event Notification Works</span></span>

<span data-ttu-id="ddd86-106">Mientras se ejecuta una aplicación de DirectShow, se pueden producir eventos dentro del gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="ddd86-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="ddd86-107">Por ejemplo, un filtro podría encontrar un error de streaming.</span><span class="sxs-lookup"><span data-stu-id="ddd86-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="ddd86-108">Los filtros alertan al administrador de gráficos de filtro mediante el envío de eventos, que constan de un código de evento y dos parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="ddd86-109">El código de evento indica el tipo de evento y los parámetros de evento proporcionan información adicional.</span><span class="sxs-lookup"><span data-stu-id="ddd86-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="ddd86-110">El significado de los parámetros depende del código de evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="ddd86-111">Para obtener una lista completa de los códigos de evento, consulte [códigos de notificación de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ddd86-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="ddd86-112">Algunos eventos se controlan de forma silenciosa por el administrador de gráficos de filtro, sin que se notifique a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddd86-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="ddd86-113">Otros eventos se colocan en una cola para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddd86-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="ddd86-114">Dependiendo de la aplicación, hay varios eventos que es posible que deba controlar.</span><span class="sxs-lookup"><span data-stu-id="ddd86-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="ddd86-115">Este artículo se centra en tres eventos que son muy comunes:</span><span class="sxs-lookup"><span data-stu-id="ddd86-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="ddd86-116">El evento de [**\_ finalización de EC**](ec-complete.md) indica que la reproducción se ha completado con normalidad.</span><span class="sxs-lookup"><span data-stu-id="ddd86-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="ddd86-117">El [**evento \_ USERABORT de EC**](ec-userabort.md) indica que el usuario ha interrumpido la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ddd86-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="ddd86-118">Los representadores de vídeo envían este evento si el usuario cierra la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddd86-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="ddd86-119">El [**evento \_ ERRORABORT de EC**](ec-errorabort.md) indica que un error ha provocado que se detenga la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ddd86-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="ddd86-120">Usar la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ddd86-120">Using Event Notification</span></span>

<span data-ttu-id="ddd86-121">Una aplicación puede indicar al administrador de gráficos de filtro que envíe un mensaje de Windows a una ventana designada cada vez que se produzca un nuevo evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="ddd86-122">Esto permite que la aplicación responda dentro del bucle de mensajes de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ddd86-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="ddd86-123">En primer lugar, defina el mensaje que se enviará a la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddd86-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="ddd86-124">Las aplicaciones pueden usar números de mensaje en el intervalo de la aplicación de WM \_ a través de 0xBFFF como mensajes privados:</span><span class="sxs-lookup"><span data-stu-id="ddd86-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="ddd86-125">A continuación, consulte el administrador de gráficos de filtro para la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) y llame al método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :</span><span class="sxs-lookup"><span data-stu-id="ddd86-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="ddd86-126">Este método designa la ventana especificada (g \_ hWnd) como destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddd86-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="ddd86-127">Llame al método después de crear el gráfico de filtros, pero antes de ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ddd86-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="ddd86-128">WM \_ GRAPHNOTIFY es un mensaje de Windows normal.</span><span class="sxs-lookup"><span data-stu-id="ddd86-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="ddd86-129">Siempre que el administrador de gráficos de filtro coloca un nuevo evento en la cola de eventos, envía un mensaje de WM \_ GRAPHNOTIFY a la ventana de la aplicación designada.</span><span class="sxs-lookup"><span data-stu-id="ddd86-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="ddd86-130">El parámetro *lParam* del mensaje es igual que el tercer parámetro de [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="ddd86-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="ddd86-131">Este parámetro permite enviar datos de instancia con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddd86-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="ddd86-132">El parámetro *wParam* del mensaje de ventana siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="ddd86-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="ddd86-133">En la función **WindowProc** de la aplicación, agregue una instrucción Case para el \_ mensaje de GRAPHNOTIFY de WM:</span><span class="sxs-lookup"><span data-stu-id="ddd86-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="ddd86-134">En la función de controlador de eventos, llame al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para recuperar los eventos de la cola:</span><span class="sxs-lookup"><span data-stu-id="ddd86-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="ddd86-135">El método [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera el código de evento y los dos parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="ddd86-136">El cuarto parámetro **GetEvent** especifica la cantidad de tiempo de espera para un evento, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="ddd86-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="ddd86-137">Dado que la aplicación llama a este método en respuesta a un mensaje de GRAPHNOTIFY de WM \_ , el evento ya está en cola.</span><span class="sxs-lookup"><span data-stu-id="ddd86-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="ddd86-138">Por lo tanto, el valor de tiempo de espera se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="ddd86-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="ddd86-139">La notificación de eventos y el bucle de mensajes son asincrónicas, por lo que la cola podría contener más de un evento en el momento en que la aplicación responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="ddd86-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="ddd86-140">Además, el administrador de gráficos de filtro puede quitar determinados eventos de la cola, si no son válidos.</span><span class="sxs-lookup"><span data-stu-id="ddd86-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="ddd86-141">Por lo tanto, debe llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, lo que indica que la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="ddd86-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="ddd86-142">En este ejemplo, la aplicación responde a [**EC \_ Complete**](ec-complete.md), [**EC \_ USERABORT**](ec-userabort.md)y [**EC \_ ERRORABORT**](ec-errorabort.md) mediante la invocación de la función de limpieza definida por la aplicación, que hace que la aplicación se cierre correctamente.</span><span class="sxs-lookup"><span data-stu-id="ddd86-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="ddd86-143">En el ejemplo se omiten los dos parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="ddd86-144">Después de recuperar un evento, llame a [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) a todos los recursos libres asociados a los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="ddd86-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="ddd86-145">Tenga en cuenta que un evento de [**\_ finalización de EC**](ec-complete.md) no hace que el gráfico de filtros se detenga.</span><span class="sxs-lookup"><span data-stu-id="ddd86-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="ddd86-146">La aplicación puede detener o pausar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ddd86-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="ddd86-147">Si detiene el gráfico, los filtros liberan los recursos que contienen.</span><span class="sxs-lookup"><span data-stu-id="ddd86-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="ddd86-148">Si pausa el gráfico, los filtros continúan manteniendo los recursos.</span><span class="sxs-lookup"><span data-stu-id="ddd86-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="ddd86-149">Además, cuando una pausa en el representador de vídeo, muestra una imagen estática del fotograma más reciente.</span><span class="sxs-lookup"><span data-stu-id="ddd86-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="ddd86-150">Antes de liberar el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele la notificación de eventos llamando a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un identificador de ventana **nulo** :</span><span class="sxs-lookup"><span data-stu-id="ddd86-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="ddd86-151">En el controlador de mensajes de WM \_ GRAPHNOTIFY, compruebe el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span><span class="sxs-lookup"><span data-stu-id="ddd86-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="ddd86-152">Esto evita un posible error que se puede producir si la aplicación recibe la notificación de eventos después de liberar el puntero.</span><span class="sxs-lookup"><span data-stu-id="ddd86-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddd86-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddd86-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddd86-154">Tareas básicas de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ddd86-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="ddd86-155">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ddd86-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



