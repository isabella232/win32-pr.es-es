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
# <a name="how-to-play-a-file-clip"></a>Cómo reproducir un clip de archivo

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo reproducir un segmento de un archivo multimedia en MFPlay, estableciendo las horas de inicio y detención para la reproducción.

**Para reproducir un clip de archivo**

1.  Llame a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para crear un elemento multimedia para el archivo.
2.  Opcionalmente, obtenga la duración total del archivo, como se describe en [Cómo obtener la duración de la reproducción](how-to-get-the-playback-duration.md).
3.  Llame a [**IMFPMediaItem:: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) para establecer las horas de inicio y detención. La hora de detención no debe superar la duración del archivo.
4.  Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para iniciar la reproducción.

En el ejemplo siguiente se usa la versión de bloqueo de [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl). Si se usa la versión que no es de bloqueo, el código que aparece después de **CreateMediaItemFromURL** debe colocarse en el controlador para el evento de **tipo de \_ evento MFP \_ \_ MEDIAITEM \_ creado** . Para obtener más información sobre los eventos de MFPlay, consulte [recibir eventos del reproductor](getting-started-with-mfplay.md).

Para obtener la duración del archivo, este ejemplo llama a la `GetPlaybackDuration` función que se muestra en el tema [Cómo obtener la duración de la reproducción](how-to-get-the-playback-duration.md).


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



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



