---
description: Control de un dispositivo externo
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Control de un dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536694"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="d6182-103">Control de un dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="d6182-103">Controlling an External Device</span></span>

<span data-ttu-id="d6182-104">Para controlar un dispositivo de grabadora de cintas de vídeo (VTR), use el método [**IAMExtTransport::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="d6182-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="d6182-105">Especifique el nuevo estado mediante una de las constantes que aparecen en el [Estado de transporte del dispositivo](device-transport-state.md).</span><span class="sxs-lookup"><span data-stu-id="d6182-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="d6182-106">Por ejemplo, para detener el dispositivo, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6182-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="d6182-107">Dado que el VTR es un dispositivo físico, normalmente se produce un retraso entre la emisión del comando y la finalización del comando.</span><span class="sxs-lookup"><span data-stu-id="d6182-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="d6182-108">La aplicación debe crear un segundo subproceso de trabajo que espera a que finalice el comando.</span><span class="sxs-lookup"><span data-stu-id="d6182-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="d6182-109">Cuando el comando finaliza, el subproceso puede actualizar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d6182-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="d6182-110">Use una sección crítica para serializar el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="d6182-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="d6182-111">Algunos VTRs pueden notificar a la aplicación cuando el estado de transporte del dispositivo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d6182-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="d6182-112">Si el dispositivo es compatible con esta característica, el subproceso de trabajo puede esperar la notificación.</span><span class="sxs-lookup"><span data-stu-id="d6182-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="d6182-113">Sin embargo, según la "Especificación de subunidad de grabadora de cintas AV/C" de la asociación comercial de 1394, el comando de notificación de estado de transporte es opcional, lo que significa que no es necesario que los dispositivos lo admitan.</span><span class="sxs-lookup"><span data-stu-id="d6182-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="d6182-114">Si un dispositivo no admite notificaciones, debe sondear el dispositivo a intervalos periódicos para su estado actual.</span><span class="sxs-lookup"><span data-stu-id="d6182-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="d6182-115">En esta sección se describe primero el mecanismo de notificación y, a continuación, se describe el sondeo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6182-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="d6182-116">Uso de la notificación de estado de transporte</span><span class="sxs-lookup"><span data-stu-id="d6182-116">Using Transport State Notification</span></span>

<span data-ttu-id="d6182-117">La notificación de estado de transporte funciona haciendo que el controlador señale un evento cuando el transporte cambia a un nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="d6182-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="d6182-118">En la aplicación, declare una sección crítica, un evento y un identificador de subproceso.</span><span class="sxs-lookup"><span data-stu-id="d6182-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="d6182-119">La sección crítica se usa para sincronizar el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6182-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="d6182-120">El evento se usa para detener el subproceso de trabajo cuando se cierra la aplicación:</span><span class="sxs-lookup"><span data-stu-id="d6182-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="d6182-121">Después de crear una instancia del filtro de captura, cree el subproceso de trabajo:</span><span class="sxs-lookup"><span data-stu-id="d6182-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="d6182-122">En el subproceso de trabajo, empiece por llamar al método [**IAMExtTransport:: getStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con el valor Ed \_ Notify \_ HEVENT \_ get.</span><span class="sxs-lookup"><span data-stu-id="d6182-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="d6182-123">Esta llamada devuelve un identificador a un evento que se señalará cuando se complete una operación:</span><span class="sxs-lookup"><span data-stu-id="d6182-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="d6182-124">A continuación, vuelva a llamar a **GetState** y pase el valor de la notificación de cambio de modo de Ed \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="d6182-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="d6182-125">Si el dispositivo admite la notificación, el método devuelve el valor E \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="d6182-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="d6182-126">(De lo contrario, debe sondear el dispositivo, como se describe en la sección siguiente). Suponiendo que el dispositivo admite la notificación, el evento se señalará cada vez que cambie el estado del transporte del VTR.</span><span class="sxs-lookup"><span data-stu-id="d6182-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="d6182-127">En este momento, puede actualizar la interfaz de usuario para que refleje el nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="d6182-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="d6182-128">Para obtener la notificación siguiente, restablezca el identificador de evento y **llame de nuevo a la** notificación de cambio de modo de la actualización del modo Ed \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d6182-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="d6182-129">Antes de que se cierre el subproceso de trabajo, libere el identificador de evento llamando a **getStatus** con la marca Ed \_ Notify \_ HEVENT \_ release y la dirección del identificador:</span><span class="sxs-lookup"><span data-stu-id="d6182-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="d6182-130">En el código siguiente se muestra el procedimiento de subproceso completo.</span><span class="sxs-lookup"><span data-stu-id="d6182-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="d6182-131">Se supone que la función UpdateTransportState es una función de aplicación que actualiza la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d6182-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="d6182-132">Tenga en cuenta que el subproceso espera dos eventos: el evento de notificación (*hNotify*) y el evento de terminación del subproceso (*hThreadEnd*).</span><span class="sxs-lookup"><span data-stu-id="d6182-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="d6182-133">Tenga en cuenta también dónde se usa la sección crítica para proteger la variable de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6182-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="d6182-134">Use también la sección crítica cuando emita comandos para el dispositivo, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d6182-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="d6182-135">Antes de que se cierre la aplicación, detenga el subproceso secundario estableciendo el evento de fin de subproceso:</span><span class="sxs-lookup"><span data-stu-id="d6182-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="d6182-136">Sondear el estado de transporte</span><span class="sxs-lookup"><span data-stu-id="d6182-136">Polling the Transport State</span></span>

<span data-ttu-id="d6182-137">Si llama a **IAMExtTransport:: getStatus** con la \_ marca de notificación de cambio de modo Ed \_ \_ y el valor devuelto no es E \_ pendiente, significa que el dispositivo no admite la notificación.</span><span class="sxs-lookup"><span data-stu-id="d6182-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="d6182-138">En ese caso, debe sondear el dispositivo para determinar su estado.</span><span class="sxs-lookup"><span data-stu-id="d6182-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="d6182-139">El *sondeo* simplemente significa llamar al **\_ modo Get** a intervalos regulares para comprobar el estado de transporte.</span><span class="sxs-lookup"><span data-stu-id="d6182-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="d6182-140">Todavía debería usar un subproceso secundario y una sección crítica, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6182-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="d6182-141">El subproceso consulta el estado del dispositivo en un intervalo normal.</span><span class="sxs-lookup"><span data-stu-id="d6182-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="d6182-142">En el ejemplo siguiente se muestra una manera de implementar el subproceso:</span><span class="sxs-lookup"><span data-stu-id="d6182-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="d6182-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6182-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6182-144">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="d6182-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



