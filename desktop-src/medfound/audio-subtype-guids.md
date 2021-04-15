---
description: GUID de subtipo de audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de subtipo de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496852"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="a6b9c-103">GUID de subtipo de audio</span><span class="sxs-lookup"><span data-stu-id="a6b9c-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="a6b9c-104">Se definen los siguientes GUID de subtipo de audio.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="a6b9c-105">Para especificar el subtipo, establezca el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="a6b9c-106">Excepto donde se indique, estas constantes se definen en el archivo de encabezado mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="a6b9c-107">Cuando se usan estos subtipos, establezca el atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) en **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6b9c-108">GUID</span><span class="sxs-lookup"><span data-stu-id="a6b9c-108">GUID</span></span></th>
<th><span data-ttu-id="a6b9c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6b9c-109">Description</span></span></th>
<th><span data-ttu-id="a6b9c-110">Format (etiqueta) (FOURCC)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6b9c-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="a6b9c-112">Codificación de audio avanzada (AAC).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="a6b9c-113">Este subtipo se usa para AAC incluido en un archivo AVI con una etiqueta de formato de audio igual a 0x00FF.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="a6b9c-114">Para obtener más información, consulte el <a href="aac-decoder.md"><strong>descodificador AAC</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="a6b9c-115">Definido en wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="a6b9c-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="a6b9c-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="a6b9c-118">Codificación de audio avanzada (AAC).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a6b9c-119">Equivalente a MEDIASUBTYPE_MPEG_HEAAC, definido en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="a6b9c-120">La secuencia puede contener datos AAC sin formato o datos AAC en una secuencia de flujo de transporte de datos (ADTS) de audio.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="a6b9c-121">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="a6b9c-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="a6b9c-122"><a href="aac-decoder.md"><strong>Descodificador AAC</strong></a></span><span class="sxs-lookup"><span data-stu-id="a6b9c-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="a6b9c-123"><a href="mpeg-4-file-source.md">Origen de archivo MPEG-4</a></span><span class="sxs-lookup"><span data-stu-id="a6b9c-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="a6b9c-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="a6b9c-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-126">Not used.</span></span></td>
<td><span data-ttu-id="a6b9c-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="a6b9c-129">Códec de audio sin pérdida de Apple</span><span class="sxs-lookup"><span data-stu-id="a6b9c-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="a6b9c-130">Compatible con Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-131">WAVE_FORMAT_ALAC (0x6C61)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="a6b9c-133">Audio de varias velocidades Adaptative</span><span class="sxs-lookup"><span data-stu-id="a6b9c-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="a6b9c-134">Se admite en Windows 8.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="a6b9c-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="a6b9c-137">Audio de banda ancha multifrecuencia Adaptative</span><span class="sxs-lookup"><span data-stu-id="a6b9c-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="a6b9c-138">Se admite en Windows 8.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="a6b9c-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="a6b9c-141">Se admite en Windows 8.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="a6b9c-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="a6b9c-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="a6b9c-145">El mismo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, que se define en ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="a6b9c-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="a6b9c-146">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="a6b9c-148">Audio Dolby AC-3 en una interfaz digital de Sony/Philips (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="a6b9c-149">Este valor GUID es idéntico a los siguientes subtipos:</span><span class="sxs-lookup"><span data-stu-id="a6b9c-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="a6b9c-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definido en ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="a6b9c-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definido en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="a6b9c-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="a6b9c-154">Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="a6b9c-155">El mismo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, que se define en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-156">None</span><span class="sxs-lookup"><span data-stu-id="a6b9c-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="a6b9c-158">Datos de audio cifrados usados con la ruta de audio segura.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="a6b9c-159">WAVE_FORMAT_DRM (0x0009)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="a6b9c-161">Audio de sistemas de Digital Theater (DTS).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="a6b9c-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="a6b9c-164">Códec de audio sin pérdida de servicio</span><span class="sxs-lookup"><span data-stu-id="a6b9c-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="a6b9c-165">Compatible con Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-166">WAVE_FORMAT_FLAC (0xF1AC)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="a6b9c-168">Audio de punto flotante IEEE sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="a6b9c-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="a6b9c-171">Audio de punto flotante IEEE sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="a6b9c-172">None</span><span class="sxs-lookup"><span data-stu-id="a6b9c-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="a6b9c-174">Capa de audio MPEG-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="a6b9c-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="a6b9c-177">Carga de audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="a6b9c-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="a6b9c-180">Códec de voz de Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="a6b9c-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="a6b9c-183">Opus</span><span class="sxs-lookup"><span data-stu-id="a6b9c-183">Opus</span></span><br/> <span data-ttu-id="a6b9c-184">Compatible con Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="a6b9c-185">WAVE_FORMAT_OPUS (0x704F)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="a6b9c-187">Audio PCM sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="a6b9c-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="a6b9c-190">Audio QCELP (predicción lineal entusiasmada de código Qualcomm).</span><span class="sxs-lookup"><span data-stu-id="a6b9c-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="a6b9c-191">None</span><span class="sxs-lookup"><span data-stu-id="a6b9c-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="a6b9c-193">Windows Media Audio 9 Professional codec a través de S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="a6b9c-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="a6b9c-196">Códec de Windows Media Audio 9 sin pérdida de Windows Media Audio Códec de 9,1.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="a6b9c-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6b9c-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="a6b9c-199">Códec Windows Media Audio 8, códec de Windows Media Audio 9 o Windows Media Audio Códec 9,1.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="a6b9c-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6b9c-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="a6b9c-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="a6b9c-202">Códec Windows Media Audio 9 Professional o Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="a6b9c-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="a6b9c-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a6b9c-204">Las etiquetas de formato enumeradas en la tercera columna de esta tabla se usan en la estructura **WAVEFORMATEX** y se definen en el archivo de encabezado mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="a6b9c-205">Dada una etiqueta de formato de audio, puede crear un GUID de subtipo de audio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="a6b9c-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="a6b9c-206">Comience con el valor **MFAudioFormat \_ base**, que se define en mfaph. i.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="a6b9c-207">Reemplace el primer **valor DWORD** de este GUID por la etiqueta Format.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="a6b9c-208">Puede usar la macro [**definir \_ \_ GUID de MEDIATYPE**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para definir una nueva constante GUID que siga este patrón.</span><span class="sxs-lookup"><span data-stu-id="a6b9c-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6b9c-209">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6b9c-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b9c-210">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="a6b9c-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="a6b9c-211">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a6b9c-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a6b9c-212">GUID de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a6b9c-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="a6b9c-213">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="a6b9c-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




