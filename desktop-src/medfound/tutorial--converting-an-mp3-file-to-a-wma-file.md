---
description: En este tutorial se muestra cómo usar la API de Transcode para codificar un archivo Windows Media Audio (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: codificar un archivo WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696876"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="47ed6-103">Tutorial: codificar un archivo WMA</span><span class="sxs-lookup"><span data-stu-id="47ed6-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="47ed6-104">En este tutorial se muestra cómo usar la [API de Transcode](transcode-api.md) para codificar un archivo Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="47ed6-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="47ed6-105">En este tutorial se vuelve a usar la mayoría del código del tutorial [codificación de un archivo MP4](tutorial--encoding-an-mp4-file-.md), por lo que primero debe leer ese tutorial.</span><span class="sxs-lookup"><span data-stu-id="47ed6-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="47ed6-106">El único código que difiere es la función `CreateTranscodeProfile` , que crea el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="47ed6-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="47ed6-107">Crear el perfil de transcodificación</span><span class="sxs-lookup"><span data-stu-id="47ed6-107">Create the Transcode Profile</span></span>

<span data-ttu-id="47ed6-108">Un *perfil* de transcodificación describe los parámetros de codificación y el contenedor de archivos.</span><span class="sxs-lookup"><span data-stu-id="47ed6-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="47ed6-109">En el caso de WMA, el contenedor de archivos es un archivo de formato de streaming avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="47ed6-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="47ed6-110">El archivo ASF contiene una secuencia de audio, que está codificada mediante el [**codificador Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="47ed6-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="47ed6-111">Para compilar la topología de transcodificación, cree el perfil de transcodificación y especifique los parámetros para la secuencia de audio y el contenedor.</span><span class="sxs-lookup"><span data-stu-id="47ed6-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="47ed6-112">A continuación, cree la topología especificando el origen de entrada, la dirección URL de salida y el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="47ed6-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="47ed6-113">Para crear el perfil, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="47ed6-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="47ed6-114">Llame a la función [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para crear un perfil de transcodificación vacío.</span><span class="sxs-lookup"><span data-stu-id="47ed6-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="47ed6-115">Llame a [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) para obtener una lista de los tipos de medios de audio del codificador.</span><span class="sxs-lookup"><span data-stu-id="47ed6-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="47ed6-116">Esta función devuelve un puntero [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que representa una colección de punteros [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="47ed6-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="47ed6-117">Elija el tipo de medio de audio que coincida con los requisitos de transcodificación y copie los atributos en un almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="47ed6-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="47ed6-118">En este tutorial, se usa el primer tipo de medio de la lista.</span><span class="sxs-lookup"><span data-stu-id="47ed6-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="47ed6-119">Llame a [**IMFCollection:: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) para seleccionar un tipo de medio de audio de la lista.</span><span class="sxs-lookup"><span data-stu-id="47ed6-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="47ed6-120">Consulte el tipo de medio para obtener un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) del almacén de atributos del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="47ed6-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="47ed6-121">Llame a [**IMFAttributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) para obtener el número de atributos contenidos en el tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="47ed6-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="47ed6-122">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="47ed6-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="47ed6-123">Llame a [**IMFAttributes:: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) para copiar los atributos del tipo de archivo multimedia en el nuevo almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="47ed6-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="47ed6-124">Llame a [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) para establecer los atributos de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="47ed6-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="47ed6-125">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos para los atributos de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="47ed6-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="47ed6-126">Establezca el atributo [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) en **MFTranscodeContainerType \_ ASF**, que especifica un contenedor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="47ed6-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="47ed6-127">Llame a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para establecer los atributos de nivel de contenedor en el perfil.</span><span class="sxs-lookup"><span data-stu-id="47ed6-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="47ed6-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47ed6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ed6-129">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="47ed6-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



