---
description: Este tema es el paso 5 del tutorial Cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Paso 5: Controlar eventos de sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be80d8d336cb5f3996c72d806259ae8c74eed464245ac439fdd356f091965bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721905"
---
# <a name="step-5-handle-media-session-events"></a>Paso 5: Controlar eventos de sesión multimedia

Este tema es el paso 5 del tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md).

Para obtener información general sobre este tema, lea [Generadores de eventos multimedia](media-event-generators.md). Este tema contiene las siguientes secciones:

-   [Obtener eventos de sesión](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [Temas relacionados](#related-topics)

## <a name="getting-session-events"></a>Obtener eventos de sesión

Para obtener eventos de la sesión multimedia, el objeto CPlayer llama al método [**IMFMediaEventGenerator::BeginGetEvent,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) como se muestra en [Paso 4:](step-4--create-the-media-session.md)Crear la sesión multimedia . Este método es asincrónico, lo que significa que vuelve al autor de la llamada inmediatamente. Cuando se produce el siguiente evento de sesión, la sesión multimedia llama al método [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto CPlayer.

Es importante recordar que se llama a [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) desde un subproceso de trabajo, no desde el subproceso de aplicación. Por lo tanto, la implementación **de Invoke** debe ser segura para multiproceso. Un enfoque sería proteger los datos de miembro con una sección crítica. Sin embargo, `CPlayer` la clase muestra un enfoque alternativo:

1.  En el [**método Invoke,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) el objeto CPlayer envía un mensaje **WM APP PLAYER \_ \_ \_ EVENT** a la aplicación. El parámetro message es un [**puntero IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
2.  La aplicación recibe el mensaje **\_ WM APP PLAYER \_ \_ EVENT.**
3.  La aplicación llama al `CPlayer::HandleEvent` método y pasa el puntero [**IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
4.  El `HandleEvent` método responde al evento .

El código siguiente muestra el [**método Invoke:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)


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



El [**método Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) realiza los pasos siguientes:

1.  Llame [**a IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obtener el evento. Este método devuelve un puntero a la [**interfaz IMFMediaEvent.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
2.  Llame [**a IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) para obtener el código de evento.
3.  Si el código de evento [es MESessionClosed,](mesessionclosed.md)llame a SetEvent para establecer el *evento m \_ hCloseEvent.* El motivo de este paso se explica en [Paso 7: Apagar](step-7--shut-down-the-media-session.md)la sesión multimedia y también en los comentarios de código.
4.  Para todos los demás códigos de evento, llame [**a IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar el evento siguiente.
5.  Publique un **mensaje DE EVENTO DE WM APP \_ \_ PLAYER \_** en la ventana.

El código siguiente muestra el método HandleEvent, al que se llama cuando la aplicación recibe el **mensaje WM APP PLAYER \_ \_ \_ EVENT:**


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



Este método llama [**a IMFMediaEvent::GetType para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) obtener el tipo de evento [**y IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obtener el código de error correcto asociado al evento. La siguiente acción realizada depende del código del evento.

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

El [evento MESessionTopologyStatus](mesessiontopologystatus.md) indica un cambio en el estado de la topología. El [**atributo MF EVENT \_ \_ TOPOLOGY \_ STATUS**](mf-event-topology-status-attribute.md) del objeto de evento contiene el estado. En este ejemplo, el único valor de interés es **MF \_ TOPOSTATUS \_ READY,** que indica que la reproducción está lista para iniciarse.


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



El `CPlayer::StartPlayback` método se muestra en Paso [6: Controlar la reproducción.](step-6--control-playback.md)

En este ejemplo también se [**llama a MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) del [representador de](enhanced-video-renderer.md) vídeo mejorado (EVR). Esta interfaz es necesaria para controlar el repintado y el tamaño de la ventana de vídeo, que también se muestra en [Paso 6: Controlar la reproducción](step-6--control-playback.md).

## <a name="meendofpresentation"></a>MEEndOfPresentation

El [evento MEEndOfPresentation](meendofpresentation.md) indica que la reproducción ha llegado al final del archivo. La sesión multimedia vuelve automáticamente al estado detenido.


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

El [evento MENewPresentation](menewpresentation.md) indica el inicio de una nueva presentación. Los datos del evento son [**un puntero DEDESCRIPTOR DE LA CLASE PARA**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) LA NUEVA PRESENTACIÓN.

En muchos casos, no recibirá este evento en absoluto. Si lo hace, use el puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) para crear una nueva topología de reproducción, como se muestra en Paso [3:](step-3--open-a-media-file.md)Abrir un archivo multimedia . A continuación, poner en cola la nueva topología en la sesión multimedia.


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



Siguiente: [Paso 6: Controlar la reproducción](step-6--control-playback.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



