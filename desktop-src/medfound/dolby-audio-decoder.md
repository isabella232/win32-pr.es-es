---
description: El descodificador de audio Dolby es un MFT que descodifica Dolby Digital (AC-3) y Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Descodificador de audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808096"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="5fee9-103">Descodificador de audio Dolby</span><span class="sxs-lookup"><span data-stu-id="5fee9-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="5fee9-104">El descodificador de audio Dolby es una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) que descodifica los tipos de secuencia siguientes:</span><span class="sxs-lookup"><span data-stu-id="5fee9-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="5fee9-105">Dolby digital, también denominado Dolby AC-3</span><span class="sxs-lookup"><span data-stu-id="5fee9-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="5fee9-106">Dolby Digital Plus, también denominado AC-3 mejorado (E-AC-3)</span><span class="sxs-lookup"><span data-stu-id="5fee9-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fee9-107">En el caso de las versiones de Windows anteriores a Windows 8, la implementación de Microsoft de la tecnología Dolby Digital está restringida en lo que respecta al programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5fee9-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="5fee9-108">Para obtener más información acerca de estos formatos, consulte el documento sobre el Comité de sistemas de televisión avanzado (ATSC) ( *AC-3, E-AC-3) revisión B*.</span><span class="sxs-lookup"><span data-stu-id="5fee9-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="5fee9-109">El descodificador también puede convertir una secuencia Dolby Digital Plus en el formato Dolby digital para la salida AC-3 S/PIDF o dar formato a un flujo Dolby Digital Plus para la salida digital HDMI.</span><span class="sxs-lookup"><span data-stu-id="5fee9-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="5fee9-110">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="5fee9-110">Class Identifier</span></span>

<span data-ttu-id="5fee9-111">El identificador de clase (CLSID) del descodificador de audio Dolby es **CLSID \_ CMSDDPlusDecMFT**, definido en el archivo de encabezado wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="5fee9-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="5fee9-112">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="5fee9-112">Input Types</span></span>

<span data-ttu-id="5fee9-113">El descodificador de Dolby audio admite los siguientes subtipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fee9-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="5fee9-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="5fee9-114">Subtype</span></span>                                 | <span data-ttu-id="5fee9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fee9-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="5fee9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fee9-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="5fee9-117">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="5fee9-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="5fee9-118">Audio Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="5fee9-119">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-119">mfapi.h</span></span>      |
| <span data-ttu-id="5fee9-120">**MEDIASUBTYPE \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="5fee9-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="5fee9-121">Audio Dolby digital; vea [**subtipos de audio**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="5fee9-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="5fee9-122">Este subtipo se puede usar indistintamente con **MEDIASUBTYPE \_ Dolby \_ AC3**.</span><span class="sxs-lookup"><span data-stu-id="5fee9-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="5fee9-123">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="5fee9-124">**MFAudioFormat \_ Dolby \_ digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="5fee9-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="5fee9-125">Audio Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="5fee9-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="5fee9-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-126">mfapi.h</span></span>      |



 

<span data-ttu-id="5fee9-127">En la tabla siguiente se enumeran los atributos requires y opcionales para el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fee9-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fee9-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="5fee9-128">Attribute</span></span></th>
<th><span data-ttu-id="5fee9-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fee9-129">Description</span></span></th>
<th><span data-ttu-id="5fee9-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fee9-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fee9-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="5fee9-132">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="5fee9-132">Major type.</span></span></td>
<td><span data-ttu-id="5fee9-133">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-133">Required.</span></span> <span data-ttu-id="5fee9-134">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fee9-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="5fee9-136">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="5fee9-137">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-137">Required.</span></span> <span data-ttu-id="5fee9-138">Vea la tabla anterior para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5fee9-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5fee9-140">Frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="5fee9-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fee9-141">Optional.</span></span> <span data-ttu-id="5fee9-142">Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000.</span><span class="sxs-lookup"><span data-stu-id="5fee9-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="5fee9-143">Si no se establece este atributo, el valor predeterminado es 48000.</span><span class="sxs-lookup"><span data-stu-id="5fee9-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5fee9-144">Los flujos Dolby AC-3 se limitan a las tres tasas más altas de esta lista.</span><span class="sxs-lookup"><span data-stu-id="5fee9-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="5fee9-146">Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="5fee9-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="5fee9-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fee9-147">Optional.</span></span> <span data-ttu-id="5fee9-148">Los valores válidos están en el intervalo de 1 (mono) a 8 (configuración de canal 7,1).</span><span class="sxs-lookup"><span data-stu-id="5fee9-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="5fee9-149">Si no se establece este atributo, el valor predeterminado es 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="5fee9-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="5fee9-151">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="5fee9-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="5fee9-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5fee9-152">Optional.</span></span> <span data-ttu-id="5fee9-153">Si se especifica, el valor debe ser coherente con el número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="5fee9-154">Si no se establece el atributo, el descodificador utiliza una máscara de canal predeterminada, en función del número de canales.</span><span class="sxs-lookup"><span data-stu-id="5fee9-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5fee9-155">En la tabla siguiente se enumeran las configuraciones de canal Dolby admitidas.</span><span class="sxs-lookup"><span data-stu-id="5fee9-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fee9-156">Configuración del canal</span><span class="sxs-lookup"><span data-stu-id="5fee9-156">Channel configuration</span></span></th>
<th><span data-ttu-id="5fee9-157">Número de canales</span><span class="sxs-lookup"><span data-stu-id="5fee9-157">Number of channels</span></span></th>
<th><span data-ttu-id="5fee9-158">Máscaras de canal</span><span class="sxs-lookup"><span data-stu-id="5fee9-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fee9-159">1/0 (mono)</span><span class="sxs-lookup"><span data-stu-id="5fee9-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="5fee9-160">1</span><span class="sxs-lookup"><span data-stu-id="5fee9-160">1</span></span></td>
<td><span data-ttu-id="5fee9-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-162">2/0 (estéreo) o 1 + 1 (mono dual)</span><span class="sxs-lookup"><span data-stu-id="5fee9-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="5fee9-163">2</span><span class="sxs-lookup"><span data-stu-id="5fee9-163">2</span></span></td>
<td><span data-ttu-id="5fee9-164">0X3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-165">3/0</span><span class="sxs-lookup"><span data-stu-id="5fee9-165">3/0</span></span></td>
<td><span data-ttu-id="5fee9-166">3</span><span class="sxs-lookup"><span data-stu-id="5fee9-166">3</span></span></td>
<td><span data-ttu-id="5fee9-167">0X7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="5fee9-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-168">2/1</span><span class="sxs-lookup"><span data-stu-id="5fee9-168">2/1</span></span></td>
<td><span data-ttu-id="5fee9-169">3</span><span class="sxs-lookup"><span data-stu-id="5fee9-169">3</span></span></td>
<td><span data-ttu-id="5fee9-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-171">3/1</span><span class="sxs-lookup"><span data-stu-id="5fee9-171">3/1</span></span></td>
<td><span data-ttu-id="5fee9-172">4</span><span class="sxs-lookup"><span data-stu-id="5fee9-172">4</span></span></td>
<td><span data-ttu-id="5fee9-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-174">2/2</span><span class="sxs-lookup"><span data-stu-id="5fee9-174">2/2</span></span></td>
<td><span data-ttu-id="5fee9-175">4</span><span class="sxs-lookup"><span data-stu-id="5fee9-175">4</span></span></td>
<td><span data-ttu-id="5fee9-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5fee9-177">or</span><span class="sxs-lookup"><span data-stu-id="5fee9-177">or</span></span><br/> <span data-ttu-id="5fee9-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-179">3/2</span><span class="sxs-lookup"><span data-stu-id="5fee9-179">3/2</span></span></td>
<td><span data-ttu-id="5fee9-180">5</span><span class="sxs-lookup"><span data-stu-id="5fee9-180">5</span></span></td>
<td><span data-ttu-id="5fee9-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5fee9-182">or</span><span class="sxs-lookup"><span data-stu-id="5fee9-182">or</span></span><br/> <span data-ttu-id="5fee9-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="5fee9-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="5fee9-185">6</span><span class="sxs-lookup"><span data-stu-id="5fee9-185">6</span></span></td>
<td><span data-ttu-id="5fee9-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="5fee9-187">or</span><span class="sxs-lookup"><span data-stu-id="5fee9-187">or</span></span><br/> <span data-ttu-id="5fee9-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="5fee9-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="5fee9-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5fee9-190">Solo Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="5fee9-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="5fee9-191">8</span><span class="sxs-lookup"><span data-stu-id="5fee9-191">8</span></span></td>
<td><span data-ttu-id="5fee9-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="5fee9-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5fee9-193">Además, las configuraciones de canal 1/0, 2/0, 3/0, 2/1, 3/1 y 2/2 también pueden aparecer con un canal LFE.</span><span class="sxs-lookup"><span data-stu-id="5fee9-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="5fee9-194">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="5fee9-194">Output Types</span></span>

<span data-ttu-id="5fee9-195">El descodificador de audio Dolby admite los siguientes subtipos de salida.</span><span class="sxs-lookup"><span data-stu-id="5fee9-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="5fee9-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="5fee9-196">Subtype</span></span>                                                   | <span data-ttu-id="5fee9-197">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fee9-197">Description</span></span>                                                                                                                               | <span data-ttu-id="5fee9-198">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fee9-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5fee9-199">**MFAudioFormat \_ Dolby \_ AC3 ( \_ SPDIF)**</span><span class="sxs-lookup"><span data-stu-id="5fee9-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="5fee9-200">Audio Dolby AC-3 con formato de salida digital S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="5fee9-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="5fee9-201">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-201">mfapi.h</span></span>   |
| <span data-ttu-id="5fee9-202">**KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="5fee9-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="5fee9-203">Audio Dolby Digital Plus con formato de salida digital HDMI.</span><span class="sxs-lookup"><span data-stu-id="5fee9-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="5fee9-204">ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-204">ksmedia.h</span></span> |
| <span data-ttu-id="5fee9-205">**MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="5fee9-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="5fee9-206">Audio PCM de punto flotante IEEE 32-bit</span><span class="sxs-lookup"><span data-stu-id="5fee9-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="5fee9-207">**Windows 10**: estéreo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="5fee9-208">**Versiones anteriores**: estéreo, 5,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="5fee9-209">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-209">mfapi.h</span></span>   |
| <span data-ttu-id="5fee9-210">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="5fee9-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="5fee9-211">audio PCM de 16 bits</span><span class="sxs-lookup"><span data-stu-id="5fee9-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="5fee9-212">**Windows 10**: estéreo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="5fee9-213">**Versiones anteriores**: estéreo, 5,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="5fee9-214">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="5fee9-214">mfapi.h</span></span>   |



 

<span data-ttu-id="5fee9-215">En la tabla siguiente se enumeran los atributos obligatorios y opcionales para el tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="5fee9-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fee9-216">Atributo</span><span class="sxs-lookup"><span data-stu-id="5fee9-216">Attribute</span></span></th>
<th><span data-ttu-id="5fee9-217">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fee9-217">Description</span></span></th>
<th><span data-ttu-id="5fee9-218">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fee9-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fee9-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="5fee9-220">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="5fee9-220">Major type.</span></span></td>
<td><span data-ttu-id="5fee9-221">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-221">Required.</span></span> <span data-ttu-id="5fee9-222">Debe ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fee9-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="5fee9-224">Subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="5fee9-225">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-225">Required.</span></span> <span data-ttu-id="5fee9-226">Vea la tabla anterior para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5fee9-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5fee9-228">Frecuencia de muestreo, en muestras por segundo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="5fee9-229">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-229">Required.</span></span> <span data-ttu-id="5fee9-230">Los valores válidos son: 48000, 44100, 32000, 24000, 22050 y 16000.</span><span class="sxs-lookup"><span data-stu-id="5fee9-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="5fee9-231">La velocidad de muestra de salida debe ser idéntica a la velocidad de muestra de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fee9-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="5fee9-232">El descodificador no puede cambiar la velocidad de muestreo de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5fee9-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="5fee9-234">Número de canales, incluido el canal de baja frecuencia (LFE), si está presente.</span><span class="sxs-lookup"><span data-stu-id="5fee9-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="5fee9-235">Se requiere para la salida del PCM.</span><span class="sxs-lookup"><span data-stu-id="5fee9-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="5fee9-236">No es necesario para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="5fee9-237">Si el tipo de entrada es mono, estéreo o dual mono (todo sin canal LFE), el único valor válido es 2, para la salida estéreo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="5fee9-238">De lo contrario, el valor puede ser:</span><span class="sxs-lookup"><span data-stu-id="5fee9-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="5fee9-239">2 para downmix estéreo</span><span class="sxs-lookup"><span data-stu-id="5fee9-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="5fee9-240">6 para configuraciones de canal 5,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="5fee9-241">8 para configuraciones de canal 7,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="5fee9-243">Especifica la asignación de canales de audio a las posiciones del hablante.</span><span class="sxs-lookup"><span data-stu-id="5fee9-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="5fee9-244">Se requiere para la salida del PCM si el número de canales es mayor que 2.</span><span class="sxs-lookup"><span data-stu-id="5fee9-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="5fee9-245">El valor debe ser:</span><span class="sxs-lookup"><span data-stu-id="5fee9-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="5fee9-246">0X3 para la salida estéreo</span><span class="sxs-lookup"><span data-stu-id="5fee9-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="5fee9-247">0x3F para la salida del canal 5,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="5fee9-248">0x63F para la salida del canal 7,1</span><span class="sxs-lookup"><span data-stu-id="5fee9-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="5fee9-249">No es necesario para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="5fee9-251">Número de bits por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="5fee9-252">Se requiere para la salida del PCM.</span><span class="sxs-lookup"><span data-stu-id="5fee9-252">Required for PCM output.</span></span> <span data-ttu-id="5fee9-253">El valor debe ser 32 para <strong>MFAudioFormat_Float</strong>y 16 para <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fee9-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="5fee9-254">No es necesario para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="5fee9-256">Número de bits válidos de datos de audio en cada ejemplo de audio.</span><span class="sxs-lookup"><span data-stu-id="5fee9-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="5fee9-257">Opcional para la salida de PCM.</span><span class="sxs-lookup"><span data-stu-id="5fee9-257">Optional for PCM output.</span></span> <span data-ttu-id="5fee9-258">Si se establece, el valor debe ser idéntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="5fee9-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="5fee9-259">No es necesario para los subtipos de salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fee9-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="5fee9-261">Alineación de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="5fee9-262">Opcional para la salida de PCM.</span><span class="sxs-lookup"><span data-stu-id="5fee9-262">Optional for PCM output.</span></span> <span data-ttu-id="5fee9-263">No es necesario para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fee9-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="5fee9-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="5fee9-265">Número promedio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="5fee9-266">Opcional para la salida de PCM.</span><span class="sxs-lookup"><span data-stu-id="5fee9-266">Optional for PCM output.</span></span> <span data-ttu-id="5fee9-267">No es necesario para la salida digital.</span><span class="sxs-lookup"><span data-stu-id="5fee9-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="5fee9-268">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="5fee9-268">Transform Attributes</span></span>

<span data-ttu-id="5fee9-269">El descodificador de audio Dolby implementa el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="5fee9-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="5fee9-270">La aplicación puede utilizar este método para obtener o establecer los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="5fee9-271">Atributo</span><span class="sxs-lookup"><span data-stu-id="5fee9-271">Attribute</span></span>                                                                                | <span data-ttu-id="5fee9-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fee9-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fee9-273">CODECAPI \_ AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="5fee9-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="5fee9-274">Especifica si una secuencia de audio Dolby de 2 canales se codifica como estéreo o dual mono.</span><span class="sxs-lookup"><span data-stu-id="5fee9-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="5fee9-275">Antes de descodificar el primer fotograma Dolby, el valor es **EAVDecAudioDualMono \_ sin especificar**.</span><span class="sxs-lookup"><span data-stu-id="5fee9-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="5fee9-276">Una vez iniciada la descodificación, el valor refleja el fotograma Dolby más reciente.</span><span class="sxs-lookup"><span data-stu-id="5fee9-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="5fee9-277">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5fee9-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="5fee9-278">CODECAPI \_ AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="5fee9-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="5fee9-279">Especifica cómo el descodificador Reproduce audio dual mono.</span><span class="sxs-lookup"><span data-stu-id="5fee9-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="5fee9-280">El valor predeterminado es **eAVDecAudioDualMonoReproMode \_ \_** a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="5fee9-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="5fee9-281">La aplicación puede establecer esta propiedad en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="5fee9-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="5fee9-282">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="5fee9-283">CODECAPI \_ AVDecCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="5fee9-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="5fee9-284">En el caso de las secuencias Dolby Digital (AC-3), especifica la velocidad de bits del flujo de entrada en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="5fee9-285">Para Dolby Digital Plus (E-AC3), el valor siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="5fee9-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="5fee9-286">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5fee9-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="5fee9-287">CODECAPI \_ AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="5fee9-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="5fee9-288">El corte de alto nivel cuando el descodificador realiza el control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5fee9-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="5fee9-289">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="5fee9-290">CODECAPI \_ AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="5fee9-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="5fee9-291">El aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5fee9-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="5fee9-292">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="5fee9-293">CODECAPI \_ AVDecDDOperationalMode</span><span class="sxs-lookup"><span data-stu-id="5fee9-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="5fee9-294">Modo de control de compresión.</span><span class="sxs-lookup"><span data-stu-id="5fee9-294">The compression control mode.</span></span><br/> <span data-ttu-id="5fee9-295">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="5fee9-296">CODECAPI \_ AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="5fee9-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="5fee9-297">Tipo de downmix estéreo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-297">The type of stereo downmix.</span></span> <span data-ttu-id="5fee9-298">Esta propiedad se aplica cuando la entrada es una secuencia multicanal y el resultado es una secuencia estéreo.</span><span class="sxs-lookup"><span data-stu-id="5fee9-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="5fee9-299">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="5fee9-300">la MFT \_ admite el \_ \_ cambio de formato dinámico \_</span><span class="sxs-lookup"><span data-stu-id="5fee9-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="5fee9-301">Este atributo devuelve **false**, lo que indica que el descodificador se debe purgar antes de que se establezca un nuevo tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="5fee9-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="5fee9-302">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fee9-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5fee9-303">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5fee9-303">Remarks</span></span>

<span data-ttu-id="5fee9-304">El descodificador solo acepta secuencias Dolby sin formato, tal y como se define en/52B.</span><span class="sxs-lookup"><span data-stu-id="5fee9-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="5fee9-305">No se admiten cargas como las secuencias elementales (PES) en paquetes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="5fee9-306">En el caso de Dolby Digital Plus, el descodificador descodifica hasta 5,1 canales.</span><span class="sxs-lookup"><span data-stu-id="5fee9-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="5fee9-307">En Windows 10, los flujos de canal 7,1 se descodifican sin downmix.</span><span class="sxs-lookup"><span data-stu-id="5fee9-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="5fee9-308">En versiones anteriores del sistema operativo, si el flujo es de 7,1 canales, solo se descodificará el canal de 5,1 downmix.</span><span class="sxs-lookup"><span data-stu-id="5fee9-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="5fee9-309">Si la secuencia es Dolby Digital Plus con más de un subflujo independiente, solo se descodifica el subflujo 0 independiente.</span><span class="sxs-lookup"><span data-stu-id="5fee9-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="5fee9-310">El descodificador omite otros subflujos independientes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="5fee9-311">Además, el descodificador omite todas las subsecuencias dependientes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="5fee9-312">El descodificador admite el descifrado y la descodificación de secuencias que están protegidas por la tecnología de Rights Management digital (DRM).</span><span class="sxs-lookup"><span data-stu-id="5fee9-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="5fee9-313">Si el tipo de medio de entrada tiene una configuración de canal que no es mono, estéreo o dual mono (todo sin canal LFE), el descodificador proporciona dos opciones para las configuraciones de canal de salida:</span><span class="sxs-lookup"><span data-stu-id="5fee9-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="5fee9-314">salida de 8 canales (configuración de canal 7,1)</span><span class="sxs-lookup"><span data-stu-id="5fee9-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="5fee9-315">salida de 6 canales (configuración de canal 5,1)</span><span class="sxs-lookup"><span data-stu-id="5fee9-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="5fee9-316">Downmix estéreo</span><span class="sxs-lookup"><span data-stu-id="5fee9-316">Stereo downmix</span></span>

<span data-ttu-id="5fee9-317">Si se selecciona Stereo downmix, el tipo de downmix se puede establecer en la MFT mediante la propiedad [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="5fee9-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="5fee9-318">Si el tipo de salida es **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, cada búfer de salida contiene 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="5fee9-319">El búfer se inicia con un encabezado S/PDIF de 8 bytes, seguido de un fotograma AC-3 comprimido, seguido de un relleno de cero a 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="5fee9-320">Si el tipo de salida es **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ digital \_ Plus**, cada búfer de salida contiene 24.576 bytes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="5fee9-321">El búfer se inicia con un encabezado S/PDIF de 8 bytes, seguido de 1 – 6 fotogramas Dolby Digital Plus comprimidos correspondientes a los ejemplos de 1.536 PCM, seguidos de un relleno de ceros a 24.576 bytes.</span><span class="sxs-lookup"><span data-stu-id="5fee9-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="5fee9-322">Para la salida HDMI, solo se empaqueta el subflujo 0 independiente.</span><span class="sxs-lookup"><span data-stu-id="5fee9-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="5fee9-323">La MFT del descodificador se registra con la marca de **enumeración de MFT de marca \_ \_ \_ FIELDOFUSE**, que indica que el MFT debe desbloquearse por la aplicación antes de usarse.</span><span class="sxs-lookup"><span data-stu-id="5fee9-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="5fee9-324">Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5fee9-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fee9-325">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fee9-325">Requirements</span></span>



| <span data-ttu-id="5fee9-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fee9-326">Requirement</span></span> | <span data-ttu-id="5fee9-327">Value</span><span class="sxs-lookup"><span data-stu-id="5fee9-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fee9-328">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fee9-328">Minimum supported client</span></span><br/> | <span data-ttu-id="5fee9-329">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="5fee9-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="5fee9-330">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5fee9-330">Minimum supported server</span></span><br/> | <span data-ttu-id="5fee9-331">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5fee9-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="5fee9-332">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5fee9-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fee9-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fee9-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fee9-334">Vea también</span><span class="sxs-lookup"><span data-stu-id="5fee9-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fee9-335">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="5fee9-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
