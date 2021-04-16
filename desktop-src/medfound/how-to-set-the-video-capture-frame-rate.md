---
description: Un dispositivo de captura de vídeo puede admitir una variedad de velocidades de fotogramas.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Cómo establecer la velocidad de fotogramas de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705843"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Cómo establecer la velocidad de fotogramas de captura de vídeo

Un dispositivo de captura de vídeo puede admitir una variedad de velocidades de fotogramas. Si esta información está disponible, las velocidades de fotogramas mínimo y máximo se almacenan como atributos de tipo de medio:



| Atributo                                                         | Descripción         |
|-------------------------------------------------------------------|---------------------|
| [\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md) | Velocidad de fotogramas máxima. |
| [\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ mín.](mf-mt-frame-rate-range-min.md) | Velocidad de fotogramas mínima. |



 

El intervalo puede variar en función del formato de captura. Por ejemplo, en tamaños de fotogramas mayores, se podría reducir la velocidad máxima de fotogramas.

Para establecer la velocidad de fotogramas:

1.  Cree el origen de medios para el dispositivo de captura. Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen de medios para obtener el descriptor de presentación.
3.  Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de flujo para la secuencia de vídeo.
4.  Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo.
5.  Enumerar los formatos de captura, tal y como se describe en [cómo establecer el formato de captura de vídeo](how-to-set-the-video-capture-format.md).
6.  Seleccione el formato de salida deseado en la lista.
7.  Consulte el tipo de medio para los atributos de intervalo de velocidad de fotogramas [MF \_ MT \_ \_ \_ \_ Max](mf-mt-frame-rate-range-max.md) y [MF \_ MT \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md) . Estos valores proporcionan el intervalo de velocidades de fotogramas admitidas. Es posible que el dispositivo admita otras velocidades de fotogramas dentro de este intervalo.
8.  Establezca el atributo [**MF \_ MT \_ Frame**](mf-mt-frame-rate-attribute.md) en el tipo de medio para especificar la velocidad de fotogramas deseada.
9.  Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) con el tipo de medio modificado.

En el ejemplo siguiente se establece la velocidad de fotogramas igual a la velocidad de fotogramas máxima que admite el dispositivo:


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



