---
description: 'El descodificador Microsoft Media Foundation AAC es una transformación de Media Foundation que descodifica los siguientes perfiles de Codificación de audio avanzada (AAC) y AAC de alta eficacia (HE-AAC):'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Descodificador de AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436587"
---
# <a name="aac-decoder"></a><span data-ttu-id="d6e0c-103">Descodificador de AAC</span><span class="sxs-lookup"><span data-stu-id="d6e0c-103">AAC Decoder</span></span>

<span data-ttu-id="d6e0c-104">El descodificador Microsoft Media Foundation AAC [](media-foundation-transforms.md) es una transformación de Media Foundation que descodifica los siguientes perfiles de Codificación de audio avanzada (AAC) y AAC de alta eficacia (HE-AAC):</span><span class="sxs-lookup"><span data-stu-id="d6e0c-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="d6e0c-105">Perfil de baja complejidad (LC) de AAC MPEG-2 (multicanal).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="d6e0c-106">MPEG-4 HE-AAC v1 (multicanal) con núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="d6e0c-107">MPEG-4 HE-AAC v2 (estéreo) con núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="d6e0c-108">El descodificador de AAC admite tanto secuencias AAC sin procesar sin encabezados como AAC en una secuencia de transporte de datos de audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="d6e0c-109">A partir Windows 8, el descodificador de AAC también admite la descodificación de secuencias de transporte de audio MPEG-4 con una capa multiplex (LATM) y una capa de sincronización (LOAS).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="d6e0c-110">También puede convertir una secuencia LATM/LOAS en ADTS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d6e0c-111">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="d6e0c-111">Class Identifier</span></span>

<span data-ttu-id="d6e0c-112">El identificador de clase (CLSID) del codificador AAC es **\_ CLSID CMSAACDecMFT**, definido en el archivo de encabezado wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-112">The class identifier (CLSID) of the AAC encoder is **CLSID\_CMSAACDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="d6e0c-113">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="d6e0c-113">Media Types</span></span>

<span data-ttu-id="d6e0c-114">El descodificador de AAC admite los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-114">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="d6e0c-115">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="d6e0c-115">Input Types</span></span>

<span data-ttu-id="d6e0c-116">El descodificador de AAC admite los siguientes subtipos de audio:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-116">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="d6e0c-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="d6e0c-117">Subtype</span></span>                     | <span data-ttu-id="d6e0c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e0c-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d6e0c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6e0c-119">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="d6e0c-120">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-120">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="d6e0c-121">AAC sin procesar o AAC de ADTS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-121">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="d6e0c-122">Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales antes de la aplicación de las herramientas de replicación de banda espectral (SBR) y estéreo paramétrico (PS), si están presentes.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-122">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="d6e0c-123">El efecto de la herramienta SBR es duplicar la frecuencia de muestreo descodificada en relación con la frecuencia de muestreo principal de AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-123">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="d6e0c-124">El efecto de la herramienta PS es descodificar estéreo de una secuencia AAC-LC de núcleo monocanal.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-124">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="d6e0c-125">Este subtipo es equivalente **a MEDIASUBTYPE_MPEG_HEAAC**, definido en wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-125">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="d6e0c-126">Consulte [GUID de subtipo de audio.](audio-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-126">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="d6e0c-127">El [origen de archivo MPEG-4](mpeg-4-file-source.md) y el analizador de ADTS emiten este subtipo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-127">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="d6e0c-128">mfapi.h</span><span class="sxs-lookup"><span data-stu-id="d6e0c-128">mfapi.h</span></span>      |
| <span data-ttu-id="d6e0c-129">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-129">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="d6e0c-130">AAC sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-130">Raw AAC.</span></span> <br/> <span data-ttu-id="d6e0c-131">Este subtipo se usa para AAC incluido en un archivo AVI con la etiqueta de formato de audio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-131">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="d6e0c-132">Para este subtipo, el tipo de medio proporciona la frecuencia de muestreo y el número de canales después de aplicar las herramientas SBR y PS, si están presentes.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-132">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="d6e0c-133">wmcodecdsp.h</span><span class="sxs-lookup"><span data-stu-id="d6e0c-133">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="d6e0c-134">Para configurar el descodificador de AAC, establezca los siguientes atributos en el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-134">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6e0c-135">Atributo</span><span class="sxs-lookup"><span data-stu-id="d6e0c-135">Attribute</span></span></th>
<th><span data-ttu-id="d6e0c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e0c-136">Description</span></span></th>
<th><span data-ttu-id="d6e0c-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6e0c-137">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e0c-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-139">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-139">Major type.</span></span></td>
<td><span data-ttu-id="d6e0c-140">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-140">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-142">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-142">Audio subtype.</span></span></td>
<td><span data-ttu-id="d6e0c-143">Consulte la descripción anterior para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-143">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="d6e0c-145">Perfil y nivel de audio.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-145">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="d6e0c-146">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-146">Optional.</span></span> <span data-ttu-id="d6e0c-147">Solo se aplica a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-147">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="d6e0c-148">El valor de este atributo es el <strong>campo audioProfileLevelIndication,</strong> tal como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-148">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="d6e0c-149">Si es desconocido, establezca en cero o 0xFE ( &quot; no se especificó ningún perfil de audio &quot; ).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-149">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="d6e0c-151">Tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-151">Payload type.</span></span><br/></td>
<td><span data-ttu-id="d6e0c-152">Solo se aplica a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-152">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="d6e0c-153">El descodificador admite los siguientes tipos de carga:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-153">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="d6e0c-154">0: AAC sin formato.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-154">0: Raw AAC.</span></span> <span data-ttu-id="d6e0c-155">La secuencia solo raw_data_block(), tal como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-155">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="d6e0c-156">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-156">1: ADTS.</span></span> <span data-ttu-id="d6e0c-157">La secuencia contiene un adts_sequence(), tal como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-157">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="d6e0c-158">Solo se permite raw_data_block() por adts_frame().</span><span class="sxs-lookup"><span data-stu-id="d6e0c-158">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="d6e0c-159">3: Secuencia de transporte de audio con una capa de sincronización (LOAS) y una capa multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-159">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="d6e0c-160">De los tres tipos de LOAS, solo <strong>se admite AudioSyncStream.</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0c-160">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="d6e0c-161">La capa multiplex es <strong>AudioMuxElement,</strong>restringida a un programa de audio y una capa.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-161">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="d6e0c-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> es opcional.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="d6e0c-163">Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia solo raw_data_block elementos.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-163">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-165">Profundidad de bits deseada del audio PCM descodificado.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-165">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-167">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-167">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="d6e0c-168">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-168">Optional.</span></span> <span data-ttu-id="d6e0c-169">Para obtener más información, vea <a href="#format-constraints">Restricciones de formato</a>.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-169">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-171">Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-171">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="d6e0c-172">La interpretación de este valor depende del subtipo de medios, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-172">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-174">Frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-174">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="d6e0c-175">La interpretación de este valor depende del subtipo de medios, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-175">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-177">Información de formato adicional.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-177">Additional format information.</span></span></td>
<td><span data-ttu-id="d6e0c-178">El valor de este atributo depende del subtipo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-178">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="d6e0c-179"><strong>MFAudioFormat_AAC:</strong>contiene la parte de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece después de la estructura <strong>DESACWAVEATEX</strong> (es decir, después del <strong>miembro wfx).</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0c-179"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="d6e0c-180">Esto va seguido de los datos AudioSpecificConfig(), tal como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-180">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="d6e0c-181"><strong>MEDIASUBTYPE_RAW_AAC1:</strong>contiene los datos de AudioSpecificConfig().</span><span class="sxs-lookup"><span data-stu-id="d6e0c-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="d6e0c-182">Estos datos deben aparecer; De lo contrario, el descodificador rechazará el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-182">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="d6e0c-183">La longitud de los datos de AudioSpecificConfig() es de 2 bytes para AAC-LC o HE-AAC con señalización implícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-183">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="d6e0c-184">Es más de 2 bytes para HE-AAC con señalización explícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-184">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="d6e0c-185">El valor de <strong>audioObjectType</strong> tal como se define en AudioSpecificConfig() debe ser 2, lo que indica AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-185">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="d6e0c-186">El valor de <strong>extensionAudioObjectType</strong> debe ser 5 para SBR o 29 para PS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-186">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="d6e0c-187">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="d6e0c-187">Output Types</span></span>

<span data-ttu-id="d6e0c-188">El descodificador admite los siguientes tipos de salida:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-188">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6e0c-189">Subtype</span><span class="sxs-lookup"><span data-stu-id="d6e0c-189">Subtype</span></span></th>
<th><span data-ttu-id="d6e0c-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e0c-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e0c-191"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0c-191"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="d6e0c-192">Audio de punto flotante IEEE.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-192">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-193"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0c-193"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="d6e0c-194">Audio PCM de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-194">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-195"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="d6e0c-195"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="d6e0c-196">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-196">Requires Windows 8.</span></span> <br/> <span data-ttu-id="d6e0c-197">Este tipo de salida se puede usar para convertir una secuencia de AAC en el formato LOAS/LATM al formato ADTS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-197">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="d6e0c-198">Para convertir un flujo LOAS/LATM en un flujo de ADTS, establezca el tipo de entrada <strong>en MFAudioFormat_AAC</strong> con el tipo de carga 3 (LOAS).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-198">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="d6e0c-199">A continuación, establezca el tipo <strong>de salida MFAudioFormat_AAC</strong> con el tipo de carga 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-199">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="d6e0c-200">El descodificador volverá a formatear el conainter sin descodificar la secuencia de bits.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-200">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d6e0c-201">El descodificador no <strong>registra</strong> MFAudioFormat_AAC como un tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-201">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="d6e0c-202">Sin embargo, si la <strong>aplicación</strong> establece el tipo de entrada como se describe, el método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> devuelve MFAudioFormat_AAC en la lista de tipos de salida disponibles.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-202">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d6e0c-203">Si el flujo de entrada contiene más de dos canales, el descodificador de AAC proporciona dos opciones para el formato de salida:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-203">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="d6e0c-204">La misma configuración de canal que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-204">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="d6e0c-205">Plegado estéreo hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-205">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="d6e0c-206">Restricciones de formato</span><span class="sxs-lookup"><span data-stu-id="d6e0c-206">Format Constraints</span></span>

<span data-ttu-id="d6e0c-207">La frecuencia de muestreo de audio descodificado debe ser una de las siguientes, después de aplicar SBR (si está presente):</span><span class="sxs-lookup"><span data-stu-id="d6e0c-207">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="d6e0c-208">8 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-208">8 kHz</span></span>
-   <span data-ttu-id="d6e0c-209">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-209">11.025 kHz</span></span>
-   <span data-ttu-id="d6e0c-210">12 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-210">12 kHz</span></span>
-   <span data-ttu-id="d6e0c-211">16 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-211">16 kHz</span></span>
-   <span data-ttu-id="d6e0c-212">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-212">22.05 kHz</span></span>
-   <span data-ttu-id="d6e0c-213">24 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-213">24 kHz</span></span>
-   <span data-ttu-id="d6e0c-214">32 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-214">32 kHz</span></span>
-   <span data-ttu-id="d6e0c-215">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-215">44.1 kHz</span></span>
-   <span data-ttu-id="d6e0c-216">48 kHz</span><span class="sxs-lookup"><span data-stu-id="d6e0c-216">48 kHz</span></span>

<span data-ttu-id="d6e0c-217">No se admiten velocidades de muestreo superiores a 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-217">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="d6e0c-218">El descodificador admite hasta 6 canales de audio.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-218">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="d6e0c-219">Para cada configuración del hablante, el descodificador espera que los elementos sintácticos de AAC aparezcan en un orden determinado.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-219">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="d6e0c-220">En la tabla siguiente se enumeran las configuraciones admitidas del hablante.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-220">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="d6e0c-221">En la tercera columna de la tabla se enumeran los elementos sintácticos esperados y su orden, mediante la siguiente notación:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-221">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="d6e0c-222"><SCE1>: el single_channel_element (SCE) asociado al altavoz del centro frontal.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-222"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="d6e0c-223"><SCE2>: SCE asociado al altavoz del centro posterior.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-223"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="d6e0c-224"><CPE1>: el channel_pair_element (CPE) asociado a los altavoces frontales.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-224"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="d6e0c-225"><CPE2>: el CPE asociado a los altavoces de fondo (o lateral)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-225"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="d6e0c-226"><LFE>: el lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-226"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="d6e0c-227">Para obtener más información sobre estos elementos sintácticos, consulte ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-227">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="d6e0c-228">Configuración</span><span class="sxs-lookup"><span data-stu-id="d6e0c-228">Configuration</span></span>       | <span data-ttu-id="d6e0c-229">Máscara de canal</span><span class="sxs-lookup"><span data-stu-id="d6e0c-229">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="d6e0c-230">Elementos sintácticos de AAC</span><span class="sxs-lookup"><span data-stu-id="d6e0c-230">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d6e0c-231">Mono</span><span class="sxs-lookup"><span data-stu-id="d6e0c-231">Mono</span></span>                | <span data-ttu-id="d6e0c-232">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-232">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="d6e0c-233">Mono estéreo o dual</span><span class="sxs-lookup"><span data-stu-id="d6e0c-233">Stereo or dual mono</span></span> | <span data-ttu-id="d6e0c-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="d6e0c-235">2/1</span><span class="sxs-lookup"><span data-stu-id="d6e0c-235">2/1</span></span>                 | <span data-ttu-id="d6e0c-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="d6e0c-237">2/2</span><span class="sxs-lookup"><span data-stu-id="d6e0c-237">2/2</span></span>                 | <span data-ttu-id="d6e0c-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="d6e0c-239">3/0</span><span class="sxs-lookup"><span data-stu-id="d6e0c-239">3/0</span></span>                 | <span data-ttu-id="d6e0c-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="d6e0c-241">3/1</span><span class="sxs-lookup"><span data-stu-id="d6e0c-241">3/1</span></span>                 | <span data-ttu-id="d6e0c-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="d6e0c-243">3/2</span><span class="sxs-lookup"><span data-stu-id="d6e0c-243">3/2</span></span>                 | <span data-ttu-id="d6e0c-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="d6e0c-245">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="d6e0c-245">3/2 + LFE</span></span>           | <span data-ttu-id="d6e0c-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="d6e0c-247">En el caso de AAC sin procesar, cada ejemplo de entrada debe contener exactamente un marco comprimido de AAC completo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-247">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="d6e0c-248">Para ADTS, cada ejemplo de entrada puede contener varios fotogramas de audio, así como fotogramas parciales, es decir, los fotogramas pueden abarcar los límites de la muestra.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-248">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="d6e0c-249">Cada encabezado de ADTS debe ir seguido de un marco de AAC.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-249">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="d6e0c-250">El descodificador de AAC no admite ninguno de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-250">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="d6e0c-251">Perfil principal, Sample-Rate perfil escalable (SRS) o perfil de predicción a largo plazo (LTP).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-251">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="d6e0c-252">Formato de intercambio de datos de audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-252">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="d6e0c-253">Secuencias de transporte LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-253">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="d6e0c-254">Elementos de canal de acoplamiento (CCE).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-254">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="d6e0c-255">El descodificador omitirá los fotogramas de audio con LOS CCE.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-255">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="d6e0c-256">AAC-LC con un tamaño de marco de 960 muestras.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-256">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="d6e0c-257">Solo se admiten 1024 fotogramas de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-257">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="d6e0c-258">Transformar atributos</span><span class="sxs-lookup"><span data-stu-id="d6e0c-258">Transform Attributes</span></span>

<span data-ttu-id="d6e0c-259">El descodificador de AAC implementa el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-259">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="d6e0c-260">Las aplicaciones pueden usar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-260">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6e0c-261">Atributo</span><span class="sxs-lookup"><span data-stu-id="d6e0c-261">Attribute</span></span></th>
<th><span data-ttu-id="d6e0c-262">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e0c-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6e0c-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-264">Especifica si el audio de 2 canales se codifica como estéreo o mono dual.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-264">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="d6e0c-265">Tratar como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-265">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6e0c-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-267">Especifica cómo el descodificador reproduce el audio mono dual.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-267">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="d6e0c-268">El valor predeterminado es <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>salida Ch1 a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-268">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="d6e0c-269">Las aplicaciones pueden establecer esta propiedad para cambiar el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-269">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6e0c-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d6e0c-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="d6e0c-271">El descodificador de AAC no controla los cambios de formato dinámico y se debe vaciar o purgar antes de establecer un nuevo tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-271">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="d6e0c-272">Trate este atributo como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-272">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d6e0c-273">El descodificador de AAC notifica incorrectamente un valor <strong>de TRUE</strong> para este atributo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-273">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="d6e0c-274">En Windows 7, el descodificador notifica incorrectamente un valor de <strong>TRUE</strong> para este atributo.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-274">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="d6e0c-275">En Windows 8, el descodificador notifica <strong>FALSE</strong>, que es el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-275">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="d6e0c-276">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6e0c-276">Example Media Types</span></span>

<span data-ttu-id="d6e0c-277">Este es un ejemplo del tipo de medio de entrada necesario para una secuencia AAC-LC de 6 canales y 48 kHz, mediante una carga de AAC sin formato:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-277">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="d6e0c-278">Atributo</span><span class="sxs-lookup"><span data-stu-id="d6e0c-278">Attribute</span></span>                                                                                      | <span data-ttu-id="d6e0c-279">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e0c-279">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6e0c-280">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-280">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="d6e0c-281">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-281">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="d6e0c-282">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-282">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="d6e0c-283">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-283">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="d6e0c-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="d6e0c-285">48000</span><span class="sxs-lookup"><span data-stu-id="d6e0c-285">48000</span></span>                                                                                |
| [<span data-ttu-id="d6e0c-286">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-286">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="d6e0c-287">6</span><span class="sxs-lookup"><span data-stu-id="d6e0c-287">6</span></span>                                                                                    |
| [<span data-ttu-id="d6e0c-288">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="d6e0c-288">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="d6e0c-289">0</span><span class="sxs-lookup"><span data-stu-id="d6e0c-289">0</span></span>                                                                                    |
| [<span data-ttu-id="d6e0c-290">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-290">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="d6e0c-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="d6e0c-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="d6e0c-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="d6e0c-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="d6e0c-293">0x2a (opcional)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-293">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="d6e0c-294">Los primeros 12 bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) corresponden a los siguientes miembros de la estructura [**HEAACWAVEINFO:**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-294">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="d6e0c-295">**wPayloadType** = 0 (AAC sin procesar)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-295">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="d6e0c-296">**wAudioProfileLevelIndication** = 0x2a (perfil de AAC, nivel 4)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-296">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="d6e0c-297">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="d6e0c-297">**wStructType** = 0</span></span>

<span data-ttu-id="d6e0c-298">Los dos últimos bytes [**de MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contienen el valor de AudioSpecificConfig(), tal como se define en MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="d6e0c-298">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="d6e0c-299">AudioSpecificConfig.audioObjectType = 2 (LC de AAC) (5 bits)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="d6e0c-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="d6e0c-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="d6e0c-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="d6e0c-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="d6e0c-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="d6e0c-305">Dado este tipo de entrada, use el siguiente tipo de medio de salida para obtener audio PCM de punto flotante de 6 canales y 32 bits del descodificador:</span><span class="sxs-lookup"><span data-stu-id="d6e0c-305">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="d6e0c-306">Atributo</span><span class="sxs-lookup"><span data-stu-id="d6e0c-306">Attribute</span></span>                                                                                    | <span data-ttu-id="d6e0c-307">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e0c-307">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="d6e0c-308">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-308">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="d6e0c-309">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-309">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="d6e0c-310">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-310">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="d6e0c-311">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-311">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="d6e0c-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="d6e0c-313">32</span><span class="sxs-lookup"><span data-stu-id="d6e0c-313">32</span></span>                       |
| [<span data-ttu-id="d6e0c-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="d6e0c-315">48000</span><span class="sxs-lookup"><span data-stu-id="d6e0c-315">48000</span></span>                    |
| [<span data-ttu-id="d6e0c-316">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-316">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="d6e0c-317">6</span><span class="sxs-lookup"><span data-stu-id="d6e0c-317">6</span></span>                        |
| [<span data-ttu-id="d6e0c-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="d6e0c-319">1152000 (opcional)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-319">1152000 (optional)</span></span>       |
| [<span data-ttu-id="d6e0c-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="d6e0c-321">24 (opcional)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-321">24 (optional)</span></span>            |
| [<span data-ttu-id="d6e0c-322">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-322">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="d6e0c-323">0x3f (opcional)</span><span class="sxs-lookup"><span data-stu-id="d6e0c-323">0x3f (optional)</span></span>          |



 

<span data-ttu-id="d6e0c-324">Si está instalado el complemento de actualización de plataforma para Windows Vista, el descodificador de audio AAC está disponible en Windows Vista, pero solo se puede acceder a él en Windows Vista mediante el Lector [de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="d6e0c-324">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e0c-325">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e0c-325">Requirements</span></span>



| <span data-ttu-id="d6e0c-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e0c-326">Requirement</span></span> | <span data-ttu-id="d6e0c-327">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e0c-327">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e0c-328">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e0c-328">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e0c-329">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6e0c-329">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="d6e0c-330">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e0c-330">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e0c-331">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="d6e0c-331">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="d6e0c-332">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6e0c-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6e0c-333"><dt>Msmpeg2adec.dll en Windows 7; </dt> <dt>MSAudDecMFT.dll en Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="d6e0c-333"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e0c-334">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6e0c-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e0c-335">Objetos de códec</span><span class="sxs-lookup"><span data-stu-id="d6e0c-335">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="d6e0c-336">Tipos de medios de AAC</span><span class="sxs-lookup"><span data-stu-id="d6e0c-336">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="d6e0c-337">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="d6e0c-337">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="d6e0c-338">**Descodificador de audio Microsoft MPEG-1/DD/AAC**</span><span class="sxs-lookup"><span data-stu-id="d6e0c-338">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="d6e0c-339">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6e0c-339">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d6e0c-340">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6e0c-340">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
