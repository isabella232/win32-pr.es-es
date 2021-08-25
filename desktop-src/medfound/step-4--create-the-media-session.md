---
description: Este tema es el paso 4 del tutorial Cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Paso 4: Crear la sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9c31d4c5e07abe8f088aad38fec9f91046a7d4338905dbd917de9d414fd4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847775"
---
# <a name="step-4-create-the-media-session"></a>Paso 4: Crear la sesión multimedia

Este tema es el paso 4 del tutorial [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md). El código completo se muestra en el tema [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md).

crea `CPlayer::CreateSession` una nueva instancia de la sesión multimedia.


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



Este método realiza los pasos siguientes:

1.  Llama `CPlayer::CloseSession` a para cerrar cualquier instancia anterior de la sesión multimedia.
2.  Llama [**a MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear una nueva instancia de la sesión multimedia.
3.  Llama al [**método IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar el siguiente evento de la sesión multimedia. El primer parámetro de **BeginGetEvent es** un puntero al propio objeto **CPlayer,** que implenta la [**interfaz DE DEVOLUCIÓNASYNCAsync.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)

El control de eventos se describe en el paso 5.

Siguiente: [Paso 5: Controlar eventos de sesión multimedia](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> <dt>

[Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



