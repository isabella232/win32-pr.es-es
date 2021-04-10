---
description: Configuración de un codificador WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configuración de un codificador WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153667"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="c6fd2-103">Configuración de un codificador WMV</span><span class="sxs-lookup"><span data-stu-id="c6fd2-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="c6fd2-104">Para crear un tipo de salida válido para un codificador Windows Media Video (WMV), debe tener la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="c6fd2-105">Formato del vídeo sin comprimir que se va a codificar.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="c6fd2-106">El subtipo de vídeo que repesents el formato WMV codificado.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="c6fd2-107">Vea [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="c6fd2-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="c6fd2-108">La velocidad de bits de destino para el flujo codificado.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="c6fd2-109">Propiedades de configuración que se van a establecer en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="c6fd2-110">Las propiedades de configuración se documentan en la documentación del códec de Windows Media Audio y vídeo y de las API de DSP.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="c6fd2-111">Para obtener más información, vea "propiedades de secuencia de vídeo" en [propiedades de codificación](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c6fd2-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="c6fd2-112">Para obtener un tipo de salida válido para el codificador, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="c6fd2-113">Utilice la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para crear una instancia del codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="c6fd2-114">Consulte el codificador para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="c6fd2-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="c6fd2-115">Use la interfaz **IPropertyStore** para configurar el codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="c6fd2-116">Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el tipo de vídeo sin comprimir en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="c6fd2-117">Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener la lista de formatos de compresión del codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="c6fd2-118">Los codificadores WMV no devuelven un tipo de medio completo desde este método.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="c6fd2-119">Faltan dos partes de la información en los tipos de medios:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="c6fd2-120">La velocidad de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-120">The target bitrate.</span></span>
    -   <span data-ttu-id="c6fd2-121">Datos de códec privados del codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="c6fd2-122">Antes de establecer el tipo de salida en el codificador, debe agregar ambos elementos al tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="c6fd2-123">Para especificar la velocidad de bits de destino, establezca el atributo [**MF \_ MT \_ AVG de velocidad de \_ bits**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="c6fd2-124">Agregue los datos del códec privado al tipo de medio, como se explica en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="c6fd2-125">Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="c6fd2-126">Datos de códecs privados</span><span class="sxs-lookup"><span data-stu-id="c6fd2-126">Private Codec Data</span></span>

<span data-ttu-id="c6fd2-127">Los datos del códec privado son una estructura de datos opaca que debe obtener del codificador WMV y agregarlos al tipo de compresión, antes de establecer el tipo de compresión en el codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="c6fd2-128">Para obtener los datos privados, debe usar la interfaz **IWMCodecPrivateData** , que se documenta en el SDK de Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="c6fd2-129">Para obtener los datos del códec privado, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="c6fd2-130">Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener un tipo de medio del codificador.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="c6fd2-131">(Este es el paso 6 de la sección anterior).</span><span class="sxs-lookup"><span data-stu-id="c6fd2-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="c6fd2-132">Especifique la velocidad de bits de destino estableciendo el atributo de [**\_ velocidad de \_ \_ bits media MF MT**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="c6fd2-133">Convierta el tipo de medio en una estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) llamando a la función [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="c6fd2-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="c6fd2-134">Consulte el codificador para la interfaz **IWMCodecPrivateData** .</span><span class="sxs-lookup"><span data-stu-id="c6fd2-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="c6fd2-135">Llame al método **IWMCodecPrivateData:: SetPartialOutputType** , pasando la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertida.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="c6fd2-136">Llame dos veces al método **IWMCodecPrivateData:: GetPrivateData** , una vez para obtener el tamaño del búfer para los datos privados y una vez para copiar los datos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="c6fd2-137">Agregue los datos privados al tipo de medio mediante el establecimiento del atributo de [**\_ datos del \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) en el tipo.</span><span class="sxs-lookup"><span data-stu-id="c6fd2-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="c6fd2-138">En el ejemplo extendido siguiente se muestra cómo crear un formato de compresión WMV desde un tipo de vídeo sin comprimir:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



<span data-ttu-id="c6fd2-139">La función CreateVideoEncoder crea un codificador de vídeo para un subtipo de vídeo especificado, como **MFVideoFormat \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="c6fd2-140">La función AddPrivateData agrega los datos del códec privado al tipo de compresión:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



<span data-ttu-id="c6fd2-141">La función CopyPropertyStore es una función auxiliar que copia las propiedades de un almacén de propiedades a otro:</span><span class="sxs-lookup"><span data-stu-id="c6fd2-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c6fd2-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6fd2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6fd2-143">Crear instancias de una MFT del codificador</span><span class="sxs-lookup"><span data-stu-id="c6fd2-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="c6fd2-144">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="c6fd2-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
