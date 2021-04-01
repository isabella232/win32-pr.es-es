---
description: En este tema se describe cómo reproducir un segmento de un archivo multimedia en MFPlay, estableciendo las horas de inicio y detención para la reproducción.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Cómo reproducir un clip de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908311"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="1e104-103">Cómo reproducir un clip de archivo</span><span class="sxs-lookup"><span data-stu-id="1e104-103">How to Play a File Clip</span></span>

<span data-ttu-id="1e104-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1e104-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e104-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1e104-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1e104-106">\]</span><span class="sxs-lookup"><span data-stu-id="1e104-106">\]</span></span>

<span data-ttu-id="1e104-107">En este tema se describe cómo reproducir un segmento de un archivo multimedia en MFPlay, estableciendo las horas de inicio y detención para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="1e104-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="1e104-108">**Para reproducir un clip de archivo**</span><span class="sxs-lookup"><span data-stu-id="1e104-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="1e104-109">Llame a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para crear un elemento multimedia para el archivo.</span><span class="sxs-lookup"><span data-stu-id="1e104-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="1e104-110">Opcionalmente, obtenga la duración total del archivo, como se describe en [Cómo obtener la duración de la reproducción](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="1e104-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="1e104-111">Llame a [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) para establecer las horas de inicio y detención.</span><span class="sxs-lookup"><span data-stu-id="1e104-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="1e104-112">La hora de detención no debe superar la duración del archivo.</span><span class="sxs-lookup"><span data-stu-id="1e104-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="1e104-113">Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="1e104-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="1e104-114">En el ejemplo siguiente se usa la versión de bloqueo de [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="1e104-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="1e104-115">Si se usa la versión que no es de bloqueo, el código que aparece después de **CreateMediaItemFromURL** debe colocarse en el controlador para el evento de **tipo de \_ evento MFP \_ \_ MEDIAITEM \_ creado** .</span><span class="sxs-lookup"><span data-stu-id="1e104-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="1e104-116">Para obtener más información sobre los eventos de MFPlay, consulte [recibir eventos del reproductor](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="1e104-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="1e104-117">Para obtener la duración del archivo, este ejemplo llama a la `GetPlaybackDuration` función que se muestra en el tema [Cómo obtener la duración de la reproducción](how-to-get-the-playback-duration.md).</span><span class="sxs-lookup"><span data-stu-id="1e104-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1e104-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e104-118">Requirements</span></span>

<span data-ttu-id="1e104-119">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e104-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e104-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e104-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e104-121">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="1e104-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



