---
description: Este tema es el paso 7 del tutorial Cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Paso 7: Apagar la sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1eec6e798ee260c83fc1532c2012aed8a53625b12195848ac00fcdcf8fae3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721955"
---
# <a name="step-7-shut-down-the-media-session"></a>Paso 7: Apagar la sesión multimedia

Este tema es el paso 7 del tutorial [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md).

Para apagar la sesión [multimedia,](media-session.md)realice los pasos siguientes:

1.  Llame [**a IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la presentación actual.
2.  Espere al [evento MESessionClosed.](mesessionclosed.md) Se garantiza que este evento es el último de la sesión multimedia.
3.  Llame [**a IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Este método hace que las sesiones multimedia liberen recursos.
4.  Llame [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen de medios actual.

El método siguiente cierra la sesión multimedia. Usa un identificador de evento (*m \_ hCloseEvent*) para esperar al [evento MESessionClosed.](mesessionclosed.md) Vea [Paso 5: Controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



Antes de que se cierre la aplicación, apague la sesión multimedia y, a continuación, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para apagar la plataforma Microsoft Media Foundation dispositivo.


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



