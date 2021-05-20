---
description: En esta sección se describe Media Foundation compatibilidad con archivos de Contenedor multimedia de Matroska (DOCKER).
title: Compatibilidad con El contenedor multimedia de Matroska (TAPE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154224"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="61be8-103">Compatibilidad con El contenedor multimedia de Matroska (TAPE)</span><span class="sxs-lookup"><span data-stu-id="61be8-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="61be8-104">En esta sección se describe Media Foundation compatibilidad con archivos de Contenedor multimedia de Matroska (DOCKER).</span><span class="sxs-lookup"><span data-stu-id="61be8-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="61be8-105">El formato MPEG puede admitir varios códecs de audio y vídeo, como el audio H.264 y AAC.</span><span class="sxs-lookup"><span data-stu-id="61be8-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="61be8-106">En general, los contenedores describen cómo se scriben los datos de vídeo y audio y qué información complementaria se usa para describir esas secuencias de A/V.</span><span class="sxs-lookup"><span data-stu-id="61be8-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="61be8-107">Los contenedores también pueden incluir datos que complementan las secuencias de A/V, como el título, los idiomas de las secuencias de audio, las pistas de subtítulos o subtítulos, las fuentes para esos subtítulos, imágenes, información de capítulos y menús.</span><span class="sxs-lookup"><span data-stu-id="61be8-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="61be8-108">CSV es un formato muy flexible que admite muchas de estas características de contenedor.</span><span class="sxs-lookup"><span data-stu-id="61be8-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="61be8-109">Para obtener más información sobre el formato CSV, vea [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="61be8-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="61be8-110">Compatibilidad con características de contenedor DE CONTENEDOR</span><span class="sxs-lookup"><span data-stu-id="61be8-110">MKV container feature support</span></span>
<span data-ttu-id="61be8-111">Las características del contenedor DE PERO son compatibles con Media Foundation de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="61be8-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="61be8-112">Si hay una o varias pistas de vídeo, se reproducirá la primera pista.</span><span class="sxs-lookup"><span data-stu-id="61be8-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="61be8-113">Si hay una o varias pistas de audio presentes, se reproducirá la primera pista.</span><span class="sxs-lookup"><span data-stu-id="61be8-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="61be8-114">Se admiten pistas de título, pero no se seleccionan (se reproducen) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61be8-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="61be8-115">Si hay una o varias fuentes o imágenes, los títulos e imágenes no se representarán, aunque el archivo se cargará y reproducirá.</span><span class="sxs-lookup"><span data-stu-id="61be8-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="61be8-116">La información del menú no se admite y no se mostrará, pero el archivo se cargará y reproducirá.</span><span class="sxs-lookup"><span data-stu-id="61be8-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="61be8-117">Si los archivos con capítulos hacen referencia a archivos complementarios, los archivos complementarios no se reproducirán.</span><span class="sxs-lookup"><span data-stu-id="61be8-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="61be8-118">Las imágenes en miniatura están disponibles al buscar archivos en unidades USB mediante el explorador de archivos.</span><span class="sxs-lookup"><span data-stu-id="61be8-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="61be8-119">Este conjunto de características debe permitir la reproducción de la mayoría de los archivos MPEG si contienen códecs compatibles.</span><span class="sxs-lookup"><span data-stu-id="61be8-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="61be8-120">Se admiten los archivos MPEG que contienen pistas de audio y vídeo codificadas con los códecs enumerados en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="61be8-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="61be8-121">Códecs MPEG admitidos</span><span class="sxs-lookup"><span data-stu-id="61be8-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="61be8-122">Compatibilidad con códecs de vídeo para MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-122">Video codec support for MKV</span></span>

<span data-ttu-id="61be8-123">Identificador de Matroska: V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="61be8-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="61be8-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="61be8-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="61be8-125">Descripción: vídeo H.264</span><span class="sxs-lookup"><span data-stu-id="61be8-125">Description: H.264 video</span></span>
- <span data-ttu-id="61be8-126">Identificadores de FourCC o WAV: H264</span><span class="sxs-lookup"><span data-stu-id="61be8-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="61be8-127">Identificador de Matroska: V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="61be8-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="61be8-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="61be8-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="61be8-129">Descripción: vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="61be8-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="61be8-130">Identificador de Matroska: V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="61be8-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="61be8-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="61be8-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="61be8-132">Descripción: vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="61be8-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="61be8-133">Identificadores fourCC o WAV: MPG1</span><span class="sxs-lookup"><span data-stu-id="61be8-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="61be8-134">Identificador de Matroska: V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="61be8-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="61be8-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="61be8-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="61be8-136">Descripción: Códec Microsoft MPEG 4 versión 3</span><span class="sxs-lookup"><span data-stu-id="61be8-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="61be8-137">Identificadores de FourCC o WAV: MP43</span><span class="sxs-lookup"><span data-stu-id="61be8-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="61be8-138">Identificador de Matroska: V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="61be8-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="61be8-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="61be8-140">Descripción: vídeo MPEG-4, parte 2</span><span class="sxs-lookup"><span data-stu-id="61be8-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="61be8-141">Identificadores de FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="61be8-142">Identificador de Matroska: V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="61be8-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="61be8-143">Descripción: se asigna a varios códecs que normalmente se admiten en el formato AVI que están disponibles en la consola.</span><span class="sxs-lookup"><span data-stu-id="61be8-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="61be8-144">Identificador de Matroska: V_THEORA</span><span class="sxs-lookup"><span data-stu-id="61be8-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="61be8-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="61be8-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="61be8-146">Descripción: Theora</span><span class="sxs-lookup"><span data-stu-id="61be8-146">Description: Theora</span></span>
- <span data-ttu-id="61be8-147">Identificadores de FourCC o WAV: theo</span><span class="sxs-lookup"><span data-stu-id="61be8-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="61be8-148">Identificador de Matroska: V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="61be8-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="61be8-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="61be8-150">Descripción: Perfil simple MPEG4 ISO (DivX4)</span><span class="sxs-lookup"><span data-stu-id="61be8-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="61be8-151">Identificadores de FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="61be8-152">Identificador de Matroska: V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="61be8-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="61be8-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="61be8-154">Descripción: Perfil sencillo avanzado de MPEG4 ISO (DivX5, DivD, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="61be8-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="61be8-155">Identificadores de FourCC o WAV: MP4V</span><span class="sxs-lookup"><span data-stu-id="61be8-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="61be8-156">Identificador de Matroska: V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="61be8-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="61be8-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="61be8-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="61be8-158">Descripción: HEVC/H.265</span><span class="sxs-lookup"><span data-stu-id="61be8-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="61be8-159">Identificadores fourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="61be8-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="61be8-160">Identificador de Matroska: V_VP8</span><span class="sxs-lookup"><span data-stu-id="61be8-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="61be8-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="61be8-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="61be8-162">Descripción: Formato de códec VP8</span><span class="sxs-lookup"><span data-stu-id="61be8-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="61be8-163">Identificadores fourCC o WAV: VP80</span><span class="sxs-lookup"><span data-stu-id="61be8-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="61be8-164">Identificador de Matroska: V_VP9</span><span class="sxs-lookup"><span data-stu-id="61be8-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="61be8-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="61be8-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="61be8-166">Descripción: Formato de códec VP9</span><span class="sxs-lookup"><span data-stu-id="61be8-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="61be8-167">Identificadores fourCC o WAV: VP90</span><span class="sxs-lookup"><span data-stu-id="61be8-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="61be8-168">Identificador de Matroska: V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="61be8-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="61be8-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="61be8-170">Descripción: Motion JPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="61be8-171">Identificadores de FourCC o WAV: MJPG</span><span class="sxs-lookup"><span data-stu-id="61be8-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="61be8-172">Identificador de Matroska: V_AV1</span><span class="sxs-lookup"><span data-stu-id="61be8-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="61be8-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="61be8-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="61be8-174">Descripción: AOMedia Video 1</span><span class="sxs-lookup"><span data-stu-id="61be8-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="61be8-175">Identificadores fourCC o WAV: AV01</span><span class="sxs-lookup"><span data-stu-id="61be8-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="61be8-176">Compatibilidad con códecs de audio para MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-176">Audio codec support for MKV</span></span>

<span data-ttu-id="61be8-177">Identificador de Matroska: A_AAC</span><span class="sxs-lookup"><span data-stu-id="61be8-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="61be8-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="61be8-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="61be8-179">Descripción: Codificación de audio avanzada (AAC)</span><span class="sxs-lookup"><span data-stu-id="61be8-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="61be8-180">Identificadores fourCC o WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="61be8-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="61be8-181">Identificador de Matroska: A_AC3</span><span class="sxs-lookup"><span data-stu-id="61be8-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="61be8-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="61be8-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="61be8-183">Descripción: Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="61be8-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="61be8-184">Identificadores de FourCC o WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="61be8-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="61be8-185">Identificador de Matroska: A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="61be8-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="61be8-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="61be8-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="61be8-187">Descripción: MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="61be8-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="61be8-188">Identificadores de FourCC o WAV: WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="61be8-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="61be8-189">Identificador de Matroska: A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="61be8-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="61be8-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="61be8-191">Descripción: carga de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="61be8-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="61be8-192">Identificadores de FourCC o WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="61be8-193">Identificador de Matroska: A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="61be8-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="61be8-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="61be8-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="61be8-195">Descripción: Audio PCM sin comprimir</span><span class="sxs-lookup"><span data-stu-id="61be8-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="61be8-196">Identificadores de FourCC o WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="61be8-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="61be8-197">Identificador de Matroska: A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="61be8-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="61be8-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="61be8-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="61be8-199">Descripción: Audio PCM sin comprimir</span><span class="sxs-lookup"><span data-stu-id="61be8-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="61be8-200">Identificadores de FourCC o WAV: WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="61be8-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="61be8-201">Identificador de Matroska: A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="61be8-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="61be8-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="61be8-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="61be8-203">Descripción: Audio de punto flotante IEEE sin comprimir</span><span class="sxs-lookup"><span data-stu-id="61be8-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="61be8-204">Identificadores fourCC o WAV: WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="61be8-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="61be8-205">Identificador de Matroska: A_ALAC</span><span class="sxs-lookup"><span data-stu-id="61be8-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="61be8-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="61be8-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="61be8-207">Descripción: Códec de audio sin pérdida de Apple</span><span class="sxs-lookup"><span data-stu-id="61be8-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="61be8-208">Identificadores fourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="61be8-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="61be8-209">Identificador de Matroska: A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="61be8-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="61be8-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="61be8-211">Descripción: MPEG Audio 1, 2 Capa II</span><span class="sxs-lookup"><span data-stu-id="61be8-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="61be8-212">Identificadores fourCC o WAV: WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="61be8-213">Identificador de Matroska: A_DTS</span><span class="sxs-lookup"><span data-stu-id="61be8-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="61be8-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="61be8-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="61be8-215">Descripción: Sistema digital de traslación</span><span class="sxs-lookup"><span data-stu-id="61be8-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="61be8-216">Identificadores fourCC o WAV: WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="61be8-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="61be8-217">Identificador de Matroska: A_OPUS</span><span class="sxs-lookup"><span data-stu-id="61be8-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="61be8-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="61be8-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="61be8-219">Descripción: Uno de los dos</span><span class="sxs-lookup"><span data-stu-id="61be8-219">Description: Opus</span></span>
- <span data-ttu-id="61be8-220">Identificadores fourCC o WAV: WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="61be8-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="61be8-221">Identificador de Matroska: A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="61be8-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="61be8-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="61be8-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="61be8-223">Descripción: Pombis</span><span class="sxs-lookup"><span data-stu-id="61be8-223">Description: Vorbis</span></span>
- <span data-ttu-id="61be8-224">Identificadores fourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="61be8-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="61be8-225">Identificador de Matroska: A_FLAC</span><span class="sxs-lookup"><span data-stu-id="61be8-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="61be8-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="61be8-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="61be8-227">Descripción: Códec de audio sin pérdida de datos gratuito</span><span class="sxs-lookup"><span data-stu-id="61be8-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="61be8-228">Identificadores de FourCC o WAV: WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="61be8-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="61be8-229">Identificador de Matroska: A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="61be8-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="61be8-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="61be8-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="61be8-231">Descripción: Codificación de audio avanzada (AAC)</span><span class="sxs-lookup"><span data-stu-id="61be8-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="61be8-232">Identificadores de FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="61be8-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="61be8-233">Identificador de Matroska: A_EAC3</span><span class="sxs-lookup"><span data-stu-id="61be8-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="61be8-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="61be8-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="61be8-235">Descripción: AC-3 mejorado</span><span class="sxs-lookup"><span data-stu-id="61be8-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="61be8-236">Identificadores fourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="61be8-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="61be8-237">Identificador de Matroska: A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="61be8-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="61be8-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="61be8-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="61be8-239">Descripción: Dolby TrueHD</span><span class="sxs-lookup"><span data-stu-id="61be8-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="61be8-240">Identificadores fourCC o WAV:</span><span class="sxs-lookup"><span data-stu-id="61be8-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="61be8-241">Identificador de Matroska: A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="61be8-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="61be8-242">MSFT Media Foundation MF_MT_SUBTYPE: se asigna a varios WAVE_FORMAT de audio definidos en mmreg.h</span><span class="sxs-lookup"><span data-stu-id="61be8-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="61be8-243">Compatibilidad con códecs de subtítulos para MPEG</span><span class="sxs-lookup"><span data-stu-id="61be8-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="61be8-244">Identificador de Matroska: S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="61be8-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="61be8-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="61be8-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="61be8-246">Descripción: texto ASCII</span><span class="sxs-lookup"><span data-stu-id="61be8-246">Description: ASCII text</span></span>

<span data-ttu-id="61be8-247">Identificador de Matroska: S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="61be8-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="61be8-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="61be8-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="61be8-249">Descripción: Texto sin formato UTF-8</span><span class="sxs-lookup"><span data-stu-id="61be8-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="61be8-250">Identificador de Matroska: S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="61be8-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="61be8-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="61be8-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="61be8-252">Descripción: Formato de subtítulos</span><span class="sxs-lookup"><span data-stu-id="61be8-252">Description: Subtitles Format</span></span>

<span data-ttu-id="61be8-253">Identificador de Matroska: S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="61be8-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="61be8-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="61be8-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="61be8-255">Descripción: Formato avanzado de subtítulos</span><span class="sxs-lookup"><span data-stu-id="61be8-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="61be8-256">Identificador de Matroska: S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="61be8-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="61be8-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="61be8-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="61be8-258">Descripción: subtítulos vobSub</span><span class="sxs-lookup"><span data-stu-id="61be8-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="61be8-259">Identificador de Matroska: S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="61be8-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="61be8-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="61be8-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="61be8-261">Descripción: Subtítulos de gráficos de presentación de HDMV (PGS)</span><span class="sxs-lookup"><span data-stu-id="61be8-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="61be8-262">Detalles técnicos sobre códecs</span><span class="sxs-lookup"><span data-stu-id="61be8-262">Technical details regarding codecs</span></span>

<span data-ttu-id="61be8-263">Consulte lo siguiente para obtener detalles técnicos sobre códecs.</span><span class="sxs-lookup"><span data-stu-id="61be8-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="61be8-264">Matroska Codec Specs</span><span class="sxs-lookup"><span data-stu-id="61be8-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="61be8-265">GUID de subtipo de audio</span><span class="sxs-lookup"><span data-stu-id="61be8-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="61be8-266">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="61be8-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="61be8-267">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61be8-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61be8-268">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61be8-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="61be8-269">Media Foundation de programación</span><span class="sxs-lookup"><span data-stu-id="61be8-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



