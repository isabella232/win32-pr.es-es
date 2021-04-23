---
description: En esta sección se enumeran los tipos de medios usados para los datos MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de medios MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44db1f4423365efb7814d61b35c1985142aa14
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910033"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="791cf-103">Tipos de medios MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="791cf-104">En esta sección se enumeran los tipos de medios usados para los datos MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="791cf-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="791cf-105">Secuencia de sistema MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-105">MPEG-1 System Stream</span></span>



| <span data-ttu-id="791cf-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-106">Label</span></span> | <span data-ttu-id="791cf-107">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-107">Value</span></span> |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="791cf-108">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-108">Major type</span></span>            | <span data-ttu-id="791cf-109">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-109">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="791cf-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-110">Subtype</span></span>               | <span data-ttu-id="791cf-111">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="791cf-111">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="791cf-112">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-112">Format Type</span></span>           | <span data-ttu-id="791cf-113">FORMAT \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="791cf-113">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="791cf-114">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-114">Format Structure</span></span>      | [<span data-ttu-id="791cf-115">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="791cf-115">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="791cf-116">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-116">Media Sample Contents</span></span> | <span data-ttu-id="791cf-117">Secuencia de bytes; sin alineación</span><span class="sxs-lookup"><span data-stu-id="791cf-117">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="791cf-118">Secuencia del sistema MPEG-1 desde CD de vídeo (VCD)</span><span class="sxs-lookup"><span data-stu-id="791cf-118">MPEG-1 System Stream from Video CD</span></span>



| <span data-ttu-id="791cf-119">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-119">Label</span></span> | <span data-ttu-id="791cf-120">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-120">Value</span></span> |
|-----------------------|----------------------------|
| <span data-ttu-id="791cf-121">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-121">Major type</span></span>            | <span data-ttu-id="791cf-122">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-122">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="791cf-123">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-123">Subtype</span></span>               | <span data-ttu-id="791cf-124">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="791cf-124">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="791cf-125">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-125">Format Type</span></span>           | <span data-ttu-id="791cf-126">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="791cf-126">GUID\_NULL</span></span>                 |
| <span data-ttu-id="791cf-127">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-127">Format Structure</span></span>      | <span data-ttu-id="791cf-128">None</span><span class="sxs-lookup"><span data-stu-id="791cf-128">None</span></span>                       |
| <span data-ttu-id="791cf-129">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-129">Media Sample Contents</span></span> | <span data-ttu-id="791cf-130">Secuencia de bytes; sin alineación.</span><span class="sxs-lookup"><span data-stu-id="791cf-130">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="791cf-131">Paquete de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-131">MPEG-1 Audio Packet</span></span>



| <span data-ttu-id="791cf-132">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-132">Label</span></span> | <span data-ttu-id="791cf-133">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-133">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="791cf-134">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-134">Major type</span></span>            | <span data-ttu-id="791cf-135">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="791cf-135">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="791cf-136">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-136">Subtype</span></span>               | <span data-ttu-id="791cf-137">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="791cf-137">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="791cf-138">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-138">Format Type</span></span>           | <span data-ttu-id="791cf-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="791cf-139">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="791cf-140">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-140">Format Structure</span></span>      | [<span data-ttu-id="791cf-141">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="791cf-141">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="791cf-142">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-142">Media Sample Contents</span></span> | <span data-ttu-id="791cf-143">Paquete MPEG-1 único, incluido el encabezado de paquete.</span><span class="sxs-lookup"><span data-stu-id="791cf-143">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="791cf-144">Carga de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-144">MPEG-1 Audio Payload</span></span>



| <span data-ttu-id="791cf-145">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-145">Label</span></span> | <span data-ttu-id="791cf-146">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-146">Value</span></span> |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="791cf-147">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-147">Major type</span></span>            | <span data-ttu-id="791cf-148">MEDIATYPE \_ Audio</span><span class="sxs-lookup"><span data-stu-id="791cf-148">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="791cf-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-149">Subtype</span></span>               | <span data-ttu-id="791cf-150">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="791cf-150">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="791cf-151">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-151">Format Type</span></span>           | <span data-ttu-id="791cf-152">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="791cf-152">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="791cf-153">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-153">Format Structure</span></span>      | [<span data-ttu-id="791cf-154">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="791cf-154">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="791cf-155">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-155">Media Sample Contents</span></span> | <span data-ttu-id="791cf-156">Datos de audio MPEG-1 alineados en bytes.</span><span class="sxs-lookup"><span data-stu-id="791cf-156">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="791cf-157">Paquete de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-157">MPEG-1 Video Packet</span></span>



| <span data-ttu-id="791cf-158">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-158">Label</span></span> | <span data-ttu-id="791cf-159">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-159">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="791cf-160">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-160">Major type</span></span>            | <span data-ttu-id="791cf-161">Vídeo \_ DE MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-161">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="791cf-162">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-162">Subtype</span></span>               | <span data-ttu-id="791cf-163">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="791cf-163">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="791cf-164">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-164">Format Type</span></span>           | <span data-ttu-id="791cf-165">FORMAT \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="791cf-165">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="791cf-166">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-166">Format Structure</span></span>      | [<span data-ttu-id="791cf-167">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="791cf-167">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="791cf-168">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-168">Media Sample Contents</span></span> | <span data-ttu-id="791cf-169">Paquete MPEG-1 único, incluido el encabezado de paquete.</span><span class="sxs-lookup"><span data-stu-id="791cf-169">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="791cf-170">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-170">MPEG-1 Video payload</span></span>



| <span data-ttu-id="791cf-171">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-171">Label</span></span> | <span data-ttu-id="791cf-172">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-172">Value</span></span> |
|-----------------------|------------------------------------------|
| <span data-ttu-id="791cf-173">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-173">Major type</span></span>            | <span data-ttu-id="791cf-174">Vídeo \_ DE MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-174">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="791cf-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-175">Subtype</span></span>               | <span data-ttu-id="791cf-176">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="791cf-176">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="791cf-177">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-177">Format Type</span></span>           | <span data-ttu-id="791cf-178">FORMAT \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="791cf-178">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="791cf-179">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-179">Format Structure</span></span>      | [<span data-ttu-id="791cf-180">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="791cf-180">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="791cf-181">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-181">Media Sample Contents</span></span> | <span data-ttu-id="791cf-182">Datos de vídeo MPEG-1 alineados con bytes.</span><span class="sxs-lookup"><span data-stu-id="791cf-182">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="791cf-183">Secuencia de vídeo nativa MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-183">MPEG-1 Native Video Stream</span></span>



| <span data-ttu-id="791cf-184">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-184">Label</span></span> | <span data-ttu-id="791cf-185">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-185">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="791cf-186">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-186">Major type</span></span>            | <span data-ttu-id="791cf-187">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-187">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="791cf-188">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-188">Subtype</span></span>               | <span data-ttu-id="791cf-189">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="791cf-189">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="791cf-190">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-190">Format Type</span></span>           | <span data-ttu-id="791cf-191">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="791cf-191">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="791cf-192">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-192">Format Structure</span></span>      | <span data-ttu-id="791cf-193">None</span><span class="sxs-lookup"><span data-stu-id="791cf-193">None</span></span>                                           |
| <span data-ttu-id="791cf-194">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-194">Media Sample Contents</span></span> | <span data-ttu-id="791cf-195">Matriz de bytes de secuencia de vídeo (sin capa del sistema).</span><span class="sxs-lookup"><span data-stu-id="791cf-195">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="791cf-196">Secuencia de audio nativa MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-196">MPEG-1 Native Audio Stream</span></span>



| <span data-ttu-id="791cf-197">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="791cf-197">Label</span></span> | <span data-ttu-id="791cf-198">Value</span><span class="sxs-lookup"><span data-stu-id="791cf-198">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="791cf-199">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="791cf-199">Major type</span></span>            | <span data-ttu-id="791cf-200">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="791cf-200">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="791cf-201">Subtype</span><span class="sxs-lookup"><span data-stu-id="791cf-201">Subtype</span></span>               | <span data-ttu-id="791cf-202">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="791cf-202">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="791cf-203">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-203">Format Type</span></span>           | <span data-ttu-id="791cf-204">GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="791cf-204">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="791cf-205">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="791cf-205">Format Structure</span></span>      | <span data-ttu-id="791cf-206">None</span><span class="sxs-lookup"><span data-stu-id="791cf-206">None</span></span>                                           |
| <span data-ttu-id="791cf-207">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="791cf-207">Media Sample Contents</span></span> | <span data-ttu-id="791cf-208">Matriz de bytes de secuencia de audio (sin capa del sistema).</span><span class="sxs-lookup"><span data-stu-id="791cf-208">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="791cf-209">Comentarios</span><span class="sxs-lookup"><span data-stu-id="791cf-209">Remarks</span></span>

<span data-ttu-id="791cf-210">Los filtros MPEG-1 de DirectShow admiten estos tipos como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="791cf-210">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="791cf-211">Filtrar</span><span class="sxs-lookup"><span data-stu-id="791cf-211">Filter</span></span>               | <span data-ttu-id="791cf-212">Dirección</span><span class="sxs-lookup"><span data-stu-id="791cf-212">Direction</span></span> | <span data-ttu-id="791cf-213">Tipos de medios admitidos</span><span class="sxs-lookup"><span data-stu-id="791cf-213">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="791cf-214">Divisor MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-214">MPEG-1 Splitter</span></span>      | <span data-ttu-id="791cf-215">Entrada</span><span class="sxs-lookup"><span data-stu-id="791cf-215">Input</span></span>     | <span data-ttu-id="791cf-216">Secuencia del sistema MPEG-1MPEG-1 desde CD de vídeo (VCD)</span><span class="sxs-lookup"><span data-stu-id="791cf-216">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="791cf-217">Divisor MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-217">MPEG-1 Splitter</span></span>      | <span data-ttu-id="791cf-218">Resultados</span><span class="sxs-lookup"><span data-stu-id="791cf-218">Output</span></span>    | <span data-ttu-id="791cf-219">Carga de audio MPEG-1 Paquete de audioMPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-219">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="791cf-220">Paquete de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-220">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="791cf-221">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-221">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="791cf-222">Códec de audio de software</span><span class="sxs-lookup"><span data-stu-id="791cf-222">Software Audio Codec</span></span> | <span data-ttu-id="791cf-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="791cf-223">Input</span></span>     | <span data-ttu-id="791cf-224">Carga de audio MPEG-1 Paquete de audioMPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-224">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="791cf-225">Códec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="791cf-225">Software Video Codec</span></span> | <span data-ttu-id="791cf-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="791cf-226">Input</span></span>     | <span data-ttu-id="791cf-227">Carga de vídeo MPEG-1 Paquete de vídeoMPEG-1</span><span class="sxs-lookup"><span data-stu-id="791cf-227">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="791cf-228">Códec de audio de software</span><span class="sxs-lookup"><span data-stu-id="791cf-228">Software Audio Codec</span></span> | <span data-ttu-id="791cf-229">Resultados</span><span class="sxs-lookup"><span data-stu-id="791cf-229">Output</span></span>    | <span data-ttu-id="791cf-230">Audio de PCM</span><span class="sxs-lookup"><span data-stu-id="791cf-230">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="791cf-231">Códec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="791cf-231">Software Video Codec</span></span> | <span data-ttu-id="791cf-232">Resultados</span><span class="sxs-lookup"><span data-stu-id="791cf-232">Output</span></span>    | <span data-ttu-id="791cf-233">Vídeo sin comprimir (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="791cf-233">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="791cf-234">Los paquetes de vídeo MPEG-1 y los tipos de medios de carga útil contienen un encabezado de secuencia completo para que los datos se puedan reproducir desde el centro de un archivo sin necesidad de un encabezado de secuencia para inicializar la reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="791cf-234">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="791cf-235">El encabezado de secuencia de vídeo se anexa al tipo de datos de vídeo para el vídeo MPEG para que la reproducción pueda comenzar desde el medio de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="791cf-235">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="791cf-236">La longitud de este campo es de hasta 140 bytes; incluye el código de inicio del encabezado de secuencia (0x000001B3) al principio, junto con las matrices de cuantificación que se encuentran en el primer encabezado de secuencia encontrado.</span><span class="sxs-lookup"><span data-stu-id="791cf-236">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




