---
description: Cómo buscar la duración de un archivo multimedia.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Cómo buscar la duración de un archivo multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547363"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Cómo buscar la duración de un archivo multimedia

Para buscar la duración de un archivo multimedia, realice los pasos siguientes:

1.  Utilice el [solucionador de origen](source-resolver.md) para crear un origen de medios que pueda analizar el archivo multimedia.
2.  Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen del medio. Este método devuelve el descriptor de presentación que describe el contenido del archivo multimedia.
3.  Consulte en el descriptor de presentación el atributo de [ \_ \_ duración MF PD](mf-pd-duration-attribute.md) llamando al método [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) . El valor del atributo, si está presente, es la duración del archivo en unidades de 100-nanosegundos.


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

 

 



