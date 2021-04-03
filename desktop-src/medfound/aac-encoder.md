---
description: El codificador AAC Microsoft Media Foundation es una transformación de Media Foundation que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal y como se define en ISO/IEC 13818-7 (la parte 7 de audio MPEG-2).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908044"
---
# <a name="aac-encoder"></a><span data-ttu-id="62482-103">Codificador AAC</span><span class="sxs-lookup"><span data-stu-id="62482-103">AAC Encoder</span></span>

<span data-ttu-id="62482-104">El codificador AAC Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) que codifica el perfil de baja complejidad (LC) de codificación de audio avanzada (AAC), tal y como se define en ISO/IEC 13818-7 (la parte 7 de audio MPEG-2).</span><span class="sxs-lookup"><span data-stu-id="62482-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="62482-105">El codificador AAC no admite la codificación en ningún otro perfil AAC, como Main, SSR o LTP.</span><span class="sxs-lookup"><span data-stu-id="62482-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="62482-106">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="62482-106">Class Identifier</span></span>

<span data-ttu-id="62482-107">El identificador de clase (CLSID) del codificador AAC es **CLSID \_ AACMFTEncoder**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="62482-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="62482-108">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="62482-108">Media Types</span></span>

<span data-ttu-id="62482-109">El codificador AAC admite los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="62482-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="62482-110">En primer lugar, puede establecer los tipos en el tipo de entrada de orden primero o en el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="62482-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="62482-111">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="62482-111">Input Types</span></span>

<span data-ttu-id="62482-112">Establezca los siguientes atributos en el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="62482-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62482-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="62482-113">Attribute</span></span></th>
<th><span data-ttu-id="62482-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="62482-114">Description</span></span></th>
<th><span data-ttu-id="62482-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62482-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62482-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="62482-117">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="62482-117">Major type.</span></span></td>
<td><span data-ttu-id="62482-118">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="62482-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="62482-120">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="62482-120">Subtype.</span></span></td>
<td><span data-ttu-id="62482-121">Debe ser <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="62482-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62482-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="62482-123">Bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="62482-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="62482-124">Debe ser 16.</span><span class="sxs-lookup"><span data-stu-id="62482-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="62482-126">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="62482-126">Samples per second.</span></span></td>
<td><span data-ttu-id="62482-127">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="62482-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="62482-128">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="62482-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="62482-129">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="62482-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62482-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="62482-131">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="62482-131">Number of channels.</span></span></td>
<td><span data-ttu-id="62482-132">Debe ser 1 (mono) o 2 (estéreo) o 6 (5,1).</span><span class="sxs-lookup"><span data-stu-id="62482-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="62482-133">La compatibilidad con 6 canales de audio se presentó con Windows 10 y no está disponible para versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="62482-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="62482-134">Una vez establecido el tipo de entrada, el codificador deriva los valores siguientes y los agrega al tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="62482-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="62482-135">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="62482-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="62482-136">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="62482-137">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="62482-138">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="62482-138">Output Types</span></span>

<span data-ttu-id="62482-139">Establezca los siguientes atributos en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="62482-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62482-140">Atributo</span><span class="sxs-lookup"><span data-stu-id="62482-140">Attribute</span></span></th>
<th><span data-ttu-id="62482-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="62482-141">Description</span></span></th>
<th><span data-ttu-id="62482-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62482-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62482-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="62482-144">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="62482-144">Major type.</span></span></td>
<td><span data-ttu-id="62482-145">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="62482-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="62482-147">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="62482-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="62482-148">Debe ser <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="62482-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62482-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="62482-150">Bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="62482-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="62482-151">Debe ser 16.</span><span class="sxs-lookup"><span data-stu-id="62482-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="62482-153">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="62482-153">Samples per second.</span></span></td>
<td><span data-ttu-id="62482-154">Debe coincidir con el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="62482-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62482-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="62482-156">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="62482-156">Number of channels.</span></span></td>
<td><span data-ttu-id="62482-157">Debe coincidir con el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="62482-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="62482-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="62482-159">Velocidad de bits de la secuencia AAC codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="62482-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="62482-160">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="62482-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="62482-161">12000</span><span class="sxs-lookup"><span data-stu-id="62482-161">12000</span></span></li>
<li><span data-ttu-id="62482-162">16000</span><span class="sxs-lookup"><span data-stu-id="62482-162">16000</span></span></li>
<li><span data-ttu-id="62482-163">20000</span><span class="sxs-lookup"><span data-stu-id="62482-163">20000</span></span></li>
<li><span data-ttu-id="62482-164">24000</span><span class="sxs-lookup"><span data-stu-id="62482-164">24000</span></span></li>
</ul>
<span data-ttu-id="62482-165">El valor predeterminado para mono y estéreo es 12000 (96 kbps).</span><span class="sxs-lookup"><span data-stu-id="62482-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62482-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="62482-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="62482-167">El tipo de carga AAC.</span><span class="sxs-lookup"><span data-stu-id="62482-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="62482-168">Opcional.</span><span class="sxs-lookup"><span data-stu-id="62482-168">Optional.</span></span> <span data-ttu-id="62482-169">Si se establece, el valor debe ser cero, lo que indica que el flujo solo contiene elementos raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="62482-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="62482-170">Opcional.</span><span class="sxs-lookup"><span data-stu-id="62482-170">Optional.</span></span> <span data-ttu-id="62482-171">Si no se establece el atributo, el valor predeterminado es cero, lo que indica que el flujo solo contiene elementos raw_data_block (AAC sin formato).</span><span class="sxs-lookup"><span data-stu-id="62482-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="62482-172">En Windows 7, si se establece este atributo, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="62482-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="62482-173">A partir de Windows 8, el valor puede ser 0 (AAC sin formato) o 1 (ADTS AAC).</span><span class="sxs-lookup"><span data-stu-id="62482-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62482-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="62482-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="62482-175">El perfil de audio AAC y el nivel.</span><span class="sxs-lookup"><span data-stu-id="62482-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="62482-176">Opcional.</span><span class="sxs-lookup"><span data-stu-id="62482-176">Optional.</span></span> <span data-ttu-id="62482-177">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="62482-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="62482-178">0x29 (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="62482-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="62482-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="62482-179">0x2A</span></span></li>
<li><span data-ttu-id="62482-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="62482-180">0x2B</span></span></li>
<li><span data-ttu-id="62482-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="62482-181">0x2C</span></span></li>
<li><span data-ttu-id="62482-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="62482-182">0x2E</span></span></li>
<li><span data-ttu-id="62482-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="62482-183">0x2F</span></span></li>
<li><span data-ttu-id="62482-184">0x30</span><span class="sxs-lookup"><span data-stu-id="62482-184">0x30</span></span></li>
<li><span data-ttu-id="62482-185">0x31</span><span class="sxs-lookup"><span data-stu-id="62482-185">0x31</span></span></li>
<li><span data-ttu-id="62482-186">0x32</span><span class="sxs-lookup"><span data-stu-id="62482-186">0x32</span></span></li>
<li><span data-ttu-id="62482-187">0x33</span><span class="sxs-lookup"><span data-stu-id="62482-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="62482-188">En la tabla siguiente se enumeran los valores que se pueden usar para el atributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.</span><span class="sxs-lookup"><span data-stu-id="62482-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="62482-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION valor</span><span class="sxs-lookup"><span data-stu-id="62482-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="62482-190">Perfil</span><span class="sxs-lookup"><span data-stu-id="62482-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="62482-191">0x29</span><span class="sxs-lookup"><span data-stu-id="62482-191">0x29</span></span>                                     | <span data-ttu-id="62482-192">Perfil de AAC L2</span><span class="sxs-lookup"><span data-stu-id="62482-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="62482-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="62482-193">0x2A</span></span>                                     | <span data-ttu-id="62482-194">Perfil L4 de AAC</span><span class="sxs-lookup"><span data-stu-id="62482-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="62482-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="62482-195">0x2B</span></span>                                     | <span data-ttu-id="62482-196">L5 del perfil AAC</span><span class="sxs-lookup"><span data-stu-id="62482-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="62482-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="62482-197">0x2C</span></span>                                     | <span data-ttu-id="62482-198">Perfil de alta eficacia v1 AAC L2</span><span class="sxs-lookup"><span data-stu-id="62482-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="62482-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="62482-199">0x2E</span></span>                                     | <span data-ttu-id="62482-200">Perfil de alta eficacia v1 AAC L4</span><span class="sxs-lookup"><span data-stu-id="62482-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="62482-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="62482-201">0x2F</span></span>                                     | <span data-ttu-id="62482-202">Perfil L5 de alta eficacia v1 AAC</span><span class="sxs-lookup"><span data-stu-id="62482-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="62482-203">0x30</span><span class="sxs-lookup"><span data-stu-id="62482-203">0x30</span></span>                                     | <span data-ttu-id="62482-204">Perfil del AAC de alta eficacia V2 L2</span><span class="sxs-lookup"><span data-stu-id="62482-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="62482-205">0x31</span><span class="sxs-lookup"><span data-stu-id="62482-205">0x31</span></span>                                     | <span data-ttu-id="62482-206">Perfil de AAC de alta eficacia V2 L3</span><span class="sxs-lookup"><span data-stu-id="62482-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="62482-207">0x32</span><span class="sxs-lookup"><span data-stu-id="62482-207">0x32</span></span>                                     | <span data-ttu-id="62482-208">Perfil de AAC de alta eficacia V2 L4</span><span class="sxs-lookup"><span data-stu-id="62482-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="62482-209">0x33</span><span class="sxs-lookup"><span data-stu-id="62482-209">0x33</span></span>                                     | <span data-ttu-id="62482-210">Perfil L5 de alta eficacia V2 AAC</span><span class="sxs-lookup"><span data-stu-id="62482-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="62482-211">Una vez establecido el tipo de salida, el codificador AAC actualiza el tipo agregando el atributo de [**\_ datos de \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="62482-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="62482-212">Este atributo contiene la parte de la estructura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece después de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (es decir, después del miembro de **WFX** ).</span><span class="sxs-lookup"><span data-stu-id="62482-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="62482-213">A continuación se muestran los datos de AudioSpecificConfig (), tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="62482-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="62482-214">Cada ejemplo de salida contiene un marco AAC comprimido sin encabezado.</span><span class="sxs-lookup"><span data-stu-id="62482-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="62482-215">Este formato es equivalente al elemento de \_ bloque de datos sin formato \_ () definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="62482-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="62482-216">El atributo de [ \_ tipo de carga de módulo MF MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , si está presente en el tipo de salida, debe establecerse en cero para indicar este tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="62482-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="62482-217">Cada ejemplo de salida contiene un fotograma AAC comprimido correspondiente a los ejemplos 1024 PCM.</span><span class="sxs-lookup"><span data-stu-id="62482-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="62482-218">Por ejemplo, con una frecuencia de muestreo de 48 kHz, la duración de un fotograma comprimido es de 21,33 ms.</span><span class="sxs-lookup"><span data-stu-id="62482-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="62482-219">Si [el \_ \_ tipo de \_ carga \_ de módulo MF MT AAC](mf-mt-aac-payload-type.md) es cero (el valor predeterminado), cada ejemplo de salida contiene un \_ \_ elemento de bloque de datos sin procesar () tal y como se define en ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="62482-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="62482-220">Tipos de medios de ejemplo</span><span class="sxs-lookup"><span data-stu-id="62482-220">Example Media Types</span></span>

<span data-ttu-id="62482-221">Este es un ejemplo de los tipos de medios necesarios para codificar desde 44,1-kHz, audio estéreo de 160-Kbps a AAC sin formato</span><span class="sxs-lookup"><span data-stu-id="62482-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="62482-222">Tipo de medio de entrada:</span><span class="sxs-lookup"><span data-stu-id="62482-222">Input media type:</span></span>



| <span data-ttu-id="62482-223">Atributo</span><span class="sxs-lookup"><span data-stu-id="62482-223">Attribute</span></span>                                                                                    | <span data-ttu-id="62482-224">Value</span><span class="sxs-lookup"><span data-stu-id="62482-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="62482-225">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="62482-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="62482-226">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="62482-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="62482-227">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="62482-228">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="62482-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="62482-229">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="62482-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="62482-230">16</span><span class="sxs-lookup"><span data-stu-id="62482-230">16</span></span>                     |
| [<span data-ttu-id="62482-231">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="62482-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="62482-232">44100</span><span class="sxs-lookup"><span data-stu-id="62482-232">44100</span></span>                  |
| [<span data-ttu-id="62482-233">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="62482-234">2</span><span class="sxs-lookup"><span data-stu-id="62482-234">2</span></span>                      |
| [<span data-ttu-id="62482-235">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="62482-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="62482-236">176400 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="62482-237">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="62482-238">4 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-238">4 (optional)</span></span>           |
| [<span data-ttu-id="62482-239">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="62482-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="62482-240">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-240">1 (optional)</span></span>           |
| [<span data-ttu-id="62482-241">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="62482-242">1411200 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="62482-243">**\_ejemplos de \_ \_ tamaño fijo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="62482-244">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-244">1 (optional)</span></span>           |



 

<span data-ttu-id="62482-245">Tipo de medio de salida:</span><span class="sxs-lookup"><span data-stu-id="62482-245">Output media type:</span></span>



| <span data-ttu-id="62482-246">Atributo</span><span class="sxs-lookup"><span data-stu-id="62482-246">Attribute</span></span>                                                                                      | <span data-ttu-id="62482-247">Value</span><span class="sxs-lookup"><span data-stu-id="62482-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62482-248">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="62482-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="62482-249">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="62482-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="62482-250">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="62482-251">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="62482-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="62482-252">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="62482-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="62482-253">16</span><span class="sxs-lookup"><span data-stu-id="62482-253">16</span></span>                                                                                              |
| [<span data-ttu-id="62482-254">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="62482-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="62482-255">44100</span><span class="sxs-lookup"><span data-stu-id="62482-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="62482-256">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="62482-257">2</span><span class="sxs-lookup"><span data-stu-id="62482-257">2</span></span>                                                                                               |
| [<span data-ttu-id="62482-258">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="62482-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="62482-259">20000</span><span class="sxs-lookup"><span data-stu-id="62482-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="62482-260">\_tipo de \_ carga del AAC \_ \_ de MF MT</span><span class="sxs-lookup"><span data-stu-id="62482-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="62482-261">0 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="62482-262">\_indicación de \_ \_ nivel de \_ Perfil de audio \_ \_ MF MT AAC</span><span class="sxs-lookup"><span data-stu-id="62482-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="62482-263">0x29 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="62482-264">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="62482-265">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="62482-266">**MF \_ MT \_ All \_ Samples \_ independiente**</span><span class="sxs-lookup"><span data-stu-id="62482-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="62482-267">0 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="62482-268">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="62482-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="62482-269">160000 (opcional)</span><span class="sxs-lookup"><span data-stu-id="62482-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="62482-270">**datos de usuario de MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62482-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="62482-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0X12, 0x10} opta</span><span class="sxs-lookup"><span data-stu-id="62482-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="62482-272">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62482-272">Remarks</span></span>

<span data-ttu-id="62482-273">En la implementación actual, cada muestra de entrada debe tener una hora y una duración válidas.</span><span class="sxs-lookup"><span data-stu-id="62482-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="62482-274">Para establecer la hora de ejemplo, llame a [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="62482-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="62482-275">Para establecer la duración del ejemplo, llame a [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="62482-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="62482-276">Si no se establece la hora de ejemplo, el método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) del codificador devuelve **MF \_ E \_ no \_ muestra ninguna \_ marca** de tiempo.</span><span class="sxs-lookup"><span data-stu-id="62482-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="62482-277">Si no se establece la duración del ejemplo, el método **ProcessInput** devuelve **MF \_ E \_ no \_ muestra la \_ duración**.</span><span class="sxs-lookup"><span data-stu-id="62482-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="62482-278">La duración de la muestra se puede calcular de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="62482-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="62482-279">donde *nAudioSamplesPerChannel* es el número de muestras de audio PCM por canal en el búfer de entrada, y *nSamplesPerSec* es la frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="62482-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="62482-280">Debido a un error en la implementación actual, si la duración de ejemplo está establecida en cero, la llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) se realiza correctamente, pero una llamada subsiguiente a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) producirá una excepción de división por cero.</span><span class="sxs-lookup"><span data-stu-id="62482-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="62482-281">Para evitar este error, establezca una duración válida distinto de cero en cada ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="62482-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62482-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62482-282">Requirements</span></span>



| <span data-ttu-id="62482-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="62482-283">Requirement</span></span> | <span data-ttu-id="62482-284">Value</span><span class="sxs-lookup"><span data-stu-id="62482-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62482-285">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62482-285">Minimum supported client</span></span><br/> | <span data-ttu-id="62482-286">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="62482-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="62482-287">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62482-287">Minimum supported server</span></span><br/> | <span data-ttu-id="62482-288">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="62482-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="62482-289">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62482-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62482-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62482-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62482-291">Vea también</span><span class="sxs-lookup"><span data-stu-id="62482-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62482-292">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="62482-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="62482-293">**Descodificador AAC**</span><span class="sxs-lookup"><span data-stu-id="62482-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="62482-294">Tipos de medios AAC</span><span class="sxs-lookup"><span data-stu-id="62482-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="62482-295">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="62482-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="62482-296">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62482-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="62482-297">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62482-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

