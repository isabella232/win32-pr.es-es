---
description: Uso de datos privados de códecs de vídeo
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Uso de datos privados del códec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706118"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="b8c9e-103">Uso de datos privados del códec de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="b8c9e-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b8c9e-104">La salida comprimida generada por los códecs de Windows Media Video 9 no se puede descomprimir correctamente sin algunos datos proporcionados por el codificador.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="b8c9e-105">Estos datos, denominados datos privados de códec, se deben anexar al tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="b8c9e-106">Puede obtener los datos privados del códec llamando a los métodos de la interfaz [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="b8c9e-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="b8c9e-107">Pase la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) completada de otro modo a [IWMCodecPrivateData:: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span><span class="sxs-lookup"><span data-stu-id="b8c9e-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="b8c9e-108">Después, llame a [IWMCodecPrivateData:: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) dos veces, una vez para obtener el tamaño de los datos y, después, de nuevo para copiar los datos en un búfer de ese tamaño.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="b8c9e-109">Cree un nuevo búfer para que contenga la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con los datos privados anexados y copie la estructura y los datos en ese búfer.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="b8c9e-110">Por último, establezca el miembro **pbFormat** de la estructura de **\_ \_ tipo de medio DMO** en la dirección del búfer recién creado y establezca el miembro **cbFormat** en el tamaño combinado, en bytes, de los datos **VIDEOINFOHEADER** y privados.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="b8c9e-111">Si usa MediaFoundation, puede crear una estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) a partir de una interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) mediante una llamada a [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span><span class="sxs-lookup"><span data-stu-id="b8c9e-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="b8c9e-112">Debe usar los datos privados del códec obtenidos después de establecer primero las propiedades en el codificador.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="b8c9e-113">Si se cambia alguna propiedad, debe obtener nuevos datos privados.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="b8c9e-114">Si no utiliza los datos privados obtenidos después de establecer todas las propiedades para la sesión de codificación, es posible que el descodificador no pueda descomprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="b8c9e-115">En el ejemplo de código siguiente se muestra cómo obtener los datos privados para un tipo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="b8c9e-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="b8c9e-116">No se garantiza que los datos privados del códec entregados por un codificador de vídeo sean los mismos que los datos privados entregados por una implementación diferente del mismo códec para la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="b8c9e-117">Siempre debe generar este valor mediante los pasos descritos en este tema. nunca copie los datos privados de otro archivo.</span><span class="sxs-lookup"><span data-stu-id="b8c9e-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b8c9e-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8c9e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c9e-119">Configuración de la codificación de vídeo</span><span class="sxs-lookup"><span data-stu-id="b8c9e-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="b8c9e-120">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="b8c9e-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
