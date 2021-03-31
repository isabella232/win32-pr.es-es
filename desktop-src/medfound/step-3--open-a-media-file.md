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
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="907dc-103">Paso 3: abrir un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="907dc-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="907dc-104">En este tema se describe el paso 3 del tutorial sobre [Cómo reproducir archivos multimedia con Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="907dc-105">El código completo se muestra en el tema [ejemplo de reproducción de sesión de medio](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="907dc-106">El `CPlayer::OpenURL` método abre un archivo multimedia desde una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="907dc-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


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



<span data-ttu-id="907dc-107">Este método realiza los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="907dc-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="907dc-108">Llama a **CPlayer:: createSession** para crear una nueva instancia de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="907dc-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="907dc-109">Consulte [paso 4: crear la sesión multimedia](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="907dc-110">Crea un origen multimedia a partir de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="907dc-110">Creates a media source from the URL.</span></span> <span data-ttu-id="907dc-111">El código completo de este paso se muestra en el tema [uso de la resolución de origen](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="907dc-112">Llama a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obtener el descriptor de presentación del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="907dc-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="907dc-113">El descriptor de presentación describe cada flujo del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="907dc-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="907dc-114">Crea la topología de reproducción.</span><span class="sxs-lookup"><span data-stu-id="907dc-114">Creates the playback topology.</span></span> <span data-ttu-id="907dc-115">El código de este paso se muestra en el tema [crear topologías de reproducción](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="907dc-116">Llama a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="907dc-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="907dc-117">El método [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="907dc-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="907dc-118">Cuando se completa, se llama al método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) del objeto CPlayer; vea [paso 5: controlar eventos de sesión multimedia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="907dc-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="907dc-119">Siguiente: [paso 4: crear la sesión multimedia](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="907dc-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="907dc-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="907dc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907dc-121">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="907dc-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="907dc-122">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="907dc-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



