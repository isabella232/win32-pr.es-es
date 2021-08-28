---
description: Un dispositivo de captura de vídeo podría admitir una variedad de velocidades de fotogramas.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Cómo establecer la velocidad de fotogramas de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0e80c26c5a53a89cbc87ca509f25db1ebccf4571b4dda2e83ea63717c7d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827975"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Cómo establecer la velocidad de fotogramas de captura de vídeo

Un dispositivo de captura de vídeo podría admitir una variedad de velocidades de fotogramas. Si esta información está disponible, las velocidades de fotogramas mínimas y máximas se almacenan como atributos de tipo multimedia:



| Atributo                                                         | Descripción         |
|-------------------------------------------------------------------|---------------------|
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md) | Velocidad máxima de fotogramas. |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md) | Velocidad mínima de fotogramas. |



 

El intervalo puede variar en función del formato de captura. Por ejemplo, en tamaños de fotograma más grandes, se puede reducir la velocidad máxima de fotogramas.

Para establecer la velocidad de fotogramas:

1.  Cree el origen multimedia para el dispositivo de captura. Consulte [Enumeración de dispositivos de captura de vídeo.](enumerating-video-capture-devices.md)
2.  Llame [**a IMFMediaSource::CreatePresentationDescriptor en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) el origen multimedia para obtener el descriptor de presentación.
3.  Llame [**a IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de secuencia de la secuencia de vídeo.
4.  Llame [**a IMFStreamDescriptor::GetMediaTypeHandler en**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) el descriptor de secuencia.
5.  Enumere los formatos de captura, como se describe [en Cómo establecer el formato de captura de vídeo](how-to-set-the-video-capture-format.md).
6.  Seleccione el formato de salida deseado de la lista.
7.  Consulte el tipo de medio para los atributos [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MAX](mf-mt-frame-rate-range-max.md) y [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MIN.](mf-mt-frame-rate-range-min.md) Estos valores dan al intervalo de velocidades de fotogramas admitidas. El dispositivo podría admitir otras velocidades de fotogramas dentro de este intervalo.
8.  Establezca el [**atributo MF \_ MT \_ FRAME**](mf-mt-frame-rate-attribute.md) en el tipo de medio para especificar la velocidad de fotogramas deseada.
9.  Llame [**a IMFMediaTypeHandler::SetCurrentMediaType con**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) el tipo de medio modificado.

En el ejemplo siguiente se establece la velocidad de fotogramas igual a la velocidad máxima de fotogramas que admite el dispositivo:


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

 

 



