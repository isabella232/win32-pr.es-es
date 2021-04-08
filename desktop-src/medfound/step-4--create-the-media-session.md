---
description: En este tema se describe el paso 4 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Paso 4: crear la sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003438"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="5fc58-103">Paso 4: crear la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="5fc58-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="5fc58-104">En este tema se describe el paso 4 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="5fc58-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="5fc58-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="5fc58-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="5fc58-106">`CPlayer::CreateSession`Crea una nueva instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="5fc58-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


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



<span data-ttu-id="5fc58-107">Este método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5fc58-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="5fc58-108">Llama `CPlayer::CloseSession` a para cerrar cualquier instancia anterior de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="5fc58-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="5fc58-109">Llama a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear una nueva instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="5fc58-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="5fc58-110">Llama al método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) para solicitar el siguiente evento de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="5fc58-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="5fc58-111">El primer parámetro de **BeginGetEvent** es un puntero al propio objeto **CPlayer** , que implents la interfaz [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="5fc58-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="5fc58-112">El control de eventos se describe en el paso 5.</span><span class="sxs-lookup"><span data-stu-id="5fc58-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="5fc58-113">Siguiente: [paso 5: controlar los eventos de la sesión multimedia](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="5fc58-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fc58-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5fc58-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fc58-115">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="5fc58-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="5fc58-116">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fc58-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



