---
description: En este tema se describe cómo obtener la duración de reproducción de un archivo multimedia mediante MFPlay.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: Cómo obtener la duración de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c715ae82c63006ef8ad375fa9624cbd65ee5516be2d3e3379e5ca58a2fb5166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958354"
---
# <a name="how-to-get-the-playback-duration"></a>Cómo obtener la duración de reproducción

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo obtener la duración de reproducción de un archivo multimedia mediante MFPlay.

**Para obtener la duración de reproducción**

1.  Llame [**a IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**APTPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para crear un elemento multimedia para el archivo.
2.  Llame [**a IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration). Especifique **MFP \_ POSITIONTYPE \_ 100NS para** el primer parámetro. La duración se devuelve como **PROPVARIANT** que contiene un **valor LARGE \_ INTEGER.** La duración se da en unidades de 100 nanosegundos.

En el ejemplo siguiente se muestra el paso 2:


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



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



