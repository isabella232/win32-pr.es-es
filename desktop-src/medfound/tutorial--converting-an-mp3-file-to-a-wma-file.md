---
description: En este tutorial se muestra cómo usar Transcode API para codificar un archivo Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: Codificación de un archivo WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268660"
---
# <a name="tutorial-encoding-a-wma-file"></a>Tutorial: Codificación de un archivo WMA

En este tutorial se muestra cómo usar [Transcode API](transcode-api.md) para codificar un archivo Windows Media Audio (WMA).

En este tutorial se reutiliza la mayor parte del código del tutorial Codificación de un archivo [MP4,](tutorial--encoding-an-mp4-file-.md)por lo que debe leer primero ese tutorial. El único código que difiere es la función `CreateTranscodeProfile` , que crea el perfil de transcodificación.

## <a name="create-the-transcode-profile"></a>Creación del perfil de transcodificación

Un *perfil de transcodificación* describe los parámetros de codificación y el contenedor de archivos. Para WMA, el contenedor de archivos es un archivo de formato de streaming avanzado (ASF). El archivo ASF contiene una secuencia de audio, que se codifica mediante el [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).

Para compilar la topología de transcodificación, cree el perfil de transcodificación y especifique los parámetros para la secuencia de audio y el contenedor. A continuación, cree la topología especificando el origen de entrada, la dirección URL de salida y el perfil de transcodificación.

Para crear el perfil, realice los pasos siguientes.

1.  Llame a [**la función MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para crear un perfil de transcodificación vacío.
2.  Llame [**a MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) para obtener una lista de tipos de medios de audio del codificador. Esta función devuelve un [**puntero IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que representa una colección de punteros [**IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
3.  Elija el tipo de medio de audio que coincida con los requisitos de transcodificación y copie los atributos en un almacén de atributos. En este tutorial, se usa el primer tipo de medio de la lista.
    -   Llame [**a IMFCollection::GetElement para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) seleccionar un tipo de medio de audio de la lista.
    -   Consulte el tipo de medio para obtener un puntero a la interfaz [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) del almacén de atributos del tipo de medio.
    -   Llame [**a IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) para obtener el número de atributos contenidos en el tipo de medio.
    -   Llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.
    -   Llame [**a IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) para copiar los atributos del tipo de medio en el nuevo almacén de atributos.
4.  Llame [**a IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) para establecer los atributos de la secuencia de audio.
5.  Llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos para los atributos de nivel de contenedor.
6.  Establezca el [atributo MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md) en **MFTranscodeContainerType \_ ASF**, que especifica un contenedor de archivos ASF.
7.  Llame [**a IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para establecer los atributos de nivel de contenedor en el perfil.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transcodificación de API](transcode-api.md)
</dt> </dl>

 

 



