---
description: El descodificador de audio Dolby es una transformación de Media Foundation (MFT) que codifica audio mono o estéreo en Dolby digital, también denominado Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificador Dolby digital audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705413"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="6c879-103">Codificador Dolby digital audio</span><span class="sxs-lookup"><span data-stu-id="6c879-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="6c879-104">El descodificador de audio Dolby es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que codifica audio mono o estéreo en Dolby digital, también denominado Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="6c879-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="6c879-105">El codificador no admite la entrada de varios canales, como la configuración del canal 5,1.</span><span class="sxs-lookup"><span data-stu-id="6c879-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c879-106">En el caso de las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en lo que respecta al programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c879-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="6c879-107">Para obtener más información acerca del audio Dolby digital, consulte el documento sobre el Comité de sistemas de televisión avanzado (ATSC) ( *AC-3, E-AC-3) revisión B*.</span><span class="sxs-lookup"><span data-stu-id="6c879-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="6c879-108">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="6c879-108">Class Identifier</span></span>

<span data-ttu-id="6c879-109">El identificador de clase (CLSID) del descodificador de audio Dolby es **CLSID \_ CMSDolbyDigitalEncMFT**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="6c879-109">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="6c879-110">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="6c879-110">Output Types</span></span>

<span data-ttu-id="6c879-111">Primero se debe establecer el tipo de salida, antes del tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c879-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="6c879-112">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="6c879-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c879-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="6c879-113">Attribute</span></span></th>
<th><span data-ttu-id="6c879-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c879-114">Description</span></span></th>
<th><span data-ttu-id="6c879-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c879-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c879-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="6c879-117">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="6c879-117">Major type.</span></span></td>
<td><span data-ttu-id="6c879-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-118">Required.</span></span> <span data-ttu-id="6c879-119">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c879-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="6c879-121">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="6c879-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="6c879-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-122">Required.</span></span> <span data-ttu-id="6c879-123">Debe ser <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c879-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="6c879-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="6c879-125">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-125">Samples per second.</span></span></td>
<td><span data-ttu-id="6c879-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-126">Required.</span></span> <span data-ttu-id="6c879-127">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="6c879-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="6c879-128">32000</span><span class="sxs-lookup"><span data-stu-id="6c879-128">32000</span></span></li>
<li><span data-ttu-id="6c879-129">44100</span><span class="sxs-lookup"><span data-stu-id="6c879-129">44100</span></span></li>
<li><span data-ttu-id="6c879-130">48000</span><span class="sxs-lookup"><span data-stu-id="6c879-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="6c879-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="6c879-132">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="6c879-132">Number of channels.</span></span></td>
<td><span data-ttu-id="6c879-133">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-133">Required.</span></span> <span data-ttu-id="6c879-134">Debe ser 1 (mono) o 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="6c879-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="6c879-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="6c879-136">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="6c879-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="6c879-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c879-137">Optional.</span></span> <span data-ttu-id="6c879-138">Si se establece, el valor debe ser 0X3 para los canales estéreo (Front izquierdo y derecho) o 0x4 para mono (canal de centro frontal).</span><span class="sxs-lookup"><span data-stu-id="6c879-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="6c879-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="6c879-140">Velocidad de bits de la secuencia AC-3 codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="6c879-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c879-141">Optional.</span></span> <span data-ttu-id="6c879-142">Vea la sección Comentarios para ver los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="6c879-142">See Remarks for valid values.</span></span> <span data-ttu-id="6c879-143">Si no se establece este atributo, el codificador utiliza una velocidad de bits predeterminada, como se describe en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="6c879-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6c879-144">Si no se establecen los atributos opcionales, el codificador los agrega al tipo de medio después de establecer el tipo.</span><span class="sxs-lookup"><span data-stu-id="6c879-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="6c879-145">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="6c879-145">Input Types</span></span>

<span data-ttu-id="6c879-146">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c879-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c879-147">Atributo</span><span class="sxs-lookup"><span data-stu-id="6c879-147">Attribute</span></span></th>
<th><span data-ttu-id="6c879-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c879-148">Description</span></span></th>
<th><span data-ttu-id="6c879-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c879-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c879-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="6c879-151">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="6c879-151">Major type.</span></span></td>
<td><span data-ttu-id="6c879-152">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-152">Required.</span></span> <span data-ttu-id="6c879-153">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c879-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="6c879-155">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="6c879-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="6c879-156">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-156">Required.</span></span> <span data-ttu-id="6c879-157">Debe ser <strong>MFAudioFormat_PCM</strong> o <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c879-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="6c879-159">Número de bits por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="6c879-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="6c879-160">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-160">Required.</span></span> <span data-ttu-id="6c879-161">El valor debe ser 16 si el subtipo es <strong>MFAudioFormat_PCM</strong>, o 32 si el subtipo es <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c879-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="6c879-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="6c879-163">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-163">Samples per second.</span></span></td>
<td><span data-ttu-id="6c879-164">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-164">Required.</span></span> <span data-ttu-id="6c879-165">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="6c879-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="6c879-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="6c879-167">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="6c879-167">Number of channels.</span></span></td>
<td><span data-ttu-id="6c879-168">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-168">Required.</span></span> <span data-ttu-id="6c879-169">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="6c879-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="6c879-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="6c879-171">Alineación de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6c879-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="6c879-172">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-172">Required.</span></span> <span data-ttu-id="6c879-173">Calcule el valor de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6c879-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="6c879-174"><strong>MFAudioFormat_PCM</strong>: número de canales × 2.</span><span class="sxs-lookup"><span data-stu-id="6c879-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="6c879-175"><strong>MFAudioFormat_Float</strong>: número de canales × 4.</span><span class="sxs-lookup"><span data-stu-id="6c879-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="6c879-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="6c879-177">Velocidad de bits de la secuencia de AC3s codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="6c879-178">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c879-178">Required.</span></span> <span data-ttu-id="6c879-179">Debe ser igual que la alineación de bloque × ejemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c879-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="6c879-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="6c879-181">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="6c879-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="6c879-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c879-182">Optional.</span></span> <span data-ttu-id="6c879-183">Si se establece, el valor debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="6c879-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c879-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="6c879-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="6c879-185">Número de bits válidos de datos de audio en cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="6c879-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="6c879-186">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6c879-186">Optional.</span></span> <span data-ttu-id="6c879-187">Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="6c879-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6c879-188">El codificador no admite la conversión de velocidad de muestra o la conversión estéreo/mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c879-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c879-189">Remarks</span></span>

<span data-ttu-id="6c879-190">Cada fotograma de audio Dolby AC-3 contiene 1536 muestras de audio por canal.</span><span class="sxs-lookup"><span data-stu-id="6c879-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="6c879-191">Sin embargo, cada búfer de entrada del codificador puede contener cualquier número de muestras de PCM.</span><span class="sxs-lookup"><span data-stu-id="6c879-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="6c879-192">El tamaño de cada búfer de entrada debe ser un múltiplo de la alineación del bloque.</span><span class="sxs-lookup"><span data-stu-id="6c879-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="6c879-193">El codificador almacena en caché los ejemplos de entrada hasta que tiene suficiente para 1536 muestras de audio por canal. en ese momento, el codificador genera un fotograma AC-3.</span><span class="sxs-lookup"><span data-stu-id="6c879-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="6c879-194">Cada búfer de salida contiene un marco AC-3 sin procesar.</span><span class="sxs-lookup"><span data-stu-id="6c879-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="6c879-195">La duración es equivalente a la duración de las muestras de 1536 PCM con la frecuencia de muestreo actual (32 ms) a la velocidad de muestra de 48 kHz, 34,83 MS en 44,1 kHz y 48 MS a 32 kHz).</span><span class="sxs-lookup"><span data-stu-id="6c879-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="6c879-196">El tamaño de cada búfer de salida depende de la velocidad de bits y la velocidad de muestra.</span><span class="sxs-lookup"><span data-stu-id="6c879-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="6c879-197">Para especificar la velocidad de bits de codificación, establezca el atributo [MF \_ MT \_ audio \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) en el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="6c879-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="6c879-198">En la tabla siguiente se muestra la relación entre la velocidad de bits de codificación y los \_ \_ bytes promedio de audio MF MT \_ \_ \_ por \_ segundo.</span><span class="sxs-lookup"><span data-stu-id="6c879-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="6c879-199">Velocidad de bits (kbps)</span><span class="sxs-lookup"><span data-stu-id="6c879-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="6c879-200">\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="6c879-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="6c879-201">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c879-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6c879-202">64</span><span class="sxs-lookup"><span data-stu-id="6c879-202">64</span></span>              | <span data-ttu-id="6c879-203">8000</span><span class="sxs-lookup"><span data-stu-id="6c879-203">8000</span></span>                                                                                     | <span data-ttu-id="6c879-204">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-204">Mono only.</span></span>                                              |
| <span data-ttu-id="6c879-205">80</span><span class="sxs-lookup"><span data-stu-id="6c879-205">80</span></span>              | <span data-ttu-id="6c879-206">10000</span><span class="sxs-lookup"><span data-stu-id="6c879-206">10000</span></span>                                                                                    | <span data-ttu-id="6c879-207">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-207">Mono only.</span></span>                                              |
| <span data-ttu-id="6c879-208">96</span><span class="sxs-lookup"><span data-stu-id="6c879-208">96</span></span>              | <span data-ttu-id="6c879-209">12000</span><span class="sxs-lookup"><span data-stu-id="6c879-209">12000</span></span>                                                                                    | <span data-ttu-id="6c879-210">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-210">Mono only.</span></span>                                              |
| <span data-ttu-id="6c879-211">112</span><span class="sxs-lookup"><span data-stu-id="6c879-211">112</span></span>             | <span data-ttu-id="6c879-212">14000</span><span class="sxs-lookup"><span data-stu-id="6c879-212">14000</span></span>                                                                                    | <span data-ttu-id="6c879-213">Solo mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-213">Mono only.</span></span>                                              |
| <span data-ttu-id="6c879-214">128</span><span class="sxs-lookup"><span data-stu-id="6c879-214">128</span></span>             | <span data-ttu-id="6c879-215">16000</span><span class="sxs-lookup"><span data-stu-id="6c879-215">16000</span></span>                                                                                    | <span data-ttu-id="6c879-216">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="6c879-217">160</span><span class="sxs-lookup"><span data-stu-id="6c879-217">160</span></span>             | <span data-ttu-id="6c879-218">20000</span><span class="sxs-lookup"><span data-stu-id="6c879-218">20000</span></span>                                                                                    | <span data-ttu-id="6c879-219">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="6c879-220">192</span><span class="sxs-lookup"><span data-stu-id="6c879-220">192</span></span>             | <span data-ttu-id="6c879-221">24000</span><span class="sxs-lookup"><span data-stu-id="6c879-221">24000</span></span>                                                                                    | <span data-ttu-id="6c879-222">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-222">Mono or stereo.</span></span> <span data-ttu-id="6c879-223">Esta es la configuración predeterminada de mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="6c879-224">224</span><span class="sxs-lookup"><span data-stu-id="6c879-224">224</span></span>             | <span data-ttu-id="6c879-225">28000</span><span class="sxs-lookup"><span data-stu-id="6c879-225">28000</span></span>                                                                                    | <span data-ttu-id="6c879-226">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="6c879-227">256</span><span class="sxs-lookup"><span data-stu-id="6c879-227">256</span></span>             | <span data-ttu-id="6c879-228">32000</span><span class="sxs-lookup"><span data-stu-id="6c879-228">32000</span></span>                                                                                    | <span data-ttu-id="6c879-229">Mono o estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-229">Mono or stereo.</span></span> <span data-ttu-id="6c879-230">Esta es la configuración predeterminada de estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="6c879-231">320</span><span class="sxs-lookup"><span data-stu-id="6c879-231">320</span></span>             | <span data-ttu-id="6c879-232">40000</span><span class="sxs-lookup"><span data-stu-id="6c879-232">40000</span></span>                                                                                    | <span data-ttu-id="6c879-233">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="6c879-234">384</span><span class="sxs-lookup"><span data-stu-id="6c879-234">384</span></span>             | <span data-ttu-id="6c879-235">48000</span><span class="sxs-lookup"><span data-stu-id="6c879-235">48000</span></span>                                                                                    | <span data-ttu-id="6c879-236">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="6c879-237">448</span><span class="sxs-lookup"><span data-stu-id="6c879-237">448</span></span>             | <span data-ttu-id="6c879-238">56 000</span><span class="sxs-lookup"><span data-stu-id="6c879-238">56000</span></span>                                                                                    | <span data-ttu-id="6c879-239">Solo estéreo.</span><span class="sxs-lookup"><span data-stu-id="6c879-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="6c879-240">La velocidad de bits de codificación predeterminada está establecida en 256 kbps para estéreo y 192 kbps para mono.</span><span class="sxs-lookup"><span data-stu-id="6c879-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="6c879-241">La configuración predeterminada se refleja en los tipos de medios devueltos por el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) del codificador.</span><span class="sxs-lookup"><span data-stu-id="6c879-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="6c879-242">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c879-242">Example Media Types</span></span>

<span data-ttu-id="6c879-243">A continuación se muestra un ejemplo de los tipos de medios que se necesitan para codificar el PCM de entero de 16 bits, audio estéreo de 48 kHz a la velocidad de bits predeterminada de 256 kbps.</span><span class="sxs-lookup"><span data-stu-id="6c879-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="6c879-244">Tipo de medio de salida:</span><span class="sxs-lookup"><span data-stu-id="6c879-244">Output media type:</span></span>

| <span data-ttu-id="6c879-245">Atributo</span><span class="sxs-lookup"><span data-stu-id="6c879-245">Attribute</span></span>                                                                           | <span data-ttu-id="6c879-246">Value</span><span class="sxs-lookup"><span data-stu-id="6c879-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="6c879-247">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="6c879-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="6c879-248">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6c879-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="6c879-249">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="6c879-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="6c879-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="6c879-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="6c879-251">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="6c879-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="6c879-252">48000</span><span class="sxs-lookup"><span data-stu-id="6c879-252">48000</span></span>                         |
| [<span data-ttu-id="6c879-253">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c879-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="6c879-254">2</span><span class="sxs-lookup"><span data-stu-id="6c879-254">2</span></span>                             |



 

<span data-ttu-id="6c879-255">Tipo de medio de entrada:</span><span class="sxs-lookup"><span data-stu-id="6c879-255">Input media type:</span></span>

| <span data-ttu-id="6c879-256">Atributo</span><span class="sxs-lookup"><span data-stu-id="6c879-256">Attribute</span></span>                                                                                | <span data-ttu-id="6c879-257">Value</span><span class="sxs-lookup"><span data-stu-id="6c879-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="6c879-258">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="6c879-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="6c879-259">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6c879-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="6c879-260">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="6c879-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="6c879-261">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="6c879-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="6c879-262">MF \_ MT \_ audio \_ bits \_ por \_ muestra</span><span class="sxs-lookup"><span data-stu-id="6c879-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="6c879-263">16</span><span class="sxs-lookup"><span data-stu-id="6c879-263">16</span></span>                     |
| [<span data-ttu-id="6c879-264">\_muestras de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="6c879-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="6c879-265">48000</span><span class="sxs-lookup"><span data-stu-id="6c879-265">48000</span></span>                  |
| [<span data-ttu-id="6c879-266">\_canales de \_ número de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c879-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="6c879-267">2</span><span class="sxs-lookup"><span data-stu-id="6c879-267">2</span></span>                      |
| [<span data-ttu-id="6c879-268">\_alineación del \_ bloque de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="6c879-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="6c879-269">4</span><span class="sxs-lookup"><span data-stu-id="6c879-269">4</span></span>                      |
| [<span data-ttu-id="6c879-270">\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="6c879-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="6c879-271">192000</span><span class="sxs-lookup"><span data-stu-id="6c879-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="6c879-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c879-272">Requirements</span></span>



| <span data-ttu-id="6c879-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c879-273">Requirement</span></span> | <span data-ttu-id="6c879-274">Value</span><span class="sxs-lookup"><span data-stu-id="6c879-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c879-275">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c879-275">Minimum supported client</span></span><br/> | <span data-ttu-id="6c879-276">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="6c879-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="6c879-277">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c879-277">Minimum supported server</span></span><br/> | <span data-ttu-id="6c879-278">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6c879-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6c879-279">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c879-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c879-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c879-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c879-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c879-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c879-282">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="6c879-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




