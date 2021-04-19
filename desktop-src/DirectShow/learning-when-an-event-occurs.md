---
description: Aprendizaje cuando se produce un evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Aprendizaje cuando se produce un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537702"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="ee393-103">Aprendizaje cuando se produce un evento</span><span class="sxs-lookup"><span data-stu-id="ee393-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="ee393-104">Para procesar los eventos de DirectShow, una aplicación necesita una manera de averiguar cuándo esperan los eventos en la cola.</span><span class="sxs-lookup"><span data-stu-id="ee393-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="ee393-105">El administrador de gráficos de filtro proporciona dos maneras de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="ee393-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="ee393-106">**Notificación de ventana:** El administrador de gráficos de filtros envía un mensaje de Windows definido por el usuario a una ventana de la aplicación cada vez que hay un nuevo evento.</span><span class="sxs-lookup"><span data-stu-id="ee393-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="ee393-107">**Señalización de eventos:** El administrador de gráficos de filtro indica un evento de Windows si hay eventos de DirectShow en la cola y restablece el evento si la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="ee393-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="ee393-108">Una aplicación puede utilizar cualquiera de las técnicas.</span><span class="sxs-lookup"><span data-stu-id="ee393-108">An application can use either technique.</span></span> <span data-ttu-id="ee393-109">La notificación de ventana suele ser más sencilla.</span><span class="sxs-lookup"><span data-stu-id="ee393-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="ee393-110">**Notificación de ventana**</span><span class="sxs-lookup"><span data-stu-id="ee393-110">**Window Notification**</span></span>

<span data-ttu-id="ee393-111">Para configurar la notificación de ventana, llame al método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) y especifique un mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="ee393-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="ee393-112">Las aplicaciones pueden usar números de mensaje en el intervalo de la aplicación de WM \_ a través de 0xBFFF como mensajes privados.</span><span class="sxs-lookup"><span data-stu-id="ee393-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="ee393-113">Siempre que el administrador de gráficos de filtro coloca una nueva notificación de eventos en la cola, envía este mensaje a la ventana designada.</span><span class="sxs-lookup"><span data-stu-id="ee393-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="ee393-114">La aplicación responde al mensaje desde dentro del bucle de mensajes de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ee393-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="ee393-115">En el ejemplo de código siguiente se muestra cómo establecer la ventana de notificación.</span><span class="sxs-lookup"><span data-stu-id="ee393-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="ee393-116">El mensaje es un mensaje de Windows normal y se publica por separado de la cola de notificación de eventos de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee393-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="ee393-117">La ventaja de este enfoque es que la mayoría de las aplicaciones ya implementan un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ee393-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="ee393-118">Por lo tanto, puede incorporar el control de eventos de DirectShow sin mucho trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="ee393-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="ee393-119">En el ejemplo de código siguiente se muestra un esquema de cómo responder al mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="ee393-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="ee393-120">Para obtener un ejemplo completo, vea [responder a eventos](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="ee393-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="ee393-121">Dado que la notificación de eventos y el bucle de mensajes son asincrónicas, la cola podría contener más de un evento en el momento en que la aplicación responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="ee393-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="ee393-122">Además, a veces se pueden borrar los eventos de la cola si dejan de ser válidos.</span><span class="sxs-lookup"><span data-stu-id="ee393-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="ee393-123">Por lo tanto, en el código de control de eventos, llame a [**IAMMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) hasta que devuelva un código de error, que indica que la cola está vacía.</span><span class="sxs-lookup"><span data-stu-id="ee393-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="ee393-124">Antes de liberar el puntero [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele la notificación de eventos llamando a [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) con un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ee393-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="ee393-125">En el código de procesamiento de eventos, compruebe si el puntero de **IMediaEventEx** es válido antes de llamar a [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="ee393-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="ee393-126">Estos pasos impiden un posible error, en el que la aplicación recibe la notificación de eventos después de haber liberado el puntero **IMediaEventEx** .</span><span class="sxs-lookup"><span data-stu-id="ee393-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="ee393-127">**Señalización de eventos**</span><span class="sxs-lookup"><span data-stu-id="ee393-127">**Event Signaling**</span></span>

<span data-ttu-id="ee393-128">El administrador de gráficos de filtro mantiene un evento de restablecimiento manual que refleja el estado de la cola de eventos.</span><span class="sxs-lookup"><span data-stu-id="ee393-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="ee393-129">Si la cola contiene notificaciones de eventos pendientes, el administrador de gráficos de filtros indica el evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="ee393-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="ee393-130">Si la cola está vacía, una llamada al método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) restablece el evento.</span><span class="sxs-lookup"><span data-stu-id="ee393-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="ee393-131">Una aplicación puede utilizar este evento para determinar el estado de la cola.</span><span class="sxs-lookup"><span data-stu-id="ee393-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="ee393-132">La terminología puede resultar confusa aquí.</span><span class="sxs-lookup"><span data-stu-id="ee393-132">The terminology can be confusing here.</span></span> <span data-ttu-id="ee393-133">El evento de restablecimiento manual es el tipo de evento creado por la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) de Windows; no tiene nada que hacer con los eventos definidos por DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee393-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="ee393-134">Llame al método [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) para obtener un identificador para el evento de restablecimiento manual.</span><span class="sxs-lookup"><span data-stu-id="ee393-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="ee393-135">Espere a que se Señalice el evento llamando a una función como [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="ee393-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="ee393-136">Una vez señalado el evento, llame a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obtener el evento de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee393-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="ee393-137">En el ejemplo de código siguiente se muestra este método.</span><span class="sxs-lookup"><span data-stu-id="ee393-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="ee393-138">Obtiene el identificador de evento y, a continuación, espera en intervalos de 100 milisegundos para que se Señalice el evento.</span><span class="sxs-lookup"><span data-stu-id="ee393-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="ee393-139">Si el evento se señala, llama a **GetEvent** e imprime el código de evento y los parámetros de evento en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="ee393-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="ee393-140">El bucle finaliza cuando se produce el evento de [**\_ finalización de EC**](ec-complete.md) , lo que indica que se ha completado la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ee393-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="ee393-141">Dado que el gráfico de filtros establece o restablece automáticamente el evento cuando sea necesario, la aplicación no debería hacerlo.</span><span class="sxs-lookup"><span data-stu-id="ee393-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="ee393-142">Además, al liberar el gráfico de filtros, el gráfico de filtros cierra el controlador de eventos, por lo que no debe usar el identificador de eventos después de ese punto.</span><span class="sxs-lookup"><span data-stu-id="ee393-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
