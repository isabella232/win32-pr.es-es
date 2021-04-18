---
description: Generadores de eventos multimedia
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Generadores de eventos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721351"
---
# <a name="media-event-generators"></a><span data-ttu-id="a179d-103">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="a179d-103">Media Event Generators</span></span>

<span data-ttu-id="a179d-104">Media Foundation proporciona una manera coherente para que los objetos envíen eventos.</span><span class="sxs-lookup"><span data-stu-id="a179d-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="a179d-105">Un objeto puede utilizar eventos para indicar la finalización de un método asincrónico o para notificar a la aplicación sobre un cambio en el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="a179d-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="a179d-106">Si un objeto envía eventos, expone la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="a179d-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="a179d-107">Siempre que el objeto envía un nuevo evento, el evento se coloca en una cola.</span><span class="sxs-lookup"><span data-stu-id="a179d-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="a179d-108">La aplicación puede solicitar el siguiente evento de la cola mediante una llamada a uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a179d-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="a179d-109">**IMFMediaEventGenerator::GetEvent**</span><span class="sxs-lookup"><span data-stu-id="a179d-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="a179d-110">**IMFMediaEventGenerator::BeginGetEvent**</span><span class="sxs-lookup"><span data-stu-id="a179d-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="a179d-111">El método [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) es sincrónico.</span><span class="sxs-lookup"><span data-stu-id="a179d-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="a179d-112">Si un evento ya está en la cola, el método se devuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a179d-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="a179d-113">Si no hay ningún evento en la cola, el método produce un error inmediatamente o se bloquea hasta que se pone en cola el siguiente evento, en función de la marca que se pase a **GetEvent**.</span><span class="sxs-lookup"><span data-stu-id="a179d-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="a179d-114">El método [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) es asincrónico, por lo que nunca se bloquea.</span><span class="sxs-lookup"><span data-stu-id="a179d-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="a179d-115">Este método toma un puntero a la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que la aplicación debe implementar.</span><span class="sxs-lookup"><span data-stu-id="a179d-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="a179d-116">Cuando se invoca la devolución de llamada, la aplicación llama a [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obtener el evento de la cola.</span><span class="sxs-lookup"><span data-stu-id="a179d-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="a179d-117">Para obtener más información sobre **IMFAsyncCallback**, consulte [métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a179d-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="a179d-118">Los eventos se representan mediante la interfaz [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="a179d-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="a179d-119">Esta interfaz tiene los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a179d-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="a179d-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): recupera el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="a179d-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="a179d-121">El tipo de evento indica lo que ha sucedido para desencadenar el evento.</span><span class="sxs-lookup"><span data-stu-id="a179d-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="a179d-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): recupera un valor **HRESULT** , que indica si la operación que desencadenó el evento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a179d-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="a179d-123">Si se produce un error en una operación de forma asincrónica, **getStatus** devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="a179d-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="a179d-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): recupera un **PROPVARIANT** que contiene datos de evento.</span><span class="sxs-lookup"><span data-stu-id="a179d-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="a179d-125">Los datos del evento dependen del tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="a179d-125">The event data depends on the event type.</span></span> <span data-ttu-id="a179d-126">Algunos eventos no tienen datos.</span><span class="sxs-lookup"><span data-stu-id="a179d-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="a179d-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): recupera un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="a179d-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="a179d-128">Este método se aplica al [evento MEExtendedType](meextendedtype.md)y proporciona una manera de definir eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a179d-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="a179d-129">La interfaz [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) también hereda la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="a179d-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="a179d-130">Algunos eventos llevan información adicional como atributos.</span><span class="sxs-lookup"><span data-stu-id="a179d-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="a179d-131">Para obtener una lista de tipos de eventos y sus datos y atributos asociados, vea [eventos de Media Foundation](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="a179d-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="a179d-132">Implementación de IMFMediaEventGenerator</span><span class="sxs-lookup"><span data-stu-id="a179d-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="a179d-133">Si está escribiendo un componente de complemento para Media Foundation, como un origen de multimedia personalizado o un receptor de multimedia, puede que tenga que implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span><span class="sxs-lookup"><span data-stu-id="a179d-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="a179d-134">Para facilitar esta tarea, Media Foundation proporciona un objeto auxiliar que implementa una cola de eventos.</span><span class="sxs-lookup"><span data-stu-id="a179d-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="a179d-135">Cree la cola de eventos mediante una llamada a la función [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="a179d-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="a179d-136">La cola de eventos expone la interfaz [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="a179d-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="a179d-137">En la implementación del objeto de los métodos **IMFMediaEventGenerator** , llame al método correspondiente en la cola de eventos.</span><span class="sxs-lookup"><span data-stu-id="a179d-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="a179d-138">El objeto de cola de eventos es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a179d-138">The event queue object is thread safe.</span></span> <span data-ttu-id="a179d-139">Nunca conserve el mismo objeto de sección crítica al llamar a [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) y [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), ya que **GetEvent** podría bloquearse indefinidamente en espera de [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span><span class="sxs-lookup"><span data-stu-id="a179d-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="a179d-140">Si contiene la misma sección crítica para ambos métodos, se producirá un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="a179d-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="a179d-141">Antes de liberar la cola de eventos, llame a [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) para liberar los recursos que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="a179d-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="a179d-142">Cuando el objeto necesite generar un evento, llame a uno de los métodos siguientes en la cola de eventos:</span><span class="sxs-lookup"><span data-stu-id="a179d-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="a179d-143">**IMFMediaEventQueue::QueueEvent**</span><span class="sxs-lookup"><span data-stu-id="a179d-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="a179d-144">**IMFMediaEventQueue::QueueEventParamVar**</span><span class="sxs-lookup"><span data-stu-id="a179d-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="a179d-145">**IMFMediaEventQueue::QueueEventParamUnk**</span><span class="sxs-lookup"><span data-stu-id="a179d-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="a179d-146">Estos métodos colocan un nuevo evento en la cola y señalan cualquier llamador que esté esperando el siguiente evento.</span><span class="sxs-lookup"><span data-stu-id="a179d-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="a179d-147">En el código siguiente se muestra una clase que implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) con este objeto auxiliar.</span><span class="sxs-lookup"><span data-stu-id="a179d-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="a179d-148">Esta clase define un método de **cierre** público que cierra la cola de eventos y libera el puntero de cola de eventos.</span><span class="sxs-lookup"><span data-stu-id="a179d-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="a179d-149">Este comportamiento sería típico para los orígenes multimedia y los receptores multimedia, que siempre tienen un método **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="a179d-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="a179d-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a179d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a179d-151">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="a179d-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



