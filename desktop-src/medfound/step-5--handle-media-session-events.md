---
description: En este tema se describe el paso 5 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Paso 5: controlar los eventos de la sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717399"
---
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="c3090-103">Paso 5: controlar los eventos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="c3090-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="c3090-104">En este tema se describe el paso 5 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="c3090-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="c3090-106">Para obtener información sobre este tema, lea [generadores de eventos multimedia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="c3090-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="c3090-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c3090-108">Obtención de eventos de sesión</span><span class="sxs-lookup"><span data-stu-id="c3090-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="c3090-109">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="c3090-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="c3090-110">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="c3090-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="c3090-111">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="c3090-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="c3090-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3090-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="c3090-113">Obtención de eventos de sesión</span><span class="sxs-lookup"><span data-stu-id="c3090-113">Getting Session Events</span></span>

<span data-ttu-id="c3090-114">Para obtener los eventos de la sesión multimedia, el objeto CPlayer llama al método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , como se muestra en [el paso 4: crear la sesión multimedia](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="c3090-115">Este método es asincrónico, lo que significa que vuelve inmediatamente al llamador.</span><span class="sxs-lookup"><span data-stu-id="c3090-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="c3090-116">Cuando se produce el siguiente evento de sesión, la sesión multimedia llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto CPlayer.</span><span class="sxs-lookup"><span data-stu-id="c3090-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="c3090-117">Es importante recordar que se llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde un subproceso de trabajo, no desde el subproceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3090-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="c3090-118">Por lo tanto, la implementación de **Invoke** debe ser segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3090-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="c3090-119">Un enfoque sería proteger los datos de miembro con una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="c3090-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="c3090-120">Sin embargo, la `CPlayer` clase muestra un enfoque alternativo:</span><span class="sxs-lookup"><span data-stu-id="c3090-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="c3090-121">En el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , el objeto CPlayer envía un mensaje de evento de reproductor de aplicaciones de **WM \_ \_ \_** a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3090-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="c3090-122">El parámetro Message es un puntero [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="c3090-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="c3090-123">La aplicación recibe el mensaje de **evento de reproductor de aplicación de WM \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="c3090-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="c3090-124">La aplicación llama al `CPlayer::HandleEvent` método, pasando el puntero [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="c3090-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="c3090-125">El `HandleEvent` método responde al evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="c3090-126">En el código siguiente se muestra el método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="c3090-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



<span data-ttu-id="c3090-127">El método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) realiza los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="c3090-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="c3090-128">Llame a [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obtener el evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="c3090-129">Este método devuelve un puntero a la interfaz [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="c3090-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="c3090-130">Llame a [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obtener el código de evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="c3090-131">Si el código de evento es [MESessionClosed](mesessionclosed.md), llame a SetEvent para establecer el evento *m \_ hCloseEvent* .</span><span class="sxs-lookup"><span data-stu-id="c3090-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="c3090-132">El motivo de este paso se explica en el [paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md)y también en los comentarios del código.</span><span class="sxs-lookup"><span data-stu-id="c3090-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="c3090-133">Para todos los demás códigos de evento, llame a [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar el evento siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3090-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="c3090-134">Publicar un mensaje de evento de reproductor de aplicaciones de WM en la ventana. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3090-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="c3090-135">En el código siguiente se muestra el método HandleEvent, al que se llama cuando la aplicación recibe el mensaje de **evento de reproductor de aplicaciones de WM \_ \_ \_** :</span><span class="sxs-lookup"><span data-stu-id="c3090-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



<span data-ttu-id="c3090-136">Este método llama a [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obtener el tipo de evento y [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obtener el código de error correcto asociado al evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="c3090-137">La siguiente acción realizada depende del código de evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="c3090-138">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="c3090-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="c3090-139">El evento [MESessionTopologyStatus](mesessiontopologystatus.md) señala un cambio en el estado de la topología.</span><span class="sxs-lookup"><span data-stu-id="c3090-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="c3090-140">El atributo de estado de la [**\_ topología de eventos \_ \_ MF**](mf-event-topology-status-attribute.md) del objeto de evento contiene el estado.</span><span class="sxs-lookup"><span data-stu-id="c3090-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="c3090-141">En este ejemplo, el único valor de interés es **MF \_ TOPOSTATUS \_ Ready**, que indica que la reproducción está lista para iniciarse.</span><span class="sxs-lookup"><span data-stu-id="c3090-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



<span data-ttu-id="c3090-142">El `CPlayer::StartPlayback` método se muestra en el [paso 6: controlar la reproducción](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="c3090-143">En este ejemplo también se llama a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) del [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="c3090-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="c3090-144">Esta interfaz es necesaria para controlar la repintado y el cambio de tamaño de la ventana de vídeo, que también se muestra en el [paso 6: controlar la reproducción](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="c3090-145">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="c3090-145">MEEndOfPresentation</span></span>

<span data-ttu-id="c3090-146">El evento [MEEndOfPresentation](meendofpresentation.md) señala que la reproducción ha alcanzado el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="c3090-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="c3090-147">La sesión de medios vuelve a cambiar automáticamente al estado detenido.</span><span class="sxs-lookup"><span data-stu-id="c3090-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="c3090-148">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="c3090-148">MENewPresentation</span></span>

<span data-ttu-id="c3090-149">El evento [MENewPresentation](menewpresentation.md) señala el inicio de una nueva presentación.</span><span class="sxs-lookup"><span data-stu-id="c3090-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="c3090-150">Los datos de evento son un puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para la nueva presentación.</span><span class="sxs-lookup"><span data-stu-id="c3090-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="c3090-151">En muchos casos, no recibirá este evento.</span><span class="sxs-lookup"><span data-stu-id="c3090-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="c3090-152">Si lo hace, use el puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para crear una nueva topología de reproducción, como se muestra en el [paso 3: abrir un archivo multimedia](step-3--open-a-media-file.md).</span><span class="sxs-lookup"><span data-stu-id="c3090-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="c3090-153">A continuación, poner en cola la nueva topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="c3090-153">Then queue the new topology on the Media Session.</span></span>


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



<span data-ttu-id="c3090-154">Siguiente: [paso 6: controlar la reproducción](step-6--control-playback.md)</span><span class="sxs-lookup"><span data-stu-id="c3090-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3090-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3090-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3090-156">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="c3090-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="c3090-157">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3090-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



