---
description: Este tema es el paso 7 del tutorial sobre cómo reproducir archivos multimedia con Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Paso 7: apagar la sesión multimedia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157033"
---
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="14caa-103">Paso 7: apagar la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="14caa-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="14caa-104">Este tema es el paso 7 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="14caa-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="14caa-106">Para cerrar la [sesión multimedia](media-session.md), realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="14caa-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="14caa-107">Llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="14caa-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="14caa-108">Espere el evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="14caa-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="14caa-109">Se garantiza que este evento es el último evento de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="14caa-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="14caa-110">Llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="14caa-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="14caa-111">Este método hace que las sesiones multimedia liberen recursos.</span><span class="sxs-lookup"><span data-stu-id="14caa-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="14caa-112">Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="14caa-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="14caa-113">El método siguiente cierra la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="14caa-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="14caa-114">Usa un identificador de evento (*m \_ hCloseEvent*) para esperar el evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="14caa-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="14caa-115">Vea [paso 5: controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


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



<span data-ttu-id="14caa-116">Antes de salir de la aplicación, apague la sesión multimedia y, a continuación, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar la plataforma Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="14caa-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="14caa-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14caa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14caa-118">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="14caa-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="14caa-119">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14caa-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



