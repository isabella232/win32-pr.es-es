---
description: En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipos de medios AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003311"
---
# <a name="aac-media-types"></a><span data-ttu-id="18bae-103">Tipos de medios AAC</span><span class="sxs-lookup"><span data-stu-id="18bae-103">AAC Media Types</span></span>

<span data-ttu-id="18bae-104">En este tema se describe cómo especificar el formato de una secuencia de codificación de audio avanzada (AAC) en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="18bae-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="18bae-105">Se definen dos subtipos para el audio AAC:</span><span class="sxs-lookup"><span data-stu-id="18bae-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="18bae-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="18bae-106">Subtype</span></span>                     | <span data-ttu-id="18bae-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="18bae-107">Description</span></span>          | <span data-ttu-id="18bae-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18bae-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="18bae-109">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="18bae-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="18bae-110">AAC sin procesar o ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="18bae-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="18bae-111">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="18bae-111">mfapi.h</span></span>      |
| <span data-ttu-id="18bae-112">**MEDIASUBTYPE \_ raw \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="18bae-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="18bae-113">AAC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="18bae-113">Raw AAC.</span></span>             | <span data-ttu-id="18bae-114">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="18bae-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="18bae-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC</span><span class="sxs-lookup"><span data-stu-id="18bae-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="18bae-116">Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y de estéreo paramétricos (PS), si está presente.</span><span class="sxs-lookup"><span data-stu-id="18bae-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="18bae-117">El efecto de la herramienta SBR es duplicar la velocidad de muestra descodificada en relación con la velocidad de muestra de núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="18bae-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="18bae-118">El efecto de la herramienta PS es descodificar estéreo de una secuencia de núcleos AAC-LC de canal mono.</span><span class="sxs-lookup"><span data-stu-id="18bae-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="18bae-119">Este subtipo es equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, que se define en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="18bae-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="18bae-120">Vea [GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="18bae-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="18bae-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ raw \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="18bae-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="18bae-122">Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual al formato de onda \_ \_ raw \_ AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="18bae-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="18bae-123">Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.</span><span class="sxs-lookup"><span data-stu-id="18bae-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="18bae-124">Los siguientes atributos de tipo de medio se aplican al audio AAC.</span><span class="sxs-lookup"><span data-stu-id="18bae-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18bae-125">Atributo</span><span class="sxs-lookup"><span data-stu-id="18bae-125">Attribute</span></span></th>
<th><span data-ttu-id="18bae-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="18bae-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18bae-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="18bae-128">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="18bae-128">Major type.</span></span> <span data-ttu-id="18bae-129">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="18bae-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18bae-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="18bae-131">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="18bae-131">Audio subtype.</span></span> <span data-ttu-id="18bae-132">Consulte la descripción anterior para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="18bae-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18bae-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="18bae-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="18bae-134">Nivel y Perfil de audio.</span><span class="sxs-lookup"><span data-stu-id="18bae-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="18bae-135">El valor de este atributo es el campo <strong>audioProfileLevelIndication</strong> , tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="18bae-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="18bae-136">Si es desconocido, establezca en cero o 0xFE (no se ha &quot; especificado ningún perfil de audio &quot; ).</span><span class="sxs-lookup"><span data-stu-id="18bae-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18bae-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="18bae-138">Velocidad de bits de la secuencia AAC codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="18bae-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18bae-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="18bae-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="18bae-140">Tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="18bae-140">Payload type.</span></span><br/> <span data-ttu-id="18bae-141">Solo se aplica a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="18bae-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="18bae-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> es opcional.</span><span class="sxs-lookup"><span data-stu-id="18bae-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="18bae-143">Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que el flujo solo contiene elementos raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="18bae-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18bae-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="18bae-145">Profundidad de bits del audio PCM descodificado.</span><span class="sxs-lookup"><span data-stu-id="18bae-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18bae-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="18bae-147">Asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="18bae-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18bae-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="18bae-149">Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="18bae-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="18bae-150">La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18bae-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18bae-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="18bae-152">Frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="18bae-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="18bae-153">La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18bae-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18bae-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="18bae-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="18bae-155">El valor de este atributo depende del subtipo:</span><span class="sxs-lookup"><span data-stu-id="18bae-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="18bae-156"><strong>MFAudioFormat_AAC</strong>: contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>WAVEFORMATEX</strong> (es decir, después del miembro de <strong>WFX</strong> ).</span><span class="sxs-lookup"><span data-stu-id="18bae-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="18bae-157">A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="18bae-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="18bae-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene los datos de AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="18bae-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="18bae-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18bae-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18bae-160">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="18bae-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="18bae-161">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="18bae-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="18bae-162">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18bae-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="18bae-163">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="18bae-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

