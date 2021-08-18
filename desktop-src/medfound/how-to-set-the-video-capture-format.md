---
description: Un dispositivo de captura de vídeo puede admitir varios formatos de captura. Los formatos suelen diferir según el tipo de compresión, el espacio de color (YUV o RGB), el tamaño del fotograma o la velocidad de fotogramas.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Cómo establecer el formato de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0968560772345bea91f5acfb79e7157a6376f388a5c0065634a273196b7552cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974404"
---
# <a name="how-to-set-the-video-capture-format"></a>Cómo establecer el formato de captura de vídeo

Un dispositivo de captura de vídeo puede admitir varios formatos de captura. Los formatos suelen diferir según el tipo de compresión, el espacio de color (YUV o RGB), el tamaño del fotograma o la velocidad de fotogramas.

La lista de formatos admitidos se encuentra en el *descriptor de presentación*. Para obtener más información, vea [Descriptores de presentación](presentation-descriptors.md).

Para enumerar los formatos admitidos:

1.  Cree el origen multimedia para el dispositivo de captura. Consulte [Enumeración de dispositivos de captura de vídeo.](enumerating-video-capture-devices.md)
2.  Llame [**a IMFMediaSource::CreatePresentationDescriptor en**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) el origen multimedia para obtener el descriptor de presentación.
3.  Llame [**a IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obtener el descriptor de secuencia de la secuencia de vídeo.
4.  Llame [**a IMFStreamDescriptor::GetMediaTypeHandler en**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) el descriptor de secuencia.
5.  Llame [**a IMFMediaTypeHandler::GetMediaTypeCount para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) obtener el número de formatos admitidos.
6.  En un bucle, llame [**a IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obtener cada formato. El formato se representa mediante un *tipo de medio*. Para obtener más información, vea [Tipos de medios de vídeo.](video-media-types.md)

En el ejemplo siguiente se enumeran los formatos de captura de un dispositivo:


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



La `LogMediaType` función utilizada en este ejemplo se muestra en el tema Código de [depuración de tipo multimedia](media-type-debugging-code.md).

Para establecer el formato de captura:

1.  Obtenga un puntero a la [**interfaz IMFMediaTypeHandler,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) como se muestra en el ejemplo anterior.
2.  Llame [**a IMFMediaTypeHandler::GetMediaTypeByIndex para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) obtener el formato deseado, especificado por index.
3.  Llame [**a IMFMediaTypeHandler::SetCurrentMediaType para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) establecer el formato.

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



El orden en el que se devuelven los formatos depende del dispositivo. Normalmente, se agrupan primero por tipo de compresión o espacio de color; y, a continuación, del tamaño de fotograma más pequeño al mayor tamaño de fotograma dentro de cada grupo.

La velocidad de fotogramas se controla de forma ligeramente diferente que los demás atributos de formato. Para obtener más información, [vea Cómo establecer la velocidad de fotogramas de captura de vídeo.](how-to-set-the-video-capture-frame-rate.md)

> [!Note]  
> En algunos dispositivos, la lista de formatos contendrá una entrada duplicada para cada formato. Por ejemplo, si el dispositivo admite 15 formatos de captura distintos, la lista contendrá 30 entradas. Dentro de cada par, uno de los tipos de medios tendrá el atributo [**MF MT AM FORMAT \_ \_ \_ \_ TYPE**](mf-mt-am-format-type-attribute.md) igual a **FORMAT \_ VideoInfo** y el otro tendrá **MF MT AM FORMAT \_ \_ \_ \_ TYPE** igual a **FORMAT \_ VideoInfo2.** (Estos dos valores se definen en el archivo de encabezado uuids.h). El segundo tipo también puede contener información de color adicional [(Información](extended-color-information.md)de color extendida) o mostrar un valor diferente para el entrelazado [**(MODO \_ DE \_ INTERLACE \_ DE MF MT**](mf-mt-interlace-mode-attribute.md)). Estos tipos duplicados existen para admitir aplicaciones DirectShow anteriores. En una Media Foundation, debe omitir el tipo **FORMAT \_ VideoInfo** cada vez que se muestra un tipo **FORMAT \_ VideoInfo2** duplicado.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



