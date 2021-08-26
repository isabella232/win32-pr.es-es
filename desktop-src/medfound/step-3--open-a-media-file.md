---
description: Este tema es el paso 3 del tutorial Cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Paso 3: Abrir un archivo multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c198b07358ebbf5d8da591d75d44f4687b600f6bb387c4f55901974397308dc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012370"
---
# <a name="step-3-open-a-media-file"></a>Paso 3: Abrir un archivo multimedia

Este tema es el paso 3 del tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md).

El `CPlayer::OpenURL` método abre un archivo multimedia desde una dirección URL.


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
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

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



Este método realiza los pasos siguientes:

1.  Llama **a CPlayer::CreateSession** para crear una nueva instancia de la sesión multimedia. Vea [Paso 4: Crear la sesión multimedia](step-4--create-the-media-session.md).
2.  Crea un origen multimedia a partir de la dirección URL. El código completo de este paso se muestra en el tema [Using the Source Resolver](using-the-source-resolver.md).
3.  Llama [**a IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obtener el descriptor de presentación del origen multimedia. El descriptor de presentación describe cada secuencia del archivo de origen.
4.  Crea la topología de reproducción. El código de este paso se muestra en el tema [Creación de topologías de reproducción.](creating-playback-topologies.md)
5.  Llama [**a IMFMediaSession::SetTopology para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) establecer la topología en la sesión multimedia.

El [**método SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se completa de forma asincrónica. Cuando se completa, se llama al método [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto CPlayer; vea [Paso 5: Controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).

Siguiente: [Paso 4: Crear la sesión multimedia](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



