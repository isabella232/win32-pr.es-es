---
description: Cómo buscar la duración de un archivo multimedia.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Cómo buscar la duración de un archivo multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1885d356be54875079341eabc7433c9753792daf01c4848a00ee4ed4fbb343ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878849"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Cómo buscar la duración de un archivo multimedia

Para buscar la duración de un archivo multimedia, realice los pasos siguientes:

1.  Use el [Solucionador de origen](source-resolver.md) para crear un origen multimedia que pueda analizar el archivo multimedia.
2.  Llame [**a IMFMediaSource::CreatePresentationDescriptor en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) el origen multimedia. Este método devuelve el descriptor de presentación que describe el contenido del archivo multimedia.
3.  Consulte el descriptor de presentación para el atributo [MF \_ PD \_ DURATION](mf-pd-duration-attribute.md) llamando al [**métodoATTRIBUTEAttributes::GetUINT64.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) El valor del atributo, si está presente, es la duración del archivo en unidades de 100 nanosegundos.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 



