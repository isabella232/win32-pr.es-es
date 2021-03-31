---
description: En este tema se describe el paso 3 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Paso 3: abrir un archivo multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104083572"
---
# <a name="step-3-open-a-media-file"></a>Paso 3: abrir un archivo multimedia

En este tema se describe el paso 3 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).

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

1.  Llama a **CPlayer:: createSession** para crear una nueva instancia de la sesión multimedia. Consulte [paso 4: crear la sesión multimedia](step-4--create-the-media-session.md).
2.  Crea un origen multimedia a partir de la dirección URL. El código completo de este paso se muestra en el tema [uso de la resolución de origen](using-the-source-resolver.md).
3.  Llama a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obtener el descriptor de presentación del origen multimedia. El descriptor de presentación describe cada flujo del archivo de código fuente.
4.  Crea la topología de reproducción. El código de este paso se muestra en el tema [crear topologías de reproducción](creating-playback-topologies.md).
5.  Llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.

El método [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se completa de forma asincrónica. Cuando se completa, se llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto CPlayer; vea [paso 5: controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).

Siguiente: [paso 4: crear la sesión multimedia](step-4--create-the-media-session.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



