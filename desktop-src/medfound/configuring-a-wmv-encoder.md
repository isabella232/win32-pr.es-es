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
# <a name="configuring-a-wmv-encoder"></a>Configuración de un codificador WMV

Para crear un tipo de salida válido para un codificador Windows Media Video (WMV), debe tener la siguiente información:

-   Formato del vídeo sin comprimir que se va a codificar.
-   El subtipo de vídeo que repesents el formato WMV codificado. Vea [GUID de subtipo de vídeo](video-subtype-guids.md).
-   La velocidad de bits de destino para el flujo codificado.
-   Propiedades de configuración que se van a establecer en el codificador.

Las propiedades de configuración se documentan en la documentación del códec de Windows Media Audio y vídeo y de las API de DSP. Para obtener más información, vea "propiedades de secuencia de vídeo" en [propiedades de codificación](configuring-the-encoder.md).

Para obtener un tipo de salida válido para el codificador, realice los pasos siguientes.

1.  Utilice la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para crear una instancia del codificador.
2.  Consulte el codificador para la interfaz **IPropertyStore** .
3.  Use la interfaz **IPropertyStore** para configurar el codificador.
4.  Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el tipo de vídeo sin comprimir en el codificador.
5.  Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener la lista de formatos de compresión del codificador. Los codificadores WMV no devuelven un tipo de medio completo desde este método. Faltan dos partes de la información en los tipos de medios:

    -   La velocidad de bits de destino.
    -   Datos de códec privados del codificador.

    Antes de establecer el tipo de salida en el codificador, debe agregar ambos elementos al tipo de medio.

6.  Para especificar la velocidad de bits de destino, establezca el atributo [**MF \_ MT \_ AVG de velocidad de \_ bits**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio.
7.  Agregue los datos del códec privado al tipo de medio, como se explica en la sección siguiente.
8.  Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.

### <a name="private-codec-data"></a>Datos de códecs privados

Los datos del códec privado son una estructura de datos opaca que debe obtener del codificador WMV y agregarlos al tipo de compresión, antes de establecer el tipo de compresión en el codificador. Para obtener los datos privados, debe usar la interfaz **IWMCodecPrivateData** , que se documenta en el SDK de Windows Media Format 11.

Para obtener los datos del códec privado, realice los pasos siguientes:

1.  Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener un tipo de medio del codificador. (Este es el paso 6 de la sección anterior).
2.  Especifique la velocidad de bits de destino estableciendo el atributo de [**\_ velocidad de \_ \_ bits media MF MT**](mf-mt-avg-bitrate-attribute.md) en el tipo de medio.
3.  Convierta el tipo de medio en una estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) llamando a la función [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .
4.  Consulte el codificador para la interfaz **IWMCodecPrivateData** .
5.  Llame al método **IWMCodecPrivateData:: SetPartialOutputType** , pasando la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertida.
6.  Llame dos veces al método **IWMCodecPrivateData:: GetPrivateData** , una vez para obtener el tamaño del búfer para los datos privados y una vez para copiar los datos en el búfer.
7.  Agregue los datos privados al tipo de medio mediante el establecimiento del atributo de [**\_ datos del \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) en el tipo.

En el ejemplo extendido siguiente se muestra cómo crear un formato de compresión WMV desde un tipo de vídeo sin comprimir:


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



La función CreateVideoEncoder crea un codificador de vídeo para un subtipo de vídeo especificado, como **MFVideoFormat \_ WMV3**:


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



La función AddPrivateData agrega los datos del códec privado al tipo de compresión:


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



La función CopyPropertyStore es una función auxiliar que copia las propiedades de un almacén de propiedades a otro:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear instancias de una MFT del codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 
