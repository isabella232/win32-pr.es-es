---
description: El codificador de audio Dolby es una transformación de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby Digital, también denominado Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Dolby Digital Audio Encoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153568"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="494f3-103">Dolby Digital Audio Encoder</span><span class="sxs-lookup"><span data-stu-id="494f3-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="494f3-104">El codificador de audio Dolby es una [transformación](media-foundation-transforms.md) de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby Digital, también denominado Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="494f3-104">The Dolby audio encoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="494f3-105">El codificador no admite la entrada multicanal, como la configuración del canal 5.1.</span><span class="sxs-lookup"><span data-stu-id="494f3-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="494f3-106">Para las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en los términos del programa de licencias Dolby Digital para que las usen las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="494f3-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="494f3-107">Para obtener más información sobre el audio Dolby Digital, consulte el documento del Comité de sistemas de televisión avanzados (ATSC) *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span><span class="sxs-lookup"><span data-stu-id="494f3-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="494f3-108">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="494f3-108">Class Identifier</span></span>

<span data-ttu-id="494f3-109">El identificador de clase (CLSID) del codificador de audio Dolby es **\_ CLSID CMSDolbyDigitalEncMFT**, definido en el archivo de encabezado wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="494f3-109">The class identifier (CLSID) of the Dolby audio encoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="494f3-110">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="494f3-110">Output Types</span></span>

<span data-ttu-id="494f3-111">El tipo de salida debe establecerse primero, antes que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="494f3-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="494f3-112">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="494f3-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="494f3-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="494f3-113">Attribute</span></span></th>
<th><span data-ttu-id="494f3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="494f3-114">Description</span></span></th>
<th><span data-ttu-id="494f3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="494f3-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="494f3-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="494f3-117">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="494f3-117">Major type.</span></span></td>
<td><span data-ttu-id="494f3-118">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-118">Required.</span></span> <span data-ttu-id="494f3-119">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="494f3-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="494f3-121">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="494f3-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="494f3-122">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-122">Required.</span></span> <span data-ttu-id="494f3-123">Debe ser <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="494f3-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="494f3-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="494f3-125">Ejemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="494f3-125">Samples per second.</span></span></td>
<td><span data-ttu-id="494f3-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-126">Required.</span></span> <span data-ttu-id="494f3-127">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="494f3-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="494f3-128">32000</span><span class="sxs-lookup"><span data-stu-id="494f3-128">32000</span></span></li>
<li><span data-ttu-id="494f3-129">44100</span><span class="sxs-lookup"><span data-stu-id="494f3-129">44100</span></span></li>
<li><span data-ttu-id="494f3-130">48000</span><span class="sxs-lookup"><span data-stu-id="494f3-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="494f3-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="494f3-132">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="494f3-132">Number of channels.</span></span></td>
<td><span data-ttu-id="494f3-133">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-133">Required.</span></span> <span data-ttu-id="494f3-134">Debe ser 1 (mono) o 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="494f3-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="494f3-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="494f3-136">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="494f3-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="494f3-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494f3-137">Optional.</span></span> <span data-ttu-id="494f3-138">Si se establece, el valor debe ser 0x3 para estéreo (canales delante izquierdo y derecho) o 0x4 para mono (canal front-center).</span><span class="sxs-lookup"><span data-stu-id="494f3-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="494f3-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="494f3-140">Velocidad de bits de la secuencia AC-3 codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="494f3-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="494f3-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494f3-141">Optional.</span></span> <span data-ttu-id="494f3-142">Vea Comentarios para obtener valores válidos.</span><span class="sxs-lookup"><span data-stu-id="494f3-142">See Remarks for valid values.</span></span> <span data-ttu-id="494f3-143">Si no se establece este atributo, el codificador usa una velocidad de bits predeterminada, como se describe en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="494f3-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="494f3-144">Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.</span><span class="sxs-lookup"><span data-stu-id="494f3-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="494f3-145">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="494f3-145">Input Types</span></span>

<span data-ttu-id="494f3-146">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="494f3-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="494f3-147">Atributo</span><span class="sxs-lookup"><span data-stu-id="494f3-147">Attribute</span></span></th>
<th><span data-ttu-id="494f3-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="494f3-148">Description</span></span></th>
<th><span data-ttu-id="494f3-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="494f3-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="494f3-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="494f3-151">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="494f3-151">Major type.</span></span></td>
<td><span data-ttu-id="494f3-152">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-152">Required.</span></span> <span data-ttu-id="494f3-153">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="494f3-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="494f3-155">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="494f3-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="494f3-156">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-156">Required.</span></span> <span data-ttu-id="494f3-157">Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="494f3-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="494f3-159">Número de bits por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="494f3-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="494f3-160">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-160">Required.</span></span> <span data-ttu-id="494f3-161">El valor debe ser 16 si el subtipo <strong>es MFAudioFormat_PCM</strong>o 32 si el subtipo <strong>es MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="494f3-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="494f3-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="494f3-163">Ejemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="494f3-163">Samples per second.</span></span></td>
<td><span data-ttu-id="494f3-164">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-164">Required.</span></span> <span data-ttu-id="494f3-165">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="494f3-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="494f3-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="494f3-167">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="494f3-167">Number of channels.</span></span></td>
<td><span data-ttu-id="494f3-168">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-168">Required.</span></span> <span data-ttu-id="494f3-169">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="494f3-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="494f3-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="494f3-171">Alineación de bloques, en bytes.</span><span class="sxs-lookup"><span data-stu-id="494f3-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="494f3-172">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-172">Required.</span></span> <span data-ttu-id="494f3-173">Calcule el valor como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="494f3-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="494f3-174"><strong>MFAudioFormat_PCM:</strong>número de canales × 2.</span><span class="sxs-lookup"><span data-stu-id="494f3-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="494f3-175"><strong>MFAudioFormat_Float:</strong>número de canales × 4.</span><span class="sxs-lookup"><span data-stu-id="494f3-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="494f3-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="494f3-177">Velocidad de bits de la secuencia AC3 codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="494f3-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="494f3-178">Necesario.</span><span class="sxs-lookup"><span data-stu-id="494f3-178">Required.</span></span> <span data-ttu-id="494f3-179">Debe ser igual a la alineación × muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="494f3-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="494f3-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="494f3-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="494f3-181">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="494f3-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="494f3-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494f3-182">Optional.</span></span> <span data-ttu-id="494f3-183">Si se establece, el valor debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="494f3-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="494f3-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="494f3-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="494f3-185">Número de bits válidos de datos de audio en cada muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="494f3-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="494f3-186">Opcional.</span><span class="sxs-lookup"><span data-stu-id="494f3-186">Optional.</span></span> <span data-ttu-id="494f3-187">Si se establece, el valor debe ser idéntico <a href="mf-mt-audio-bits-per-sample-attribute.md">al MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="494f3-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="494f3-188">El codificador no admite la conversión de frecuencia de muestreo ni la conversión estéreo/mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="494f3-189">Comentarios</span><span class="sxs-lookup"><span data-stu-id="494f3-189">Remarks</span></span>

<span data-ttu-id="494f3-190">Cada fotograma de audio Dolby AC-3 contiene 1536 muestras de audio por canal.</span><span class="sxs-lookup"><span data-stu-id="494f3-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="494f3-191">Sin embargo, cada búfer de entrada al codificador puede contener cualquier número de muestras de PCM.</span><span class="sxs-lookup"><span data-stu-id="494f3-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="494f3-192">El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque.</span><span class="sxs-lookup"><span data-stu-id="494f3-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="494f3-193">El codificador almacena en caché los ejemplos de entrada hasta que tiene suficiente para 1536 muestras de audio por canal. momento en el que el codificador genera un fotograma AC-3.</span><span class="sxs-lookup"><span data-stu-id="494f3-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="494f3-194">Cada búfer de salida contiene un marco AC-3 sin procesar.</span><span class="sxs-lookup"><span data-stu-id="494f3-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="494f3-195">La duración es equivalente a la duración de 1536 muestras de PCM con la frecuencia de muestreo actual (32 ms) a 48 kHz, 34,83 ms a 44,1 kHz y 48 ms a 32 kHz).</span><span class="sxs-lookup"><span data-stu-id="494f3-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="494f3-196">El tamaño de cada búfer de salida depende de la velocidad de bits y la frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="494f3-197">Para especificar la velocidad de bits de codificación, establezca el atributo [MF MT AUDIO AVG BYTES PER \_ \_ \_ \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="494f3-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="494f3-198">En la tabla siguiente se muestra la relación entre la velocidad de bits de codificación y LOS BYTES PROMEDIO \_ DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO.</span><span class="sxs-lookup"><span data-stu-id="494f3-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="494f3-199">Velocidad de bits (kbps)</span><span class="sxs-lookup"><span data-stu-id="494f3-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="494f3-200">PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO</span><span class="sxs-lookup"><span data-stu-id="494f3-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="494f3-201">Comentarios</span><span class="sxs-lookup"><span data-stu-id="494f3-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="494f3-202">64</span><span class="sxs-lookup"><span data-stu-id="494f3-202">64</span></span>              | <span data-ttu-id="494f3-203">8000</span><span class="sxs-lookup"><span data-stu-id="494f3-203">8000</span></span>                                                                                     | <span data-ttu-id="494f3-204">Solo Mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-204">Mono only.</span></span>                                              |
| <span data-ttu-id="494f3-205">80</span><span class="sxs-lookup"><span data-stu-id="494f3-205">80</span></span>              | <span data-ttu-id="494f3-206">10000</span><span class="sxs-lookup"><span data-stu-id="494f3-206">10000</span></span>                                                                                    | <span data-ttu-id="494f3-207">Solo Mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-207">Mono only.</span></span>                                              |
| <span data-ttu-id="494f3-208">96</span><span class="sxs-lookup"><span data-stu-id="494f3-208">96</span></span>              | <span data-ttu-id="494f3-209">12000</span><span class="sxs-lookup"><span data-stu-id="494f3-209">12000</span></span>                                                                                    | <span data-ttu-id="494f3-210">Solo Mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-210">Mono only.</span></span>                                              |
| <span data-ttu-id="494f3-211">112</span><span class="sxs-lookup"><span data-stu-id="494f3-211">112</span></span>             | <span data-ttu-id="494f3-212">14000</span><span class="sxs-lookup"><span data-stu-id="494f3-212">14000</span></span>                                                                                    | <span data-ttu-id="494f3-213">Solo Mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-213">Mono only.</span></span>                                              |
| <span data-ttu-id="494f3-214">128</span><span class="sxs-lookup"><span data-stu-id="494f3-214">128</span></span>             | <span data-ttu-id="494f3-215">16000</span><span class="sxs-lookup"><span data-stu-id="494f3-215">16000</span></span>                                                                                    | <span data-ttu-id="494f3-216">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="494f3-217">160</span><span class="sxs-lookup"><span data-stu-id="494f3-217">160</span></span>             | <span data-ttu-id="494f3-218">20000</span><span class="sxs-lookup"><span data-stu-id="494f3-218">20000</span></span>                                                                                    | <span data-ttu-id="494f3-219">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="494f3-220">192</span><span class="sxs-lookup"><span data-stu-id="494f3-220">192</span></span>             | <span data-ttu-id="494f3-221">24000</span><span class="sxs-lookup"><span data-stu-id="494f3-221">24000</span></span>                                                                                    | <span data-ttu-id="494f3-222">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-222">Mono or stereo.</span></span> <span data-ttu-id="494f3-223">Esta es la configuración predeterminada para mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="494f3-224">224</span><span class="sxs-lookup"><span data-stu-id="494f3-224">224</span></span>             | <span data-ttu-id="494f3-225">28000</span><span class="sxs-lookup"><span data-stu-id="494f3-225">28000</span></span>                                                                                    | <span data-ttu-id="494f3-226">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="494f3-227">256</span><span class="sxs-lookup"><span data-stu-id="494f3-227">256</span></span>             | <span data-ttu-id="494f3-228">32000</span><span class="sxs-lookup"><span data-stu-id="494f3-228">32000</span></span>                                                                                    | <span data-ttu-id="494f3-229">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-229">Mono or stereo.</span></span> <span data-ttu-id="494f3-230">Esta es la configuración predeterminada para estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="494f3-231">320</span><span class="sxs-lookup"><span data-stu-id="494f3-231">320</span></span>             | <span data-ttu-id="494f3-232">40000</span><span class="sxs-lookup"><span data-stu-id="494f3-232">40000</span></span>                                                                                    | <span data-ttu-id="494f3-233">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="494f3-234">384</span><span class="sxs-lookup"><span data-stu-id="494f3-234">384</span></span>             | <span data-ttu-id="494f3-235">48000</span><span class="sxs-lookup"><span data-stu-id="494f3-235">48000</span></span>                                                                                    | <span data-ttu-id="494f3-236">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="494f3-237">448</span><span class="sxs-lookup"><span data-stu-id="494f3-237">448</span></span>             | <span data-ttu-id="494f3-238">56 000</span><span class="sxs-lookup"><span data-stu-id="494f3-238">56000</span></span>                                                                                    | <span data-ttu-id="494f3-239">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="494f3-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="494f3-240">La velocidad de bits de codificación predeterminada se establece en 256 kbps para estéreo y 192 kbps para mono.</span><span class="sxs-lookup"><span data-stu-id="494f3-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="494f3-241">La configuración predeterminada se refleja en los tipos de medios devueltos por el método [**IMFTransform::GetOutputAvailableType del**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) codificador.</span><span class="sxs-lookup"><span data-stu-id="494f3-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="494f3-242">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="494f3-242">Example Media Types</span></span>

<span data-ttu-id="494f3-243">Este es un ejemplo de los tipos de medios necesarios para codificar un PCM entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada de 256 kbps.</span><span class="sxs-lookup"><span data-stu-id="494f3-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="494f3-244">Tipo de medio de salida:</span><span class="sxs-lookup"><span data-stu-id="494f3-244">Output media type:</span></span>

| <span data-ttu-id="494f3-245">Atributo</span><span class="sxs-lookup"><span data-stu-id="494f3-245">Attribute</span></span>                                                                           | <span data-ttu-id="494f3-246">Valor</span><span class="sxs-lookup"><span data-stu-id="494f3-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="494f3-247">TIPO \_ PRINCIPAL DE MT \_ DE \_ MF</span><span class="sxs-lookup"><span data-stu-id="494f3-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="494f3-248">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="494f3-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="494f3-249">\_SUBTIPO DE MT DE MF \_</span><span class="sxs-lookup"><span data-stu-id="494f3-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="494f3-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="494f3-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="494f3-251">MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO</span><span class="sxs-lookup"><span data-stu-id="494f3-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="494f3-252">48000</span><span class="sxs-lookup"><span data-stu-id="494f3-252">48000</span></span>                         |
| [<span data-ttu-id="494f3-253">CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT</span><span class="sxs-lookup"><span data-stu-id="494f3-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="494f3-254">2</span><span class="sxs-lookup"><span data-stu-id="494f3-254">2</span></span>                             |



 

<span data-ttu-id="494f3-255">Tipo de medio de entrada:</span><span class="sxs-lookup"><span data-stu-id="494f3-255">Input media type:</span></span>

| <span data-ttu-id="494f3-256">Atributo</span><span class="sxs-lookup"><span data-stu-id="494f3-256">Attribute</span></span>                                                                                | <span data-ttu-id="494f3-257">Valor</span><span class="sxs-lookup"><span data-stu-id="494f3-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="494f3-258">TIPO \_ PRINCIPAL DE MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="494f3-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="494f3-259">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="494f3-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="494f3-260">\_SUBTIPO MT DE MF \_</span><span class="sxs-lookup"><span data-stu-id="494f3-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="494f3-261">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="494f3-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="494f3-262">BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ EJEMPLO</span><span class="sxs-lookup"><span data-stu-id="494f3-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="494f3-263">16</span><span class="sxs-lookup"><span data-stu-id="494f3-263">16</span></span>                     |
| [<span data-ttu-id="494f3-264">MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO</span><span class="sxs-lookup"><span data-stu-id="494f3-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="494f3-265">48000</span><span class="sxs-lookup"><span data-stu-id="494f3-265">48000</span></span>                  |
| [<span data-ttu-id="494f3-266">CANALES \_ NUM \_ DE AUDIO \_ MF MT \_</span><span class="sxs-lookup"><span data-stu-id="494f3-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="494f3-267">2</span><span class="sxs-lookup"><span data-stu-id="494f3-267">2</span></span>                      |
| [<span data-ttu-id="494f3-268">ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO \_ \_ MF MT</span><span class="sxs-lookup"><span data-stu-id="494f3-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="494f3-269">4</span><span class="sxs-lookup"><span data-stu-id="494f3-269">4</span></span>                      |
| [<span data-ttu-id="494f3-270">PROMEDIO \_ DE BYTES PROMEDIO DE AUDIO MF MT POR \_ \_ \_ \_ \_ SEGUNDO</span><span class="sxs-lookup"><span data-stu-id="494f3-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="494f3-271">192000</span><span class="sxs-lookup"><span data-stu-id="494f3-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="494f3-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="494f3-272">Requirements</span></span>



| <span data-ttu-id="494f3-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="494f3-273">Requirement</span></span> | <span data-ttu-id="494f3-274">Valor</span><span class="sxs-lookup"><span data-stu-id="494f3-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="494f3-275">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="494f3-275">Minimum supported client</span></span><br/> | <span data-ttu-id="494f3-276">Windows 8 aplicaciones \[ de escritorio \| para aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="494f3-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="494f3-277">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="494f3-277">Minimum supported server</span></span><br/> | <span data-ttu-id="494f3-278">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="494f3-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="494f3-279">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="494f3-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="494f3-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="494f3-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="494f3-281">Consulte también</span><span class="sxs-lookup"><span data-stu-id="494f3-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="494f3-282">Objetos de códec</span><span class="sxs-lookup"><span data-stu-id="494f3-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




