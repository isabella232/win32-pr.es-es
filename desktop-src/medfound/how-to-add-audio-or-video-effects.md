---
description: En este tema se describe cómo usar efectos de audio y vídeo con MFPlay.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Cómo agregar efectos de audio o vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715893"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="a2f2d-103">Cómo agregar efectos de audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="a2f2d-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="a2f2d-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2f2d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a2f2d-106">\]</span><span class="sxs-lookup"><span data-stu-id="a2f2d-106">\]</span></span>

<span data-ttu-id="a2f2d-107">En este tema se describe cómo usar efectos de audio y vídeo con MFPlay.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="a2f2d-108">Para usar un efecto con MFPlay, el efecto debe implementarse como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="a2f2d-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="a2f2d-109">Para obtener más información, vea [transformaciones de Media Foundation](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="a2f2d-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="a2f2d-110">**Para agregar un efecto de audio o vídeo**</span><span class="sxs-lookup"><span data-stu-id="a2f2d-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="a2f2d-111">Cree una instancia de la MFT que implementa el efecto.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="a2f2d-112">Llame a [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span><span class="sxs-lookup"><span data-stu-id="a2f2d-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="a2f2d-113">Llame a [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) antes de abrir el archivo multimedia para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="a2f2d-114">MFPlay determina automáticamente si el efecto es un efecto de vídeo o de audio.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="a2f2d-115">El método [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) también toma un parámetro booleano que especifica si el efecto es opcional o obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="a2f2d-116">Si MFPlay no puede Agregar un efecto necesario (por ejemplo, porque el formato del flujo es incompatible), se produce un error de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="a2f2d-117">En la mayoría de los casos, es mejor establecer un efecto como opcional.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="a2f2d-118">MFPlay continúa usando el efecto para toda la reproducción posterior.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="a2f2d-119">Para quitar el efecto, llame a [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) o [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span><span class="sxs-lookup"><span data-stu-id="a2f2d-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a2f2d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2f2d-120">Requirements</span></span>

<span data-ttu-id="a2f2d-121">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a2f2d-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f2d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2f2d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f2d-123">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="a2f2d-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



