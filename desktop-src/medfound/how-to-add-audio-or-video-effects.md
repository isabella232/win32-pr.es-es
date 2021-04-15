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
# <a name="how-to-add-audio-or-video-effects"></a>Cómo agregar efectos de audio o vídeo

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo usar efectos de audio y vídeo con MFPlay.

Para usar un efecto con MFPlay, el efecto debe implementarse como una transformación de Media Foundation (MFT). Para obtener más información, vea [transformaciones de Media Foundation](media-foundation-transforms.md).

**Para agregar un efecto de audio o vídeo**

1.  Cree una instancia de la MFT que implementa el efecto.
2.  Llame a [**IMFPMediaPlayer:: InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).

Llame a [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) antes de abrir el archivo multimedia para la reproducción. MFPlay determina automáticamente si el efecto es un efecto de vídeo o de audio.

El método [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) también toma un parámetro booleano que especifica si el efecto es opcional o obligatorio. Si MFPlay no puede Agregar un efecto necesario (por ejemplo, porque el formato del flujo es incompatible), se produce un error de reproducción. En la mayoría de los casos, es mejor establecer un efecto como opcional.

MFPlay continúa usando el efecto para toda la reproducción posterior. Para quitar el efecto, llame a [**IMFPMediaPlayer:: RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) o [**IMFPMediaPlayer:: RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).


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



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



