---
description: En este tema se describe cómo obtener la duración de la reproducción de un archivo multimedia mediante MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Cómo obtener la duración de la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652499"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="350a4-103">Cómo obtener la duración de la reproducción</span><span class="sxs-lookup"><span data-stu-id="350a4-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="350a4-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="350a4-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="350a4-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="350a4-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="350a4-106">\]</span><span class="sxs-lookup"><span data-stu-id="350a4-106">\]</span></span>

<span data-ttu-id="350a4-107">En este tema se describe cómo obtener la duración de la reproducción de un archivo multimedia mediante MFPlay.</span><span class="sxs-lookup"><span data-stu-id="350a4-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="350a4-108">**Para obtener la duración de la reproducción**</span><span class="sxs-lookup"><span data-stu-id="350a4-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="350a4-109">Llame a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para crear un elemento multimedia para el archivo.</span><span class="sxs-lookup"><span data-stu-id="350a4-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="350a4-110">Llame a [**IMFPMediaItem:: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span><span class="sxs-lookup"><span data-stu-id="350a4-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="350a4-111">Especifique **MFP \_ POSITIONTYPE de \_ 100 NS** para el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="350a4-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="350a4-112">La duración se devuelve como un **PROPVARIANT** que contiene un **valor \_ entero grande** .</span><span class="sxs-lookup"><span data-stu-id="350a4-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="350a4-113">La duración se proporciona en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="350a4-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="350a4-114">En el ejemplo siguiente se muestra el paso 2:</span><span class="sxs-lookup"><span data-stu-id="350a4-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="350a4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="350a4-115">Requirements</span></span>

<span data-ttu-id="350a4-116">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="350a4-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="350a4-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="350a4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350a4-118">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="350a4-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



