---
description: En esta sección se enumeran los tipos de medios que se usan para los datos MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Tipos de medios MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689634"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="c85dd-103">Tipos de medios MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="c85dd-104">En esta sección se enumeran los tipos de medios que se usan para los datos MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="c85dd-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="c85dd-105">Secuencia de sistema MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-105">MPEG-1 System Stream</span></span>



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="c85dd-106">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-106">Major type</span></span>            | <span data-ttu-id="c85dd-107">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c85dd-107">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="c85dd-108">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-108">Subtype</span></span>               | <span data-ttu-id="c85dd-109">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="c85dd-109">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="c85dd-110">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-110">Format Type</span></span>           | <span data-ttu-id="c85dd-111">FORMATO \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="c85dd-111">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="c85dd-112">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-112">Format Structure</span></span>      | [<span data-ttu-id="c85dd-113">**\_MPEGSYSTEMTYPE AM**</span><span class="sxs-lookup"><span data-stu-id="c85dd-113">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="c85dd-114">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-114">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-115">Secuencia de bytes; sin alineación</span><span class="sxs-lookup"><span data-stu-id="c85dd-115">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="c85dd-116">Secuencia del sistema MPEG-1 desde el CD de vídeo</span><span class="sxs-lookup"><span data-stu-id="c85dd-116">MPEG-1 System Stream from Video CD</span></span>



|                       |                            |
|-----------------------|----------------------------|
| <span data-ttu-id="c85dd-117">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-117">Major type</span></span>            | <span data-ttu-id="c85dd-118">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c85dd-118">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="c85dd-119">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-119">Subtype</span></span>               | <span data-ttu-id="c85dd-120">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="c85dd-120">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="c85dd-121">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-121">Format Type</span></span>           | <span data-ttu-id="c85dd-122">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="c85dd-122">GUID\_NULL</span></span>                 |
| <span data-ttu-id="c85dd-123">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-123">Format Structure</span></span>      | <span data-ttu-id="c85dd-124">None</span><span class="sxs-lookup"><span data-stu-id="c85dd-124">None</span></span>                       |
| <span data-ttu-id="c85dd-125">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-125">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-126">Secuencia de bytes; sin alineación.</span><span class="sxs-lookup"><span data-stu-id="c85dd-126">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="c85dd-127">Paquete de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-127">MPEG-1 Audio Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="c85dd-128">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-128">Major type</span></span>            | <span data-ttu-id="c85dd-129">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c85dd-129">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="c85dd-130">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-130">Subtype</span></span>               | <span data-ttu-id="c85dd-131">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="c85dd-131">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="c85dd-132">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-132">Format Type</span></span>           | <span data-ttu-id="c85dd-133">DAR formato a \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="c85dd-133">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="c85dd-134">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-134">Format Structure</span></span>      | [<span data-ttu-id="c85dd-135">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="c85dd-135">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="c85dd-136">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-136">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-137">Paquete MPEG-1 único, incluido el encabezado de paquete.</span><span class="sxs-lookup"><span data-stu-id="c85dd-137">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="c85dd-138">Carga de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-138">MPEG-1 Audio Payload</span></span>



|                       |                                            |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="c85dd-139">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-139">Major type</span></span>            | <span data-ttu-id="c85dd-140">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c85dd-140">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="c85dd-141">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-141">Subtype</span></span>               | <span data-ttu-id="c85dd-142">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="c85dd-142">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="c85dd-143">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-143">Format Type</span></span>           | <span data-ttu-id="c85dd-144">DAR formato a \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="c85dd-144">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="c85dd-145">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-145">Format Structure</span></span>      | [<span data-ttu-id="c85dd-146">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="c85dd-146">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="c85dd-147">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-147">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-148">Datos de audio MPEG-1 alineados en bytes.</span><span class="sxs-lookup"><span data-stu-id="c85dd-148">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="c85dd-149">Paquete de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-149">MPEG-1 Video Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="c85dd-150">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-150">Major type</span></span>            | <span data-ttu-id="c85dd-151">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c85dd-151">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="c85dd-152">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-152">Subtype</span></span>               | <span data-ttu-id="c85dd-153">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="c85dd-153">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="c85dd-154">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-154">Format Type</span></span>           | <span data-ttu-id="c85dd-155">FORMATO \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="c85dd-155">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="c85dd-156">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-156">Format Structure</span></span>      | [<span data-ttu-id="c85dd-157">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="c85dd-157">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="c85dd-158">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-158">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-159">Paquete MPEG-1 único, incluido el encabezado de paquete.</span><span class="sxs-lookup"><span data-stu-id="c85dd-159">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="c85dd-160">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-160">MPEG-1 Video payload</span></span>



|                       |                                          |
|-----------------------|------------------------------------------|
| <span data-ttu-id="c85dd-161">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-161">Major type</span></span>            | <span data-ttu-id="c85dd-162">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c85dd-162">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="c85dd-163">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-163">Subtype</span></span>               | <span data-ttu-id="c85dd-164">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="c85dd-164">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="c85dd-165">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-165">Format Type</span></span>           | <span data-ttu-id="c85dd-166">FORMATO \_ MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="c85dd-166">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="c85dd-167">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-167">Format Structure</span></span>      | [<span data-ttu-id="c85dd-168">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="c85dd-168">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="c85dd-169">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-169">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-170">Datos de vídeo MPEG-1 alineados en bytes.</span><span class="sxs-lookup"><span data-stu-id="c85dd-170">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="c85dd-171">Secuencia de vídeo de MPEG-1 nativo</span><span class="sxs-lookup"><span data-stu-id="c85dd-171">MPEG-1 Native Video Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="c85dd-172">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-172">Major type</span></span>            | <span data-ttu-id="c85dd-173">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c85dd-173">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="c85dd-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-174">Subtype</span></span>               | <span data-ttu-id="c85dd-175">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="c85dd-175">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="c85dd-176">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-176">Format Type</span></span>           | <span data-ttu-id="c85dd-177">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="c85dd-177">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="c85dd-178">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-178">Format Structure</span></span>      | <span data-ttu-id="c85dd-179">None</span><span class="sxs-lookup"><span data-stu-id="c85dd-179">None</span></span>                                           |
| <span data-ttu-id="c85dd-180">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-180">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-181">Matriz de bytes de secuencia de vídeo (sin capa del sistema).</span><span class="sxs-lookup"><span data-stu-id="c85dd-181">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="c85dd-182">Secuencia de audio de MPEG-1 nativo</span><span class="sxs-lookup"><span data-stu-id="c85dd-182">MPEG-1 Native Audio Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="c85dd-183">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="c85dd-183">Major type</span></span>            | <span data-ttu-id="c85dd-184">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c85dd-184">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="c85dd-185">Subtype</span><span class="sxs-lookup"><span data-stu-id="c85dd-185">Subtype</span></span>               | <span data-ttu-id="c85dd-186">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="c85dd-186">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="c85dd-187">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-187">Format Type</span></span>           | <span data-ttu-id="c85dd-188">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="c85dd-188">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="c85dd-189">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="c85dd-189">Format Structure</span></span>      | <span data-ttu-id="c85dd-190">None</span><span class="sxs-lookup"><span data-stu-id="c85dd-190">None</span></span>                                           |
| <span data-ttu-id="c85dd-191">Contenido de ejemplo multimedia</span><span class="sxs-lookup"><span data-stu-id="c85dd-191">Media Sample Contents</span></span> | <span data-ttu-id="c85dd-192">Matriz de bytes de secuencia de audio (sin capa del sistema).</span><span class="sxs-lookup"><span data-stu-id="c85dd-192">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c85dd-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c85dd-193">Remarks</span></span>

<span data-ttu-id="c85dd-194">Los filtros MPEG-1 de DirectShow admiten estos tipos de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="c85dd-194">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="c85dd-195">Filter</span><span class="sxs-lookup"><span data-stu-id="c85dd-195">Filter</span></span>               | <span data-ttu-id="c85dd-196">Dirección</span><span class="sxs-lookup"><span data-stu-id="c85dd-196">Direction</span></span> | <span data-ttu-id="c85dd-197">Tipos de medios admitidos</span><span class="sxs-lookup"><span data-stu-id="c85dd-197">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85dd-198">Separador MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-198">MPEG-1 Splitter</span></span>      | <span data-ttu-id="c85dd-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="c85dd-199">Input</span></span>     | <span data-ttu-id="c85dd-200">Flujo del sistema streamMPEG-1 del sistema MPEG-1 del CD de vídeo</span><span class="sxs-lookup"><span data-stu-id="c85dd-200">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="c85dd-201">Separador MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-201">MPEG-1 Splitter</span></span>      | <span data-ttu-id="c85dd-202">Output</span><span class="sxs-lookup"><span data-stu-id="c85dd-202">Output</span></span>    | <span data-ttu-id="c85dd-203">Carga de audio packetMPEG-1 de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-203">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="c85dd-204">Paquete de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-204">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="c85dd-205">Carga de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-205">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="c85dd-206">Códec de audio de software</span><span class="sxs-lookup"><span data-stu-id="c85dd-206">Software Audio Codec</span></span> | <span data-ttu-id="c85dd-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="c85dd-207">Input</span></span>     | <span data-ttu-id="c85dd-208">Carga de audio packetMPEG-1 de audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-208">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="c85dd-209">Códec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="c85dd-209">Software Video Codec</span></span> | <span data-ttu-id="c85dd-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="c85dd-210">Input</span></span>     | <span data-ttu-id="c85dd-211">Carga de vídeo MPEG-1 video packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="c85dd-211">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="c85dd-212">Códec de audio de software</span><span class="sxs-lookup"><span data-stu-id="c85dd-212">Software Audio Codec</span></span> | <span data-ttu-id="c85dd-213">Output</span><span class="sxs-lookup"><span data-stu-id="c85dd-213">Output</span></span>    | <span data-ttu-id="c85dd-214">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="c85dd-214">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="c85dd-215">Códec de vídeo de software</span><span class="sxs-lookup"><span data-stu-id="c85dd-215">Software Video Codec</span></span> | <span data-ttu-id="c85dd-216">Output</span><span class="sxs-lookup"><span data-stu-id="c85dd-216">Output</span></span>    | <span data-ttu-id="c85dd-217">Vídeo sin comprimir (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span><span class="sxs-lookup"><span data-stu-id="c85dd-217">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="c85dd-218">Los tipos de medios de paquete y carga de vídeo MPEG-1 contienen un encabezado de secuencia completo para que los datos se puedan reproducir desde el centro de un archivo sin necesidad de un encabezado de secuencia para inicializar la reproducción del vídeo.</span><span class="sxs-lookup"><span data-stu-id="c85dd-218">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="c85dd-219">El encabezado de la secuencia de vídeo se anexa al tipo de datos de vídeo del vídeo MPEG para que el juego pueda comenzar desde el medio de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="c85dd-219">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="c85dd-220">La longitud de este campo es de hasta 140 bytes. incluye el código de inicio del encabezado de secuencia (0x000001B3) al principio, junto con las matrices de cuantificación encontradas en el primer encabezado de secuencia encontrado.</span><span class="sxs-lookup"><span data-stu-id="c85dd-220">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




