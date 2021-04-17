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
# <a name="how-to-get-the-playback-duration"></a>Cómo obtener la duración de la reproducción

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo obtener la duración de la reproducción de un archivo multimedia mediante MFPlay.

**Para obtener la duración de la reproducción**

1.  Llame a [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) o [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) para crear un elemento multimedia para el archivo.
2.  Llame a [**IMFPMediaItem:: GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration). Especifique **MFP \_ POSITIONTYPE de \_ 100 NS** para el primer parámetro. La duración se devuelve como un **PROPVARIANT** que contiene un **valor \_ entero grande** . La duración se proporciona en unidades de 100-nanosegundos.

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

 

 



