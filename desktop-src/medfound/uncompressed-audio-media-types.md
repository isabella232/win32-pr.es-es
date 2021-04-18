---
description: Tipos de medios de audio sin comprimir
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: Tipos de medios de audio sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697932"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="b8f37-103">Tipos de medios de audio sin comprimir</span><span class="sxs-lookup"><span data-stu-id="b8f37-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="b8f37-104">Para crear un tipo de audio sin comprimir completo, establezca al menos los siguientes atributos en el puntero de la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="b8f37-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="b8f37-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="b8f37-105">Attribute</span></span>                                                                                    | <span data-ttu-id="b8f37-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8f37-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8f37-107">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="b8f37-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="b8f37-108">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="b8f37-108">Major type.</span></span> <span data-ttu-id="b8f37-109">Establézcalo en MFMediaType \_ audio.</span><span class="sxs-lookup"><span data-stu-id="b8f37-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="b8f37-110">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="b8f37-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="b8f37-111">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="b8f37-111">Subtype.</span></span> <span data-ttu-id="b8f37-112">Vea [GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b8f37-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="b8f37-113">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8f37-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="b8f37-114">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="b8f37-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="b8f37-115">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="b8f37-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="b8f37-116">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="b8f37-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="b8f37-117">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8f37-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="b8f37-118">Alineación de bloque.</span><span class="sxs-lookup"><span data-stu-id="b8f37-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="b8f37-119">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="b8f37-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="b8f37-120">Número promedio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="b8f37-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="b8f37-121">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="b8f37-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="b8f37-122">Número de bits por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="b8f37-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="b8f37-123">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="b8f37-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="b8f37-124">Especifica si cada ejemplo de audio es independiente.</span><span class="sxs-lookup"><span data-stu-id="b8f37-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="b8f37-125">Establézcalo en **true** para los \_ formatos MFAudioFormat PCM y MFAudioFormat \_ float.</span><span class="sxs-lookup"><span data-stu-id="b8f37-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="b8f37-126">Además, se requieren los siguientes atributos en algunos formatos de audio.</span><span class="sxs-lookup"><span data-stu-id="b8f37-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="b8f37-127">Atributo</span><span class="sxs-lookup"><span data-stu-id="b8f37-127">Attribute</span></span>                                                                                      | <span data-ttu-id="b8f37-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8f37-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8f37-129">**\_ \_ bits válidos de audio MF MT \_ \_ \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="b8f37-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="b8f37-130">Número de bits válidos de datos de audio en cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="b8f37-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="b8f37-131">Establezca este atributo si las muestras de audio tienen relleno, es decir, si el número de bits válidos en cada ejemplo de audio es menor que el tamaño de la muestra.</span><span class="sxs-lookup"><span data-stu-id="b8f37-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="b8f37-132">**\_máscara de \_ canal de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8f37-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="b8f37-133">Asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="b8f37-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="b8f37-134">Establezca este atributo para las secuencias de audio multicanal, como 5,1.</span><span class="sxs-lookup"><span data-stu-id="b8f37-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="b8f37-135">Este atributo no es necesario para audio mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="b8f37-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="b8f37-136">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8f37-136">Example Code</span></span>

<span data-ttu-id="b8f37-137">En el código siguiente se muestra cómo crear un tipo de medio para audio PCM sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="b8f37-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="b8f37-138">En el siguiente ejemplo se toma como entrada un formato de audio codificado y se crea un tipo de audio PCM coincidente.</span><span class="sxs-lookup"><span data-stu-id="b8f37-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="b8f37-139">Este tipo sería adecuado para establecer en un codificador o descodificador, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b8f37-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b8f37-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8f37-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8f37-141">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="b8f37-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 



