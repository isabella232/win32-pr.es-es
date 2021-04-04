---
description: El codificador de audio MPEG-2 Microsoft Media Foundation es una transformación Media Foundation que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o MPEG-2 (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908377"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="2b8d5-103">Codificador de audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="2b8d5-104">El codificador de audio MPEG-2 Microsoft Media Foundation es una [transformación Media Foundation](media-foundation-transforms.md) que codifica audio mono o estéreo en audio MPEG-1 (ISO/IEC 11172-3) o MPEG-2 (ISO/IEC 13818-3).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="2b8d5-105">El codificador admite el audio de nivel 1 y nivel 2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="2b8d5-106">No admite audio de MPEG-Layer 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="2b8d5-107">En MPEG-2, el codificador admite la parte de bajas frecuencias de muestreo (LSF) del audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="2b8d5-108">No es compatible con las extensiones multicanal.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="2b8d5-109">La MFT genera una secuencia MPEG elemental.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="2b8d5-110">No puede generar secuencias elementales con paquetes, secuencias de programa o flujos de transporte.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="2b8d5-111">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="2b8d5-111">Class Identifier</span></span>

<span data-ttu-id="2b8d5-112">El identificador de clase (CLSID) del codificador de audio MEPG-2 es **CLSID \_ CMPEG2AudioEncoderMFT**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="2b8d5-113">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="2b8d5-113">Output Types</span></span>

<span data-ttu-id="2b8d5-114">Primero se debe establecer el tipo de salida, antes del tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="2b8d5-115">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b8d5-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-116">Attribute</span></span></th>
<th><span data-ttu-id="2b8d5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b8d5-117">Description</span></span></th>
<th><span data-ttu-id="2b8d5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8d5-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b8d5-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="2b8d5-120">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-120">Major type.</span></span></td>
<td><span data-ttu-id="2b8d5-121">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-121">Required.</span></span> <span data-ttu-id="2b8d5-122">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="2b8d5-124">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="2b8d5-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-125">Required.</span></span> <span data-ttu-id="2b8d5-126">Debe ser <strong>MFAudioFormat_MPEG</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="2b8d5-127">Este subtipo se usa para audio MPEG-1 y MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="2b8d5-129">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-129">Samples per second.</span></span></td>
<td><span data-ttu-id="2b8d5-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-130">Required.</span></span> <span data-ttu-id="2b8d5-131">En MPEG-1 y MPEG-2 se admiten los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="2b8d5-132">32000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-132">32000</span></span></li>
<li><span data-ttu-id="2b8d5-133">44100</span><span class="sxs-lookup"><span data-stu-id="2b8d5-133">44100</span></span></li>
<li><span data-ttu-id="2b8d5-134">48000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-134">48000</span></span></li>
</ul>
<span data-ttu-id="2b8d5-135">Además, se admiten los siguientes valores para MPEG-2 LSF:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="2b8d5-136">16000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-136">16000</span></span></li>
<li><span data-ttu-id="2b8d5-137">22050</span><span class="sxs-lookup"><span data-stu-id="2b8d5-137">22050</span></span></li>
<li><span data-ttu-id="2b8d5-138">24000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="2b8d5-140">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-140">Number of channels.</span></span></td>
<td><span data-ttu-id="2b8d5-141">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-141">Required.</span></span> <span data-ttu-id="2b8d5-142">Debe ser 1 (mono) o 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="2b8d5-144">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="2b8d5-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-145">Optional.</span></span> <span data-ttu-id="2b8d5-146">Si se establece, el valor debe ser 0X3 para los canales estéreo (Front izquierdo y derecho) o 0x4 para mono (canal de centro frontal).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="2b8d5-148">Velocidad de bits de la secuencia MPEG codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="2b8d5-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-149">Optional.</span></span><br/> <span data-ttu-id="2b8d5-150">Las especificaciones ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definen varias velocidades de bits, en función de la frecuencia de muestreo, el número de canales y la capa de audio (1 o 2).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="2b8d5-151">El codificador tiene como valor predeterminado el audio de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="2b8d5-152">Si no se establece el atributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> , el codificador utiliza las siguientes velocidades de bits predeterminadas:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="2b8d5-153">MPEG-1 estéreo: 224.000 bits por segundo (BPS) = 28.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="2b8d5-154">MPEG-1 mono: 192.000 BPS = 24.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="2b8d5-155">MPEG-2 LSF, mono o estéreo: 160.000 BPS = 20.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="2b8d5-156">Este atributo se puede establecer en otros valores.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-156">This attribute can be set to other values.</span></span> <span data-ttu-id="2b8d5-157">Si el valor no es válido de acuerdo con las especificaciones de MPEG, el MFT rechazará el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="2b8d5-158">También puede establecer la velocidad de bits mediante la interfaz <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b8d5-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="2b8d5-159">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2b8d5-160">Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="2b8d5-161">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="2b8d5-161">Input Types</span></span>

<span data-ttu-id="2b8d5-162">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b8d5-163">Atributo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-163">Attribute</span></span></th>
<th><span data-ttu-id="2b8d5-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b8d5-164">Description</span></span></th>
<th><span data-ttu-id="2b8d5-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8d5-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b8d5-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="2b8d5-167">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-167">Major type.</span></span></td>
<td><span data-ttu-id="2b8d5-168">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-168">Required.</span></span> <span data-ttu-id="2b8d5-169">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="2b8d5-171">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="2b8d5-172">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-172">Required.</span></span> <span data-ttu-id="2b8d5-173">Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="2b8d5-175">Número de bits por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="2b8d5-176">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-176">Required.</span></span> <span data-ttu-id="2b8d5-177">El valor debe ser 16 si el subtipo es <strong>MFAudioFormat_PCM</strong>, o 32 si el subtipo es <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="2b8d5-179">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-179">Samples per second.</span></span></td>
<td><span data-ttu-id="2b8d5-180">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-180">Required.</span></span> <span data-ttu-id="2b8d5-181">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="2b8d5-183">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-183">Number of channels.</span></span></td>
<td><span data-ttu-id="2b8d5-184">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-184">Required.</span></span> <span data-ttu-id="2b8d5-185">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="2b8d5-187">Alineación de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="2b8d5-188">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-188">Required.</span></span> <span data-ttu-id="2b8d5-189">Calcule el valor de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="2b8d5-190"><strong>MFAudioFormat_PCM</strong>: número de canales × 2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="2b8d5-191"><strong>MFAudioFormat_Float</strong>: número de canales × 4.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="2b8d5-193">Velocidad de bits de la secuencia de AC3s codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="2b8d5-194">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-194">Required.</span></span> <span data-ttu-id="2b8d5-195">Debe ser igual que la alineación de bloque × ejemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b8d5-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="2b8d5-197">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="2b8d5-198">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-198">Optional.</span></span> <span data-ttu-id="2b8d5-199">Si se establece, el valor debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b8d5-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="2b8d5-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="2b8d5-201">Número de bits válidos de datos de audio en cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="2b8d5-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-202">Optional.</span></span> <span data-ttu-id="2b8d5-203">Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2b8d5-204">El codificador no admite la conversión de velocidad de muestra o la conversión estéreo/mono.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="2b8d5-205">Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="2b8d5-206">Propiedades de códec</span><span class="sxs-lookup"><span data-stu-id="2b8d5-206">Codec Properties</span></span>

<span data-ttu-id="2b8d5-207">El codificador admite las siguientes propiedades a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="2b8d5-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="2b8d5-208">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b8d5-208">Property</span></span>                                                                                | <span data-ttu-id="2b8d5-209">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b8d5-209">Description</span></span>                                                                                      | <span data-ttu-id="2b8d5-210">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2b8d5-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b8d5-211">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="2b8d5-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="2b8d5-212">Especifica la velocidad media de bits codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="2b8d5-213">Tal y como se describe en el atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="2b8d5-214">CODECAPI \_ AVEncMPACodingMode</span><span class="sxs-lookup"><span data-stu-id="2b8d5-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="2b8d5-215">Especifica el modo de codificación de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="2b8d5-216">Estéreo para audio de 2 canales o canal único para audio de un canal.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="2b8d5-217">En el caso de audio de 2 canales, el codificador también admite canal dual y estéreo en conjunto.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="2b8d5-218">CODECAPI \_ AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="2b8d5-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="2b8d5-219">Especifica si se debe establecer el bit de copyright en la secuencia de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="2b8d5-220">Sin derechos de autor.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="2b8d5-221">CODECAPI \_ AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="2b8d5-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="2b8d5-222">Especifica el tipo de filtro de desacentuación que se debe usar cuando se descodifica el flujo codificado.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="2b8d5-223">No se ha especificado ningún énfasis.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="2b8d5-224">AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="2b8d5-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="2b8d5-225">Especifica si se debe agregar una comprobación de redundancia cíclica (CRC) al encabezado del marco.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="2b8d5-226">Una suma de comprobación de CRC se escribe en la secuencia de bits.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="2b8d5-227">CODECAPI \_ AVEncMPALayer</span><span class="sxs-lookup"><span data-stu-id="2b8d5-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="2b8d5-228">Especifica la capa de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="2b8d5-229">Audio de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="2b8d5-230">CODECAPI \_ AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="2b8d5-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="2b8d5-231">Especifica si se va a establecer para el bit original de la secuencia de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="2b8d5-232">El bit "original" está desactivado.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="2b8d5-233">CODECAPI \_ AVEncMPAPrivateUserBit</span><span class="sxs-lookup"><span data-stu-id="2b8d5-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="2b8d5-234">Especifica si se debe establecer para el bit de usuario privado en la secuencia de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="2b8d5-235">El bit de usuario privado está desactivado.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="2b8d5-236">Para obtener un puntero a la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , llame a [**QUERYINTERFACE**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la MFT.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="2b8d5-237">MFT implementa los siguientes métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="2b8d5-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="2b8d5-238">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="2b8d5-239">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="2b8d5-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="2b8d5-241">**IsModifiable**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="2b8d5-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="2b8d5-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="2b8d5-244">Todos los demás métodos de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) devuelven **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8d5-245">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8d5-245">Remarks</span></span>

<span data-ttu-id="2b8d5-246">Cada fotograma de audio MPEG contiene muestras de audio de 384 (capa 1) o 1152 (capa 2) por canal.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="2b8d5-247">Sin embargo, cada búfer de entrada del codificador puede contener cualquier número de muestras de PCM.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="2b8d5-248">El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="2b8d5-249">El codificador almacena en caché los ejemplos de entrada hasta que sea suficiente para una trama de audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="2b8d5-250">Cada búfer de salida contiene un fotograma MPEG sin formato.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="2b8d5-251">El tamaño de cada búfer de salida depende de la velocidad de bits y la velocidad de muestra.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="2b8d5-252">Configurar el codificador</span><span class="sxs-lookup"><span data-stu-id="2b8d5-252">Configuring the Encoder</span></span>

<span data-ttu-id="2b8d5-253">Para cambiar cualquiera de las opciones de configuración predeterminadas del codificador, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="2b8d5-254">Cree una instancia de la MFT del codificador.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="2b8d5-255">Llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obtener la lista de los tipos de salida preferidos.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="2b8d5-256">El codificador enumera todas las velocidades de muestra para mono y estéreo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="2b8d5-257">Seleccione uno de estos tipos de medios, en función de la velocidad de muestra y el número de canales.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="2b8d5-258">El atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) indica la velocidad de bits predeterminada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="2b8d5-259">Opcional: puede invalidar la velocidad de bits predeterminada si establece un nuevo valor para [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="2b8d5-260">Las velocidades de bits válidas dependen de la velocidad de muestra, el número de canales y el nivel de audio.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="2b8d5-261">En este punto del proceso de configuración, el codificador tiene como valor predeterminado audio de nivel 2 y solo acepta velocidades de bits de capa 2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="2b8d5-262">Podrá cambiar el codificador a la capa 1 en un paso posterior (consulte el paso 7).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="2b8d5-263">En ese caso, deje la velocidad de bits predeterminada por ahora; puede cambiarla de nuevo en el paso 8.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="2b8d5-264">Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="2b8d5-265">Si establece su propio valor para [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) y el MFT rechaza el tipo de medio de salida, es probable que haya especificado una velocidad de bits no válida.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="2b8d5-266">Llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para enumerar el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="2b8d5-267">Dado que la velocidad de muestra y el número de canales deben ser idénticos al tipo de salida, solo se enumeran dos opciones: entrada PCM de punto flotante de 32 bits y entrada PCM de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="2b8d5-268">Seleccione una de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-268">Select one of these.</span></span>
6.  <span data-ttu-id="2b8d5-269">Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="2b8d5-270">Opcional: para codificar el audio de nivel 1, establezca la propiedad [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) en **eAVEncMPALayer \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="2b8d5-271">Opcional: para cambiar la velocidad de bits, establezca la propiedad [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="2b8d5-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="2b8d5-272">La velocidad de bits debe ser una de las velocidades de bits válidas que se enumeran en las especificaciones de LSF MPEG-1 o MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="2b8d5-273">Como alternativa, puede llamar a [**ICodecAPI:: GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obtener una lista de velocidades de bits válidas, basándose en la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="2b8d5-274">Opcional: con audio de 2 canales, puede establecer la propiedad [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para cambiar el modo de codificación a canal dual o estéreo en conjunto.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="2b8d5-275">Puede llamar a [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obtener las opciones válidas.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="2b8d5-276">(Para audio de un canal, la única opción es mono).</span><span class="sxs-lookup"><span data-stu-id="2b8d5-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="2b8d5-277">Opcional: establezca cualquiera de las demás propiedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) enumeradas previamente.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="2b8d5-278">Es importante seguir el orden de estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="2b8d5-279">En concreto, establezca el tipo de medio de salida antes de cambiar las propiedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="2b8d5-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="2b8d5-280">Además, debe establecer las propiedades de **ICodecAPI** antes de que el MFT reciba la primera muestra de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="2b8d5-281">Después de que el MFT reciba entradas, las propiedades del códec son de solo lectura y [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) devuelve el valor **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="2b8d5-282">Velocidades de bits admitidas</span><span class="sxs-lookup"><span data-stu-id="2b8d5-282">Supported Bit Rates</span></span>

<span data-ttu-id="2b8d5-283">El codificador admite las siguientes velocidades de bits.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="2b8d5-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="2b8d5-284">MPEG-1</span></span>

<span data-ttu-id="2b8d5-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-285">MPEG-2</span></span>

<span data-ttu-id="2b8d5-286">Nivel 1</span><span class="sxs-lookup"><span data-stu-id="2b8d5-286">Layer 1</span></span>

<span data-ttu-id="2b8d5-287">Nivel 2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-287">Layer 2</span></span>

<span data-ttu-id="2b8d5-288">Nivel 1</span><span class="sxs-lookup"><span data-stu-id="2b8d5-288">Layer 1</span></span>

<span data-ttu-id="2b8d5-289">Nivel 2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-289">Layer 2</span></span>

<span data-ttu-id="2b8d5-290">32</span><span class="sxs-lookup"><span data-stu-id="2b8d5-290">32</span></span>

<span data-ttu-id="2b8d5-291">32\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-291">32\*</span></span>

<span data-ttu-id="2b8d5-292">32</span><span class="sxs-lookup"><span data-stu-id="2b8d5-292">32</span></span>

<span data-ttu-id="2b8d5-293">8</span><span class="sxs-lookup"><span data-stu-id="2b8d5-293">8</span></span>

<span data-ttu-id="2b8d5-294">64</span><span class="sxs-lookup"><span data-stu-id="2b8d5-294">64</span></span>

<span data-ttu-id="2b8d5-295">48\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-295">48\*</span></span>

<span data-ttu-id="2b8d5-296">38</span><span class="sxs-lookup"><span data-stu-id="2b8d5-296">38</span></span>

<span data-ttu-id="2b8d5-297">16</span><span class="sxs-lookup"><span data-stu-id="2b8d5-297">16</span></span>

<span data-ttu-id="2b8d5-298">96</span><span class="sxs-lookup"><span data-stu-id="2b8d5-298">96</span></span>

<span data-ttu-id="2b8d5-299">56\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-299">56\*</span></span>

<span data-ttu-id="2b8d5-300">56</span><span class="sxs-lookup"><span data-stu-id="2b8d5-300">56</span></span>

<span data-ttu-id="2b8d5-301">24</span><span class="sxs-lookup"><span data-stu-id="2b8d5-301">24</span></span>

<span data-ttu-id="2b8d5-302">128</span><span class="sxs-lookup"><span data-stu-id="2b8d5-302">128</span></span>

<span data-ttu-id="2b8d5-303">64</span><span class="sxs-lookup"><span data-stu-id="2b8d5-303">64</span></span>

<span data-ttu-id="2b8d5-304">64</span><span class="sxs-lookup"><span data-stu-id="2b8d5-304">64</span></span>

<span data-ttu-id="2b8d5-305">32</span><span class="sxs-lookup"><span data-stu-id="2b8d5-305">32</span></span>

<span data-ttu-id="2b8d5-306">160</span><span class="sxs-lookup"><span data-stu-id="2b8d5-306">160</span></span>

<span data-ttu-id="2b8d5-307">80\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-307">80\*</span></span>

<span data-ttu-id="2b8d5-308">80</span><span class="sxs-lookup"><span data-stu-id="2b8d5-308">80</span></span>

<span data-ttu-id="2b8d5-309">40</span><span class="sxs-lookup"><span data-stu-id="2b8d5-309">40</span></span>

<span data-ttu-id="2b8d5-310">192</span><span class="sxs-lookup"><span data-stu-id="2b8d5-310">192</span></span>

<span data-ttu-id="2b8d5-311">96</span><span class="sxs-lookup"><span data-stu-id="2b8d5-311">96</span></span>

<span data-ttu-id="2b8d5-312">96</span><span class="sxs-lookup"><span data-stu-id="2b8d5-312">96</span></span>

<span data-ttu-id="2b8d5-313">48</span><span class="sxs-lookup"><span data-stu-id="2b8d5-313">48</span></span>

<span data-ttu-id="2b8d5-314">224</span><span class="sxs-lookup"><span data-stu-id="2b8d5-314">224</span></span>

<span data-ttu-id="2b8d5-315">112</span><span class="sxs-lookup"><span data-stu-id="2b8d5-315">112</span></span>

<span data-ttu-id="2b8d5-316">112</span><span class="sxs-lookup"><span data-stu-id="2b8d5-316">112</span></span>

<span data-ttu-id="2b8d5-317">56</span><span class="sxs-lookup"><span data-stu-id="2b8d5-317">56</span></span>

<span data-ttu-id="2b8d5-318">256</span><span class="sxs-lookup"><span data-stu-id="2b8d5-318">256</span></span>

<span data-ttu-id="2b8d5-319">128</span><span class="sxs-lookup"><span data-stu-id="2b8d5-319">128</span></span>

<span data-ttu-id="2b8d5-320">128</span><span class="sxs-lookup"><span data-stu-id="2b8d5-320">128</span></span>

<span data-ttu-id="2b8d5-321">64</span><span class="sxs-lookup"><span data-stu-id="2b8d5-321">64</span></span>

<span data-ttu-id="2b8d5-322">288</span><span class="sxs-lookup"><span data-stu-id="2b8d5-322">288</span></span>

<span data-ttu-id="2b8d5-323">160</span><span class="sxs-lookup"><span data-stu-id="2b8d5-323">160</span></span>

<span data-ttu-id="2b8d5-324">144</span><span class="sxs-lookup"><span data-stu-id="2b8d5-324">144</span></span>

<span data-ttu-id="2b8d5-325">80</span><span class="sxs-lookup"><span data-stu-id="2b8d5-325">80</span></span>

<span data-ttu-id="2b8d5-326">320</span><span class="sxs-lookup"><span data-stu-id="2b8d5-326">320</span></span>

<span data-ttu-id="2b8d5-327">192</span><span class="sxs-lookup"><span data-stu-id="2b8d5-327">192</span></span>

<span data-ttu-id="2b8d5-328">160</span><span class="sxs-lookup"><span data-stu-id="2b8d5-328">160</span></span>

<span data-ttu-id="2b8d5-329">96</span><span class="sxs-lookup"><span data-stu-id="2b8d5-329">96</span></span>

<span data-ttu-id="2b8d5-330">352</span><span class="sxs-lookup"><span data-stu-id="2b8d5-330">352</span></span>

<span data-ttu-id="2b8d5-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-331">224\*\*</span></span>

<span data-ttu-id="2b8d5-332">176</span><span class="sxs-lookup"><span data-stu-id="2b8d5-332">176</span></span>

<span data-ttu-id="2b8d5-333">112</span><span class="sxs-lookup"><span data-stu-id="2b8d5-333">112</span></span>

<span data-ttu-id="2b8d5-334">384</span><span class="sxs-lookup"><span data-stu-id="2b8d5-334">384</span></span>

<span data-ttu-id="2b8d5-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-335">256\*\*</span></span>

<span data-ttu-id="2b8d5-336">192</span><span class="sxs-lookup"><span data-stu-id="2b8d5-336">192</span></span>

<span data-ttu-id="2b8d5-337">128</span><span class="sxs-lookup"><span data-stu-id="2b8d5-337">128</span></span>

<span data-ttu-id="2b8d5-338">416</span><span class="sxs-lookup"><span data-stu-id="2b8d5-338">416</span></span>

<span data-ttu-id="2b8d5-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-339">230\*\*</span></span>

<span data-ttu-id="2b8d5-340">224</span><span class="sxs-lookup"><span data-stu-id="2b8d5-340">224</span></span>

<span data-ttu-id="2b8d5-341">144</span><span class="sxs-lookup"><span data-stu-id="2b8d5-341">144</span></span>

<span data-ttu-id="2b8d5-342">448</span><span class="sxs-lookup"><span data-stu-id="2b8d5-342">448</span></span>

<span data-ttu-id="2b8d5-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="2b8d5-343">384\*\*</span></span>

<span data-ttu-id="2b8d5-344">256</span><span class="sxs-lookup"><span data-stu-id="2b8d5-344">256</span></span>

<span data-ttu-id="2b8d5-345">160</span><span class="sxs-lookup"><span data-stu-id="2b8d5-345">160</span></span>



 

<dl> <span data-ttu-id="2b8d5-346">\* Solo mono</span><span class="sxs-lookup"><span data-stu-id="2b8d5-346">\* Mono only</span></span>  
<span data-ttu-id="2b8d5-347">\*\* Solo estéreo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="2b8d5-348">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-348">Example Media Types</span></span>

<span data-ttu-id="2b8d5-349">Este es un ejemplo de los tipos de medios que se necesitan para codificar el PCM de entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2b8d5-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="2b8d5-350">Tipo de medio de salida:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-350">Output media type:</span></span>

| <span data-ttu-id="2b8d5-351">Atributo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-351">Attribute</span></span>                                                                           | <span data-ttu-id="2b8d5-352">Value</span><span class="sxs-lookup"><span data-stu-id="2b8d5-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="2b8d5-353">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="2b8d5-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="2b8d5-354">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="2b8d5-355">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="2b8d5-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="2b8d5-356">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="2b8d5-357">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="2b8d5-358">48000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-358">48000</span></span>                   |
| [<span data-ttu-id="2b8d5-359">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2b8d5-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="2b8d5-360">2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-360">2</span></span>                       |



 

<span data-ttu-id="2b8d5-361">Tipo de medio de entrada:</span><span class="sxs-lookup"><span data-stu-id="2b8d5-361">Input media type:</span></span>

| <span data-ttu-id="2b8d5-362">Atributo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-362">Attribute</span></span>                                                                                | <span data-ttu-id="2b8d5-363">Value</span><span class="sxs-lookup"><span data-stu-id="2b8d5-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="2b8d5-364">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="2b8d5-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="2b8d5-365">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="2b8d5-366">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="2b8d5-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="2b8d5-367">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="2b8d5-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="2b8d5-368">MF \_ MT \_ audio \_ bits \_ por \_ muestra</span><span class="sxs-lookup"><span data-stu-id="2b8d5-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="2b8d5-369">16</span><span class="sxs-lookup"><span data-stu-id="2b8d5-369">16</span></span>                     |
| [<span data-ttu-id="2b8d5-370">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="2b8d5-371">48000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-371">48000</span></span>                  |
| [<span data-ttu-id="2b8d5-372">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2b8d5-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="2b8d5-373">2</span><span class="sxs-lookup"><span data-stu-id="2b8d5-373">2</span></span>                      |
| [<span data-ttu-id="2b8d5-374">\_alineación del \_ bloque de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2b8d5-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="2b8d5-375">4</span><span class="sxs-lookup"><span data-stu-id="2b8d5-375">4</span></span>                      |
| [<span data-ttu-id="2b8d5-376">\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="2b8d5-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="2b8d5-377">192000</span><span class="sxs-lookup"><span data-stu-id="2b8d5-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="2b8d5-378">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8d5-378">Requirements</span></span>



| <span data-ttu-id="2b8d5-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8d5-379">Requirement</span></span> | <span data-ttu-id="2b8d5-380">Value</span><span class="sxs-lookup"><span data-stu-id="2b8d5-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8d5-381">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d5-381">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8d5-382">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b8d5-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2b8d5-383">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d5-383">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8d5-384">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2b8d5-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2b8d5-385">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b8d5-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8d5-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d5-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8d5-387">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8d5-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8d5-388">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="2b8d5-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
