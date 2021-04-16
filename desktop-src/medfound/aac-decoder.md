---
description: 'El descodificador AAC Microsoft Media Foundation es una transformación de Media Foundation que descodifica los siguientes perfiles de codificación de audio avanzado (AAC) y AAC (HE-AAC) de alta eficacia:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Descodificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705567"
---
# <a name="aac-decoder"></a><span data-ttu-id="e56f2-103">Descodificador AAC</span><span class="sxs-lookup"><span data-stu-id="e56f2-103">AAC Decoder</span></span>

<span data-ttu-id="e56f2-104">El descodificador AAC Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que descodifica los siguientes perfiles de codificación de audio avanzado (AAC) y AAC (HE-AAC) de alta eficacia:</span><span class="sxs-lookup"><span data-stu-id="e56f2-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="e56f2-105">Perfil de baja complejidad (LC) de MPEG-2 AAC (multicanal).</span><span class="sxs-lookup"><span data-stu-id="e56f2-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="e56f2-106">MPEG-4 HE-AAC V1 (multicanal) con núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="e56f2-107">MPEG-4 HE-AAC V2 (estéreo) con núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="e56f2-108">El descodificador AAC admite las secuencias AAC sin procesar sin encabezados y AAC en una secuencia de transporte de datos de audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="e56f2-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="e56f2-109">A partir de Windows 8, el descodificador AAC también admite la descodificación de secuencias de transporte de audio MPEG-4 con una capa de multiplexación (LATM) y una capa de sincronización (Loa).</span><span class="sxs-lookup"><span data-stu-id="e56f2-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="e56f2-110">También puede convertir una secuencia LATM/Loa a ADTS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="e56f2-111">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="e56f2-111">Media Types</span></span>

<span data-ttu-id="e56f2-112">El descodificador AAC admite los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="e56f2-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="e56f2-113">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="e56f2-113">Input Types</span></span>

<span data-ttu-id="e56f2-114">El descodificador AAC admite los siguientes subtipos de audio:</span><span class="sxs-lookup"><span data-stu-id="e56f2-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="e56f2-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="e56f2-115">Subtype</span></span>                     | <span data-ttu-id="e56f2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e56f2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e56f2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e56f2-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="e56f2-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="e56f2-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="e56f2-119">AAC sin procesar o ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="e56f2-120">Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y de estéreo paramétricos (PS), si está presente.</span><span class="sxs-lookup"><span data-stu-id="e56f2-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="e56f2-121">El efecto de la herramienta SBR es duplicar la velocidad de muestra descodificada en relación con la velocidad de muestra de núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="e56f2-122">El efecto de la herramienta PS es descodificar estéreo de una secuencia de núcleos AAC-LC de canal mono.</span><span class="sxs-lookup"><span data-stu-id="e56f2-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="e56f2-123">Este subtipo es equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definido en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e56f2-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="e56f2-124">Vea [GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e56f2-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="e56f2-125">El [origen de archivo MPEG-4](mpeg-4-file-source.md) y el analizador ADTS generan este subtipo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="e56f2-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="e56f2-126">mfapi.h</span></span>      |
| <span data-ttu-id="e56f2-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="e56f2-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="e56f2-128">AAC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e56f2-128">Raw AAC.</span></span> <br/> <span data-ttu-id="e56f2-129">Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="e56f2-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="e56f2-130">Para este subtipo, el tipo de medio proporciona la velocidad de muestra y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.</span><span class="sxs-lookup"><span data-stu-id="e56f2-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="e56f2-131">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="e56f2-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="e56f2-132">Para configurar el descodificador AAC, establezca los siguientes atributos en el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="e56f2-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e56f2-133">Atributo</span><span class="sxs-lookup"><span data-stu-id="e56f2-133">Attribute</span></span></th>
<th><span data-ttu-id="e56f2-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="e56f2-134">Description</span></span></th>
<th><span data-ttu-id="e56f2-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e56f2-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e56f2-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-137">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e56f2-137">Major type.</span></span></td>
<td><span data-ttu-id="e56f2-138">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="e56f2-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-140">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="e56f2-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="e56f2-141">Consulte la descripción anterior para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e56f2-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="e56f2-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="e56f2-143">Nivel y Perfil de audio.</span><span class="sxs-lookup"><span data-stu-id="e56f2-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="e56f2-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e56f2-144">Optional.</span></span> <span data-ttu-id="e56f2-145">Solo se aplica a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="e56f2-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="e56f2-146">El valor de este atributo es el campo <strong>audioProfileLevelIndication</strong> , tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="e56f2-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="e56f2-147">Si es desconocido, establezca en cero o 0xFE (no se ha &quot; especificado ningún perfil de audio &quot; ).</span><span class="sxs-lookup"><span data-stu-id="e56f2-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="e56f2-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="e56f2-149">Tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="e56f2-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="e56f2-150">Solo se aplica a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="e56f2-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="e56f2-151">El descodificador admite los siguientes tipos de carga:</span><span class="sxs-lookup"><span data-stu-id="e56f2-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="e56f2-152">0: AAC sin formato.</span><span class="sxs-lookup"><span data-stu-id="e56f2-152">0: Raw AAC.</span></span> <span data-ttu-id="e56f2-153">El flujo contiene solo los elementos raw_data_block (), tal y como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e56f2-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="e56f2-154">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-154">1: ADTS.</span></span> <span data-ttu-id="e56f2-155">La secuencia contiene un adts_sequence (), tal y como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e56f2-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="e56f2-156">Solo se permite un raw_data_block () por adts_frame ().</span><span class="sxs-lookup"><span data-stu-id="e56f2-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="e56f2-157">3: flujo de transporte de audio con un nivel de sincronización (Loa) y una capa de multiplexación (LATM).</span><span class="sxs-lookup"><span data-stu-id="e56f2-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="e56f2-158">De los tres tipos de loa, solo se admite <strong>AudioSyncStream</strong> .</span><span class="sxs-lookup"><span data-stu-id="e56f2-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="e56f2-159">La capa Multiplex es <strong>AudioMuxElement</strong>, está restringida a un programa de audio y una capa.</span><span class="sxs-lookup"><span data-stu-id="e56f2-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="e56f2-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> es opcional.</span><span class="sxs-lookup"><span data-stu-id="e56f2-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="e56f2-161">Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que el flujo solo contiene elementos raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="e56f2-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-163">Profundidad de bits deseada del audio PCM descodificado.</span><span class="sxs-lookup"><span data-stu-id="e56f2-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-165">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="e56f2-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="e56f2-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e56f2-166">Optional.</span></span> <span data-ttu-id="e56f2-167">Para obtener más información, consulta <a href="#format-constraints">Format Constraints</a>.</span><span class="sxs-lookup"><span data-stu-id="e56f2-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-169">Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="e56f2-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="e56f2-170">La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e56f2-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-172">Frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="e56f2-173">La interpretación de este valor depende del subtipo de medios, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e56f2-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-175">Información de formato adicional.</span><span class="sxs-lookup"><span data-stu-id="e56f2-175">Additional format information.</span></span></td>
<td><span data-ttu-id="e56f2-176">El valor de este atributo depende del subtipo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="e56f2-177"><strong>MFAudioFormat_AAC</strong>: contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>WAVEFORMATEX</strong> (es decir, después del miembro de <strong>WFX</strong> ).</span><span class="sxs-lookup"><span data-stu-id="e56f2-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="e56f2-178">A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="e56f2-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="e56f2-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contiene los datos de AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="e56f2-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="e56f2-180">Estos datos deben aparecer; de lo contrario, el descodificador rechazará el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e56f2-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="e56f2-181">La longitud de los datos AudioSpecificConfig () es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="e56f2-182">Tiene más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="e56f2-183">El valor de <strong>audioObjectType</strong> tal y como se define en AudioSpecificConfig () debe ser 2, lo que indica AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="e56f2-184">El valor de <strong>extensionAudioObjectType</strong> debe ser 5 para SBR o 29 para PS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="e56f2-185">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="e56f2-185">Output Types</span></span>

<span data-ttu-id="e56f2-186">El descodificador admite los siguientes tipos de salida:</span><span class="sxs-lookup"><span data-stu-id="e56f2-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e56f2-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="e56f2-187">Subtype</span></span></th>
<th><span data-ttu-id="e56f2-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="e56f2-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e56f2-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="e56f2-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="e56f2-190">Audio de punto flotante IEEE.</span><span class="sxs-lookup"><span data-stu-id="e56f2-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="e56f2-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="e56f2-192">audio PCM de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e56f2-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="e56f2-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="e56f2-194">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e56f2-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="e56f2-195">Este tipo de salida se puede usar para convertir una secuencia AAC en formato loa/LATM al formato ADTS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="e56f2-196">Para convertir una secuencia loa/LATM en una secuencia ADTS, establezca el tipo de entrada en <strong>MFAudioFormat_AAC</strong> con el tipo de carga 3 (Loa).</span><span class="sxs-lookup"><span data-stu-id="e56f2-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="e56f2-197">A continuación, establezca el tipo de salida en <strong>MFAudioFormat_AAC</strong> con el tipo de carga 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="e56f2-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="e56f2-198">El descodificador volverá a formatear el conainter sin descodificar el fragmentada.</span><span class="sxs-lookup"><span data-stu-id="e56f2-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e56f2-199">El descodificador no registra <strong>MFAudioFormat_AAC</strong> como un tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="e56f2-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="e56f2-200">Sin embargo, si la aplicación establece el tipo de entrada como se describe, el método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> devuelve <strong>MFAudioFormat_AAC</strong> en la lista de tipos de salida disponibles.</span><span class="sxs-lookup"><span data-stu-id="e56f2-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e56f2-201">Si el flujo de entrada contiene más de dos canales, el descodificador AAC proporciona dos opciones para el formato de salida:</span><span class="sxs-lookup"><span data-stu-id="e56f2-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="e56f2-202">La misma configuración de canal que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e56f2-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="e56f2-203">Plegado estéreo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="e56f2-204">Restricciones de formato</span><span class="sxs-lookup"><span data-stu-id="e56f2-204">Format Constraints</span></span>

<span data-ttu-id="e56f2-205">La velocidad de muestreo de audio descodificada debe ser una de las siguientes, después de aplicar SBR (si existe):</span><span class="sxs-lookup"><span data-stu-id="e56f2-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="e56f2-206">8 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-206">8 kHz</span></span>
-   <span data-ttu-id="e56f2-207">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-207">11.025 kHz</span></span>
-   <span data-ttu-id="e56f2-208">12 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-208">12 kHz</span></span>
-   <span data-ttu-id="e56f2-209">16 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-209">16 kHz</span></span>
-   <span data-ttu-id="e56f2-210">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-210">22.05 kHz</span></span>
-   <span data-ttu-id="e56f2-211">24 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-211">24 kHz</span></span>
-   <span data-ttu-id="e56f2-212">32 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-212">32 kHz</span></span>
-   <span data-ttu-id="e56f2-213">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-213">44.1 kHz</span></span>
-   <span data-ttu-id="e56f2-214">48 kHz</span><span class="sxs-lookup"><span data-stu-id="e56f2-214">48 kHz</span></span>

<span data-ttu-id="e56f2-215">No se admiten las tasas de muestreo por encima de 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="e56f2-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="e56f2-216">El descodificador admite hasta 6 canales de audio.</span><span class="sxs-lookup"><span data-stu-id="e56f2-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="e56f2-217">Para cada configuración de altavoz, el descodificador espera que los elementos sintácticos AAC aparezcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="e56f2-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="e56f2-218">En la tabla siguiente se enumeran las configuraciones de altavoz compatibles.</span><span class="sxs-lookup"><span data-stu-id="e56f2-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="e56f2-219">En la tercera columna de la tabla se enumeran los elementos sintácticos esperados y su orden mediante la notación siguiente:</span><span class="sxs-lookup"><span data-stu-id="e56f2-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="e56f2-220"><SCE1>: El single_channel_element (SCE) asociado al altavoz del centro frontal.</span><span class="sxs-lookup"><span data-stu-id="e56f2-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="e56f2-221"><SCE2>: El SCE asociado al altavoz del centro trasero.</span><span class="sxs-lookup"><span data-stu-id="e56f2-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="e56f2-222"><CPE1>: El channel_pair_element (CPE) asociado a los altavoces frontales.</span><span class="sxs-lookup"><span data-stu-id="e56f2-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="e56f2-223"><CPE2>: El CPE asociado a los altavoces traseros (o laterales)</span><span class="sxs-lookup"><span data-stu-id="e56f2-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="e56f2-224"><LFE>: El lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="e56f2-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="e56f2-225">Para obtener más información acerca de estos elementos sintácticos, consulte ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="e56f2-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="e56f2-226">Configuración</span><span class="sxs-lookup"><span data-stu-id="e56f2-226">Configuration</span></span>       | <span data-ttu-id="e56f2-227">Máscara de canal</span><span class="sxs-lookup"><span data-stu-id="e56f2-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="e56f2-228">Elementos sintácticos AAC</span><span class="sxs-lookup"><span data-stu-id="e56f2-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="e56f2-229">Mono</span><span class="sxs-lookup"><span data-stu-id="e56f2-229">Mono</span></span>                | <span data-ttu-id="e56f2-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e56f2-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="e56f2-231">Estéreo o dual mono</span><span class="sxs-lookup"><span data-stu-id="e56f2-231">Stereo or dual mono</span></span> | <span data-ttu-id="e56f2-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e56f2-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="e56f2-233">2/1</span><span class="sxs-lookup"><span data-stu-id="e56f2-233">2/1</span></span>                 | <span data-ttu-id="e56f2-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e56f2-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="e56f2-235">2/2</span><span class="sxs-lookup"><span data-stu-id="e56f2-235">2/2</span></span>                 | <span data-ttu-id="e56f2-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e56f2-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="e56f2-237">3/0</span><span class="sxs-lookup"><span data-stu-id="e56f2-237">3/0</span></span>                 | <span data-ttu-id="e56f2-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e56f2-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="e56f2-239">3/1</span><span class="sxs-lookup"><span data-stu-id="e56f2-239">3/1</span></span>                 | <span data-ttu-id="e56f2-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="e56f2-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="e56f2-241">3/2</span><span class="sxs-lookup"><span data-stu-id="e56f2-241">3/2</span></span>                 | <span data-ttu-id="e56f2-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e56f2-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="e56f2-243">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="e56f2-243">3/2 + LFE</span></span>           | <span data-ttu-id="e56f2-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e56f2-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="e56f2-245">En el AAC sin procesar, cada muestra de entrada debe contener exactamente un fotograma comprimido AAC completo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="e56f2-246">En el caso de ADTS, cada ejemplo de entrada puede contener varios fotogramas de audio, así como fotogramas parciales, es decir, los fotogramas pueden abarcar los límites de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="e56f2-247">Cada encabezado ADTS debe ir seguido de un marco AAC.</span><span class="sxs-lookup"><span data-stu-id="e56f2-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="e56f2-248">El descodificador AAC no es compatible con ninguno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="e56f2-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="e56f2-249">Perfil principal, perfil de Sample-Rate escalable (SRS) o Perfil de predicción a largo plazo (LTP).</span><span class="sxs-lookup"><span data-stu-id="e56f2-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="e56f2-250">Formato de intercambio de datos de audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="e56f2-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="e56f2-251">Flujos de transporte de LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="e56f2-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="e56f2-252">Acoplamiento de elementos de canal (CCEs).</span><span class="sxs-lookup"><span data-stu-id="e56f2-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="e56f2-253">El descodificador omitirá los fotogramas de audio con CCEs.</span><span class="sxs-lookup"><span data-stu-id="e56f2-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="e56f2-254">AAC-LC con un tamaño de fotograma 960 de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="e56f2-255">Solo se admiten los fotogramas de ejemplo 1024.</span><span class="sxs-lookup"><span data-stu-id="e56f2-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="e56f2-256">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="e56f2-256">Transform Attributes</span></span>

<span data-ttu-id="e56f2-257">El descodificador AAC implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="e56f2-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e56f2-258">Las aplicaciones pueden utilizar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e56f2-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e56f2-259">Atributo</span><span class="sxs-lookup"><span data-stu-id="e56f2-259">Attribute</span></span></th>
<th><span data-ttu-id="e56f2-260">Descripción</span><span class="sxs-lookup"><span data-stu-id="e56f2-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e56f2-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-262">Especifica si el audio de 2 canales se codifica como estéreo o dual mono.</span><span class="sxs-lookup"><span data-stu-id="e56f2-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="e56f2-263">Tratar como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e56f2-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e56f2-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-265">Especifica cómo el descodificador Reproduce audio mono dual.</span><span class="sxs-lookup"><span data-stu-id="e56f2-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="e56f2-266">El valor predeterminado es <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: CH1 de salida a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="e56f2-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="e56f2-267">Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e56f2-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e56f2-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e56f2-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="e56f2-269">El descodificador AAC no controla los cambios de formato dinámico y se debe vaciar o purgar antes de que se establezca un nuevo tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="e56f2-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="e56f2-270">Trate este atributo como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e56f2-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e56f2-271">El descodificador AAC informa incorrectamente de un valor de <strong>true</strong> para este atributo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="e56f2-272">En Windows 7, el descodificador informa incorrectamente de un valor de <strong>true</strong> para este atributo.</span><span class="sxs-lookup"><span data-stu-id="e56f2-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="e56f2-273">En Windows 8, el descodificador informa de <strong>false</strong>, que es el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="e56f2-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="e56f2-274">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="e56f2-274">Example Media Types</span></span>

<span data-ttu-id="e56f2-275">Este es un ejemplo del tipo de medio de entrada necesario para una secuencia de 6 canales AAC-LC de 48 kHz mediante una carga de AAC sin procesar:</span><span class="sxs-lookup"><span data-stu-id="e56f2-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="e56f2-276">Atributo</span><span class="sxs-lookup"><span data-stu-id="e56f2-276">Attribute</span></span>                                                                                      | <span data-ttu-id="e56f2-277">Value</span><span class="sxs-lookup"><span data-stu-id="e56f2-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e56f2-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e56f2-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="e56f2-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="e56f2-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="e56f2-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="e56f2-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="e56f2-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="e56f2-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="e56f2-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e56f2-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="e56f2-283">48000</span><span class="sxs-lookup"><span data-stu-id="e56f2-283">48000</span></span>                                                                                |
| [<span data-ttu-id="e56f2-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="e56f2-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="e56f2-285">6</span><span class="sxs-lookup"><span data-stu-id="e56f2-285">6</span></span>                                                                                    |
| [<span data-ttu-id="e56f2-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="e56f2-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="e56f2-287">0</span><span class="sxs-lookup"><span data-stu-id="e56f2-287">0</span></span>                                                                                    |
| [<span data-ttu-id="e56f2-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="e56f2-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="e56f2-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="e56f2-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="e56f2-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="e56f2-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="e56f2-291">0x2a (opcional)</span><span class="sxs-lookup"><span data-stu-id="e56f2-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="e56f2-292">Los 12 primeros bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corresponden a los siguientes miembros de la estructura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :</span><span class="sxs-lookup"><span data-stu-id="e56f2-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="e56f2-293">**wPayloadType** = 0 (AAC sin procesar)</span><span class="sxs-lookup"><span data-stu-id="e56f2-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="e56f2-294">**wAudioProfileLevelIndication** = 0X2a (perfil AAC, nivel 4)</span><span class="sxs-lookup"><span data-stu-id="e56f2-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="e56f2-295">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="e56f2-295">**wStructType** = 0</span></span>

<span data-ttu-id="e56f2-296">Los dos últimos bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contienen el valor de AudioSpecificConfig (), tal y como se define en MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="e56f2-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="e56f2-297">AudioSpecificConfig. audioObjectType = 2 (LC AAC) (5 bits)</span><span class="sxs-lookup"><span data-stu-id="e56f2-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="e56f2-298">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="e56f2-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="e56f2-299">AudioSpecificConfig. channelConfiguration = 6 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="e56f2-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="e56f2-300">GASpecificConfig. frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="e56f2-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="e56f2-301">GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="e56f2-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="e56f2-302">GASpecificConfig. extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="e56f2-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="e56f2-303">Dado este tipo de entrada, use el siguiente tipo de medio de salida para obtener el audio PCM de punto flotante de 32 bits de 6 canales del descodificador:</span><span class="sxs-lookup"><span data-stu-id="e56f2-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="e56f2-304">Atributo</span><span class="sxs-lookup"><span data-stu-id="e56f2-304">Attribute</span></span>                                                                                    | <span data-ttu-id="e56f2-305">Value</span><span class="sxs-lookup"><span data-stu-id="e56f2-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="e56f2-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e56f2-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="e56f2-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="e56f2-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="e56f2-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="e56f2-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="e56f2-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="e56f2-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="e56f2-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="e56f2-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="e56f2-311">32</span><span class="sxs-lookup"><span data-stu-id="e56f2-311">32</span></span>                       |
| [<span data-ttu-id="e56f2-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e56f2-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="e56f2-313">48000</span><span class="sxs-lookup"><span data-stu-id="e56f2-313">48000</span></span>                    |
| [<span data-ttu-id="e56f2-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="e56f2-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="e56f2-315">6</span><span class="sxs-lookup"><span data-stu-id="e56f2-315">6</span></span>                        |
| [<span data-ttu-id="e56f2-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="e56f2-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="e56f2-317">1152000 (opcional)</span><span class="sxs-lookup"><span data-stu-id="e56f2-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="e56f2-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="e56f2-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="e56f2-319">24 (opcional)</span><span class="sxs-lookup"><span data-stu-id="e56f2-319">24 (optional)</span></span>            |
| [<span data-ttu-id="e56f2-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="e56f2-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="e56f2-321">0x3F (opcional)</span><span class="sxs-lookup"><span data-stu-id="e56f2-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="e56f2-322">Si está instalado el complemento de actualización de plataforma para Windows Vista, el descodificador de audio AAC está disponible en Windows Vista, pero solo es accesible en Windows Vista mediante el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e56f2-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e56f2-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e56f2-323">Requirements</span></span>



| <span data-ttu-id="e56f2-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="e56f2-324">Requirement</span></span> | <span data-ttu-id="e56f2-325">Value</span><span class="sxs-lookup"><span data-stu-id="e56f2-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56f2-326">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e56f2-326">Minimum supported client</span></span><br/> | <span data-ttu-id="e56f2-327">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e56f2-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="e56f2-328">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e56f2-328">Minimum supported server</span></span><br/> | <span data-ttu-id="e56f2-329">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e56f2-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e56f2-330">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e56f2-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e56f2-331"><dt>Msmpeg2adec.dll en Windows 7; </dt> <dt>MSAudDecMFT.dll en Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="e56f2-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56f2-332">Vea también</span><span class="sxs-lookup"><span data-stu-id="e56f2-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56f2-333">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="e56f2-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e56f2-334">Tipos de medios AAC</span><span class="sxs-lookup"><span data-stu-id="e56f2-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="e56f2-335">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="e56f2-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="e56f2-336">**Descodificador de audio MPEG-1/DD/AAC de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="e56f2-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="e56f2-337">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e56f2-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e56f2-338">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e56f2-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
