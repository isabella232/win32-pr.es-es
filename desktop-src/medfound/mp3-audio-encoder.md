---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificador de audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082297"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="7aa54-103">Codificador de audio MP3</span><span class="sxs-lookup"><span data-stu-id="7aa54-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="7aa54-104">El codificador de audio MP3 Microsoft Media Foundation es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que codifica audio MPEG-1 capa 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="7aa54-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="7aa54-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="7aa54-105">Class Identifier</span></span>

<span data-ttu-id="7aa54-106">El identificador de clase (CLSID) del codificador MP3 es **CLSID \_ MP3ACMCodecWrapper**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="7aa54-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="7aa54-107">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="7aa54-107">Media Types</span></span>

<span data-ttu-id="7aa54-108">El codificador MP3 admite los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="7aa54-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="7aa54-109">El tipo de salida debe establecerse antes que el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7aa54-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="7aa54-110">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="7aa54-110">Output Types</span></span>

<span data-ttu-id="7aa54-111">Establezca los siguientes atributos en el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="7aa54-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aa54-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="7aa54-112">Attribute</span></span></th>
<th><span data-ttu-id="7aa54-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aa54-113">Description</span></span></th>
<th><span data-ttu-id="7aa54-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7aa54-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7aa54-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aa54-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="7aa54-116">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="7aa54-116">Major type.</span></span></td>
<td><span data-ttu-id="7aa54-117">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="7aa54-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa54-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aa54-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="7aa54-119">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="7aa54-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="7aa54-120">Debe ser <strong>MFAudioFormat_MP3</strong>.</span><span class="sxs-lookup"><span data-stu-id="7aa54-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa54-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aa54-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="7aa54-122">Velocidad de bits de la secuencia MP3 codificada, en bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="7aa54-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="7aa54-123">El codificador es compatible con todas las velocidades de bits definidas por el estándar (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 o 320 Kbps).</span><span class="sxs-lookup"><span data-stu-id="7aa54-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="7aa54-124">La velocidad de bits predeterminada es 128 kbps para mono y 320 Kbps para estéreo.</span><span class="sxs-lookup"><span data-stu-id="7aa54-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="7aa54-125">Utilice este atributo para especificar la velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="7aa54-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa54-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aa54-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="7aa54-127">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="7aa54-127">Number of channels.</span></span></td>
<td><span data-ttu-id="7aa54-128">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="7aa54-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="7aa54-129">1 (mono)</span><span class="sxs-lookup"><span data-stu-id="7aa54-129">1 (mono)</span></span></li>
<li><span data-ttu-id="7aa54-130">2 (estéreo)</span><span class="sxs-lookup"><span data-stu-id="7aa54-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aa54-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aa54-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="7aa54-132">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="7aa54-132">Samples per second.</span></span></td>
<td><span data-ttu-id="7aa54-133">Se admiten los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="7aa54-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="7aa54-134">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="7aa54-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="7aa54-135">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="7aa54-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="7aa54-136">32000 (32 KHz)</span><span class="sxs-lookup"><span data-stu-id="7aa54-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aa54-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="7aa54-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="7aa54-138">Datos de códecs adicionales.</span><span class="sxs-lookup"><span data-stu-id="7aa54-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="7aa54-139">Este atributo contiene los 12 bytes de la estructura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> que siguen el miembro de <strong>WFX</strong> de esa estructura.</span><span class="sxs-lookup"><span data-stu-id="7aa54-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7aa54-140">Como alternativa, puede rellenar una estructura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) y llamar a [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) para convertir la estructura en un tipo de medio Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7aa54-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="7aa54-141">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="7aa54-141">Input Types</span></span>

<span data-ttu-id="7aa54-142">Establezca los siguientes atributos en el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="7aa54-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="7aa54-143">Atributo</span><span class="sxs-lookup"><span data-stu-id="7aa54-143">Attribute</span></span>                                                                               | <span data-ttu-id="7aa54-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="7aa54-144">Description</span></span>         | <span data-ttu-id="7aa54-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7aa54-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="7aa54-146">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7aa54-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="7aa54-147">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="7aa54-147">Major type.</span></span>         | <span data-ttu-id="7aa54-148">Debe ser **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="7aa54-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="7aa54-149">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7aa54-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="7aa54-150">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="7aa54-150">Subtype.</span></span>            | <span data-ttu-id="7aa54-151">Debe ser **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="7aa54-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="7aa54-152">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="7aa54-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="7aa54-153">Bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="7aa54-153">Bits per sample.</span></span>    | <span data-ttu-id="7aa54-154">Debe ser 16.</span><span class="sxs-lookup"><span data-stu-id="7aa54-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="7aa54-155">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="7aa54-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="7aa54-156">Muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="7aa54-156">Samples per second.</span></span> | <span data-ttu-id="7aa54-157">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="7aa54-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="7aa54-158">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7aa54-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="7aa54-159">Número de canales.</span><span class="sxs-lookup"><span data-stu-id="7aa54-159">Number of channels.</span></span> | <span data-ttu-id="7aa54-160">Debe coincidir con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="7aa54-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="7aa54-161">El codificador solo admite datos de entrada de PCM enteros de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7aa54-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="7aa54-162">No admite la entrada de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7aa54-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="7aa54-163">Formatos de medios</span><span class="sxs-lookup"><span data-stu-id="7aa54-163">Media Formats</span></span>

<span data-ttu-id="7aa54-164">El estándar MPEG-1 y MPEG-2 define los formatos de audio de nivel 3 de 252.</span><span class="sxs-lookup"><span data-stu-id="7aa54-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="7aa54-165">El codificador MP3 admite el estándar con algunas excepciones, así como algunos formatos adicionales, como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="7aa54-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="7aa54-166">La capa 3 se define como:</span><span class="sxs-lookup"><span data-stu-id="7aa54-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="7aa54-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa54-167">Requirement</span></span> | <span data-ttu-id="7aa54-168">Value</span><span class="sxs-lookup"><span data-stu-id="7aa54-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7aa54-169">Canales</span><span class="sxs-lookup"><span data-stu-id="7aa54-169">Channels</span></span>                         | <span data-ttu-id="7aa54-170">mono o estéreo</span><span class="sxs-lookup"><span data-stu-id="7aa54-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="7aa54-171">Velocidades de muestra MPEG-1 en kHz</span><span class="sxs-lookup"><span data-stu-id="7aa54-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="7aa54-172">44,1, 48, 32</span><span class="sxs-lookup"><span data-stu-id="7aa54-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="7aa54-173">Velocidades de bits con codificación MPEG-1 en kbps</span><span class="sxs-lookup"><span data-stu-id="7aa54-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="7aa54-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span><span class="sxs-lookup"><span data-stu-id="7aa54-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="7aa54-175">Velocidades de muestra de MPEG-2 en kHz</span><span class="sxs-lookup"><span data-stu-id="7aa54-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="7aa54-176">8, 11,025, 12, 16, 22,05, 24</span><span class="sxs-lookup"><span data-stu-id="7aa54-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="7aa54-177">Velocidades de bits con codificación MPEG-2 en kbps</span><span class="sxs-lookup"><span data-stu-id="7aa54-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="7aa54-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span><span class="sxs-lookup"><span data-stu-id="7aa54-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="7aa54-179">El codificador MP3 también admite los siguientes formatos.</span><span class="sxs-lookup"><span data-stu-id="7aa54-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="7aa54-180">Velocidad de muestreo</span><span class="sxs-lookup"><span data-stu-id="7aa54-180">Sample Rate</span></span> | <span data-ttu-id="7aa54-181">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="7aa54-181">Bit Rate</span></span>     | <span data-ttu-id="7aa54-182">Número de canal</span><span class="sxs-lookup"><span data-stu-id="7aa54-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="7aa54-183">8000</span><span class="sxs-lookup"><span data-stu-id="7aa54-183">8000</span></span>        | <span data-ttu-id="7aa54-184">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="7aa54-184">18000, 20000</span></span> | <span data-ttu-id="7aa54-185">2</span><span class="sxs-lookup"><span data-stu-id="7aa54-185">2</span></span>              |
| <span data-ttu-id="7aa54-186">11025</span><span class="sxs-lookup"><span data-stu-id="7aa54-186">11025</span></span>       | <span data-ttu-id="7aa54-187">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="7aa54-187">18000, 20000</span></span> | <span data-ttu-id="7aa54-188">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-188">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-189">12000</span><span class="sxs-lookup"><span data-stu-id="7aa54-189">12000</span></span>       | <span data-ttu-id="7aa54-190">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="7aa54-190">18000, 20000</span></span> | <span data-ttu-id="7aa54-191">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-191">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-192">16000</span><span class="sxs-lookup"><span data-stu-id="7aa54-192">16000</span></span>       | <span data-ttu-id="7aa54-193">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="7aa54-193">18000, 20000</span></span> | <span data-ttu-id="7aa54-194">1</span><span class="sxs-lookup"><span data-stu-id="7aa54-194">1</span></span>              |
| <span data-ttu-id="7aa54-195">32000</span><span class="sxs-lookup"><span data-stu-id="7aa54-195">32000</span></span>       | <span data-ttu-id="7aa54-196">144000</span><span class="sxs-lookup"><span data-stu-id="7aa54-196">144000</span></span>       | <span data-ttu-id="7aa54-197">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-197">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-198">44100</span><span class="sxs-lookup"><span data-stu-id="7aa54-198">44100</span></span>       | <span data-ttu-id="7aa54-199">144000</span><span class="sxs-lookup"><span data-stu-id="7aa54-199">144000</span></span>       | <span data-ttu-id="7aa54-200">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-200">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-201">48000</span><span class="sxs-lookup"><span data-stu-id="7aa54-201">48000</span></span>       | <span data-ttu-id="7aa54-202">144000</span><span class="sxs-lookup"><span data-stu-id="7aa54-202">144000</span></span>       | <span data-ttu-id="7aa54-203">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-203">1 or 2</span></span>         |



 

<span data-ttu-id="7aa54-204">El codificador MP3 no admite los siguientes formatos definidos por el estándar.</span><span class="sxs-lookup"><span data-stu-id="7aa54-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="7aa54-205">Velocidad de muestreo</span><span class="sxs-lookup"><span data-stu-id="7aa54-205">Sample Rate</span></span> | <span data-ttu-id="7aa54-206">Velocidades de bits</span><span class="sxs-lookup"><span data-stu-id="7aa54-206">Bit Rates</span></span>                                    | <span data-ttu-id="7aa54-207">Número de canal</span><span class="sxs-lookup"><span data-stu-id="7aa54-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="7aa54-208">12000</span><span class="sxs-lookup"><span data-stu-id="7aa54-208">12000</span></span>       | <span data-ttu-id="7aa54-209">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="7aa54-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="7aa54-210">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-210">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-211">11025</span><span class="sxs-lookup"><span data-stu-id="7aa54-211">11025</span></span>       | <span data-ttu-id="7aa54-212">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="7aa54-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="7aa54-213">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-213">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-214">8000</span><span class="sxs-lookup"><span data-stu-id="7aa54-214">8000</span></span>        | <span data-ttu-id="7aa54-215">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="7aa54-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="7aa54-216">1 o 2</span><span class="sxs-lookup"><span data-stu-id="7aa54-216">1 or 2</span></span>         |
| <span data-ttu-id="7aa54-217">8000</span><span class="sxs-lookup"><span data-stu-id="7aa54-217">8000</span></span>        | <span data-ttu-id="7aa54-218">8000, 11025, 12000, 16000, 22050, 24000</span><span class="sxs-lookup"><span data-stu-id="7aa54-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="7aa54-219">2</span><span class="sxs-lookup"><span data-stu-id="7aa54-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="7aa54-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aa54-220">Requirements</span></span>



| <span data-ttu-id="7aa54-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa54-221">Requirement</span></span> | <span data-ttu-id="7aa54-222">Value</span><span class="sxs-lookup"><span data-stu-id="7aa54-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7aa54-223">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aa54-223">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa54-224">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7aa54-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="7aa54-225">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7aa54-225">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa54-226">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7aa54-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7aa54-227">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aa54-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa54-228">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="7aa54-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
