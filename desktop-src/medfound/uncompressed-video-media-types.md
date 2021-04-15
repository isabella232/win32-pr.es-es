---
description: Tipos de medios de vídeo sin comprimir
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Tipos de medios de vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547342"
---
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="857eb-103">Tipos de medios de vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="857eb-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="857eb-104">En este tema se describe cómo crear un tipo de medio que describa un formato de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="857eb-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="857eb-105">Para obtener más información sobre los tipos de medios, consulte [acerca de los tipos de medios](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="857eb-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="857eb-106">Para crear un tipo de vídeo sin comprimir completo, establezca los siguientes atributos en el puntero de la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="857eb-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="857eb-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="857eb-107">Attribute</span></span>                                                                            | <span data-ttu-id="857eb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="857eb-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="857eb-109">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="857eb-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="857eb-110">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="857eb-110">Major type.</span></span> <span data-ttu-id="857eb-111">Establezca en **\_ vídeo de MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="857eb-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="857eb-112">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="857eb-113">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="857eb-113">Subtype.</span></span> <span data-ttu-id="857eb-114">Vea [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="857eb-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="857eb-115">**\_ \_ intervalo predeterminado de MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="857eb-116">STRIDE Surface.</span><span class="sxs-lookup"><span data-stu-id="857eb-116">Surface stride.</span></span> <span data-ttu-id="857eb-117">*STRIDE* es el número de bytes necesarios para pasar de una fila de píxeles a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="857eb-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="857eb-118">Establezca este atributo si el intervalo en bytes no es igual que el ancho de vídeo en bytes.</span><span class="sxs-lookup"><span data-stu-id="857eb-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="857eb-119">De lo contrario, puede omitir este atributo.</span><span class="sxs-lookup"><span data-stu-id="857eb-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="857eb-120">**\_velocidad de \_ fotogramas MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="857eb-121">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="857eb-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="857eb-122">**\_tamaño de \_ marco MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="857eb-123">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="857eb-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="857eb-124">**\_ \_ modo entrelazado MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="857eb-125">Modo de entrelazado.</span><span class="sxs-lookup"><span data-stu-id="857eb-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="857eb-126">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="857eb-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="857eb-127">Especifica si cada ejemplo es independiente.</span><span class="sxs-lookup"><span data-stu-id="857eb-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="857eb-128">Establézcalo en **true** para los formatos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="857eb-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="857eb-129">**\_relación de \_ aspecto de píxeles MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="857eb-130">Relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="857eb-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="857eb-131">Además, establezca los siguientes atributos si conoce los valores correctos.</span><span class="sxs-lookup"><span data-stu-id="857eb-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="857eb-132">(De lo contrario, omita estos atributos).</span><span class="sxs-lookup"><span data-stu-id="857eb-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="857eb-133">Atributo</span><span class="sxs-lookup"><span data-stu-id="857eb-133">Attribute</span></span>                                                                    | <span data-ttu-id="857eb-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="857eb-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="857eb-135">**\_ \_ primarios de vídeo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="857eb-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="857eb-136">Primarios de color.</span><span class="sxs-lookup"><span data-stu-id="857eb-136">Color primaries.</span></span>   |
| [<span data-ttu-id="857eb-137">**MF \_ MT \_ Transfer ( \_ función)**</span><span class="sxs-lookup"><span data-stu-id="857eb-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="857eb-138">Función de transferencia.</span><span class="sxs-lookup"><span data-stu-id="857eb-138">Transfer function.</span></span> |
| [<span data-ttu-id="857eb-139">**MF \_ MT \_ YUV \_ Matrix**</span><span class="sxs-lookup"><span data-stu-id="857eb-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="857eb-140">Matriz de transferencia.</span><span class="sxs-lookup"><span data-stu-id="857eb-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="857eb-141">**vídeo croma de MF MT en el \_ \_ \_ \_ emplazamiento**</span><span class="sxs-lookup"><span data-stu-id="857eb-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="857eb-142">Croma en el emplazamiento.</span><span class="sxs-lookup"><span data-stu-id="857eb-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="857eb-143">**\_ \_ \_ rango nominal de vídeo \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="857eb-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="857eb-144">Intervalo nominal.</span><span class="sxs-lookup"><span data-stu-id="857eb-144">Nominal range.</span></span>     |



 

<span data-ttu-id="857eb-145">Para obtener más información, vea [información de color extendido](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="857eb-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="857eb-146">Por ejemplo, si crea un tipo de medio que describe un estándar de vídeo y el estándar define la colocación de croma, agregue esta información al tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="857eb-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="857eb-147">Esto ayuda a conservar la fidelidad de color a lo largo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="857eb-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="857eb-148">Las siguientes funciones pueden ser útiles al crear un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="857eb-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="857eb-149">Función</span><span class="sxs-lookup"><span data-stu-id="857eb-149">Function</span></span>                                                                     | <span data-ttu-id="857eb-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="857eb-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="857eb-151">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="857eb-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="857eb-152">Calcula la velocidad de fotogramas, dada la duración media de los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="857eb-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="857eb-153">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="857eb-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="857eb-154">Calcula el tamaño de la imagen para un formato de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="857eb-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="857eb-155">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="857eb-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="857eb-156">Calcula la duración media de un fotograma de vídeo, dada la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="857eb-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="857eb-157">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="857eb-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="857eb-158">Devuelve el intervalo mínimo de superficie para un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="857eb-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="857eb-159">Para obtener más información, consulte [STRIDE](image-stride.md)de la imagen.</span><span class="sxs-lookup"><span data-stu-id="857eb-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="857eb-160">**MFInitVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="857eb-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="857eb-161">Inicializa una estructura [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) para algunos formatos de vídeo estándar, como el televisor NTSC.</span><span class="sxs-lookup"><span data-stu-id="857eb-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="857eb-162">Después, puede usar la estructura para inicializar un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="857eb-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="857eb-163">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="857eb-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="857eb-164">Consulta si un formato de vídeo es un formato YUV.</span><span class="sxs-lookup"><span data-stu-id="857eb-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="857eb-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="857eb-165">Examples</span></span>

<span data-ttu-id="857eb-166">En este ejemplo se muestra una función que rellena la información más común de un formato de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="857eb-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="857eb-167">La función devuelve un puntero de la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="857eb-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="857eb-168">Después, puede agregar atributos adicionales al tipo de medio según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="857eb-168">You can then add additional attributes to the media type as needed.</span></span>


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="857eb-169">En el siguiente ejemplo se toma como entrada un formato de vídeo codificado y se crea un tipo de vídeo sin comprimir coincidente.</span><span class="sxs-lookup"><span data-stu-id="857eb-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="857eb-170">Este tipo sería adecuado para establecer en un codificador o descodificador, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="857eb-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="857eb-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="857eb-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="857eb-172">Información de color ampliada</span><span class="sxs-lookup"><span data-stu-id="857eb-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="857eb-173">Intervalo de imagen</span><span class="sxs-lookup"><span data-stu-id="857eb-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="857eb-174">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="857eb-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="857eb-175">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="857eb-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="857eb-176">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="857eb-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



