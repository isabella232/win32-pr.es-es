---
description: Un dispositivo de captura de vídeo puede admitir varios formatos de captura. Los formatos normalmente se diferencian por el tipo de compresión, el espacio de colores (YUV o RGB), el tamaño de marco o la velocidad de fotogramas.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Cómo establecer el formato de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706213"
---
# <a name="how-to-set-the-video-capture-format"></a>Cómo establecer el formato de captura de vídeo

Un dispositivo de captura de vídeo puede admitir varios formatos de captura. Los formatos normalmente se diferencian por el tipo de compresión, el espacio de colores (YUV o RGB), el tamaño de marco o la velocidad de fotogramas.

La lista de formatos admitidos se encuentra en el *descriptor de presentación*. Para obtener más información, vea [descriptores de presentación](presentation-descriptors.md).

Para enumerar los formatos admitidos:

1.  Cree el origen de medios para el dispositivo de captura. Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) en el origen de medios para obtener el descriptor de presentación.
3.  Llame a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de flujo para la secuencia de vídeo.
4.  Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) en el descriptor de flujo.
5.  Llame a [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) para obtener el número de formatos admitidos.
6.  En un bucle, llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obtener cada formato. El formato se representa mediante un *tipo de medio*. Para obtener más información, consulte [tipos de medios de vídeo](video-media-types.md).

En el ejemplo siguiente se enumeran los formatos de captura para un dispositivo:


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



La `LogMediaType` función que se usa en este ejemplo se muestra en el tema [código de depuración de tipo de medio](media-type-debugging-code.md).

Para establecer el formato de captura:

1.  Obtiene un puntero a la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , tal como se muestra en el ejemplo anterior.
2.  Llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obtener el formato deseado, especificado por el índice.
3.  Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para establecer el formato.

Si no establece el formato de captura, el dispositivo usará su formato predeterminado.

En el ejemplo siguiente se establece el formato de captura:


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



El orden en el que se devuelven los formatos depende del dispositivo. Normalmente, se agrupan primero por tipo de compresión o espacio de colores; y, después, desde el tamaño de fotograma más pequeño hasta el tamaño de fotograma más grande dentro de cada grupo.

La velocidad de fotogramas se controla de forma ligeramente diferente a los demás atributos de formato. Para obtener más información, vea [cómo establecer la velocidad de fotogramas de captura de vídeo](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> En algunos dispositivos, la lista de formatos contendrá una entrada duplicada para cada formato. Por ejemplo, si el dispositivo admite 15 formatos de captura distintos, la lista contendrá 30 entradas. Dentro de cada par, uno de los tipos de medios tendrá el [**atributo \_ MF \_ MT \_ AM format \_ Type**](mf-mt-am-format-type-attribute.md) igual a **format \_ info** y el otro tendrá el **\_ \_ \_ \_ tipo de formato MF MT AM** igual al **formato \_ VideoInfo2**. (Estos dos valores se definen en el archivo de encabezado UUID. h). El segundo tipo también puede contener información de color adicional ([información de color ampliada](extended-color-information.md)) o mostrar un valor diferente para el entrelazado ([**\_ \_ \_ modo de entrelazado MF MT**](mf-mt-interlace-mode-attribute.md)). Estos tipos duplicados existen para admitir aplicaciones de DirectShow anteriores. En una aplicación Media Foundation, debe omitir el **formato \_ videoinfo** Type cada vez que se muestre un tipo de **formato \_ VideoInfo2** duplicado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



