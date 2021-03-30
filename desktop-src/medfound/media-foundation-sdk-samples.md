---
description: En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation. Encoding SamplesPlayback SamplesPlug-InsSource Reader SamplesVideo CaptureMiscellaneous SamplesDeprecated u obsoleto SamplesRelated temas
ms.assetid: 9d460107-ec12-4df5-a7a9-d19943685599
title: Muestras de SDK de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f335b5ba744b098efdb7570aa861ad36fc9216cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820247"
---
# <a name="media-foundation-sdk-samples"></a><span data-ttu-id="f532e-103">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f532e-103">Media Foundation SDK Samples</span></span>

<span data-ttu-id="f532e-104">En esta sección se describen las aplicaciones de ejemplo que muestran cómo usar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f532e-104">This section describes sample applications that demonstrate how to use Media Foundation.</span></span>

-   [<span data-ttu-id="f532e-105">Ejemplos de codificación</span><span class="sxs-lookup"><span data-stu-id="f532e-105">Encoding Samples</span></span>](#encoding-samples)
-   [<span data-ttu-id="f532e-106">Ejemplos de reproducción</span><span class="sxs-lookup"><span data-stu-id="f532e-106">Playback Samples</span></span>](#playback-samples)
-   [<span data-ttu-id="f532e-107">Complementos de</span><span class="sxs-lookup"><span data-stu-id="f532e-107">Plug-Ins</span></span>](#plug-ins)
-   [<span data-ttu-id="f532e-108">Ejemplos de lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="f532e-108">Source Reader Samples</span></span>](#source-reader-samples)
-   [<span data-ttu-id="f532e-109">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f532e-109">Video Capture</span></span>](#video-capture)
-   [<span data-ttu-id="f532e-110">Varios ejemplos</span><span class="sxs-lookup"><span data-stu-id="f532e-110">Miscellaneous Samples</span></span>](#miscellaneous-samples)
-   [<span data-ttu-id="f532e-111">Ejemplos desusados u obsoletos</span><span class="sxs-lookup"><span data-stu-id="f532e-111">Deprecated or Obsolete Samples</span></span>](#deprecated-or-obsolete-samples)
-   [<span data-ttu-id="f532e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f532e-112">Related topics</span></span>](#related-topics)

## <a name="encoding-samples"></a><span data-ttu-id="f532e-113">Ejemplos de codificación</span><span class="sxs-lookup"><span data-stu-id="f532e-113">Encoding Samples</span></span>



| <span data-ttu-id="f532e-114">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-114">Sample</span></span>                            | <span data-ttu-id="f532e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-115">Description</span></span>                                                 |
|-----------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="f532e-116">Transcodificar</span><span class="sxs-lookup"><span data-stu-id="f532e-116">Transcode</span></span>](transcode-sample.md) | <span data-ttu-id="f532e-117">Muestra cómo recodificar un archivo multimedia en el formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f532e-117">Shows how to reencode a media file to Windows Media format.</span></span> |



 

## <a name="playback-samples"></a><span data-ttu-id="f532e-118">Ejemplos de reproducción</span><span class="sxs-lookup"><span data-stu-id="f532e-118">Playback Samples</span></span>



| <span data-ttu-id="f532e-119">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-119">Sample</span></span>                                            | <span data-ttu-id="f532e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-120">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f532e-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f532e-121">[BasicPlayback](/previous-versions//bb970475(v=vs.85))</span></span>          | <span data-ttu-id="f532e-122">Reproduce archivos de audio y vídeo mediante la [sesión multimedia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f532e-122">Plays audio and video files by using the [Media Session](media-session.md).</span></span> <span data-ttu-id="f532e-123">Este ejemplo muestra cómo crear topologías de reproducción, controlar la sesión multimedia y recibir eventos de sesión durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="f532e-123">This sample demonstrates how to create playback topologies, control the Media Session, and receive session events during playback.</span></span> |
| <span data-ttu-id="f532e-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f532e-124">[MFPlayer](/previous-versions//bb970516(v=vs.85))</span></span>                    | <span data-ttu-id="f532e-125">Muestra algunas funciones de reproducción que no se incluyen en el ejemplo [BasicPlayback](/previous-versions//bb970475(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f532e-125">Demonstrates some playback functions that are not included in the [BasicPlayback](/previous-versions//bb970475(v=vs.85)) sample.</span></span>                                                                                              |
| [<span data-ttu-id="f532e-126">ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="f532e-126">ProtectedPlayback</span></span>](protectedplayback-sample.md) | <span data-ttu-id="f532e-127">Reproduce archivos de audio y vídeo protegidos.</span><span class="sxs-lookup"><span data-stu-id="f532e-127">Plays protected audio and video files.</span></span> <span data-ttu-id="f532e-128">En este ejemplo se muestra cómo usar la sesión de la ruta de acceso a medios protegidos (PMP) y cómo usar objetos de habilitador de contenido.</span><span class="sxs-lookup"><span data-stu-id="f532e-128">This sample shows how to use the protected media path (PMP) session and how to use content enabler objects.</span></span>                                                              |



 

## <a name="plug-ins"></a><span data-ttu-id="f532e-129">Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="f532e-129">Plug-Ins</span></span>



| <span data-ttu-id="f532e-130">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-130">Sample</span></span>                                       | <span data-ttu-id="f532e-131">Sub-Area</span><span class="sxs-lookup"><span data-stu-id="f532e-131">Sub-Area</span></span>                         | <span data-ttu-id="f532e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-132">Description</span></span>                                                                                            |
|----------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f532e-133">Descodificador</span><span class="sxs-lookup"><span data-stu-id="f532e-133">Decoder</span></span>](decoder-sample.md)                | <span data-ttu-id="f532e-134">Media Foundation Transform (MFT)</span><span class="sxs-lookup"><span data-stu-id="f532e-134">Media Foundation transform (MFT)</span></span> | <span data-ttu-id="f532e-135">Descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f532e-135">Video decoder.</span></span>                                                                                         |
| [<span data-ttu-id="f532e-136">EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="f532e-136">EVRPresenter</span></span>](evrpresenter-sample.md)      | <span data-ttu-id="f532e-137">Varios</span><span class="sxs-lookup"><span data-stu-id="f532e-137">Miscellaneous</span></span>                    | <span data-ttu-id="f532e-138">Presentador personalizado para el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="f532e-138">Custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span>                 |
| [<span data-ttu-id="f532e-139">AudioDelay de MFT \_</span><span class="sxs-lookup"><span data-stu-id="f532e-139">MFT\_AudioDelay</span></span>](mft-audiodelay-sample.md) | <span data-ttu-id="f532e-140">MAESTRA</span><span class="sxs-lookup"><span data-stu-id="f532e-140">MFT</span></span>                              | <span data-ttu-id="f532e-141">Transformación de efecto de audio.</span><span class="sxs-lookup"><span data-stu-id="f532e-141">Audio effect transform.</span></span> <span data-ttu-id="f532e-142">Muestra cómo escribir una MFT básica para el procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="f532e-142">Shows how to write a basic MFT for audio processing.</span></span>                           |
| [<span data-ttu-id="f532e-143">\_Escala de grises de MFT</span><span class="sxs-lookup"><span data-stu-id="f532e-143">MFT\_Grayscale</span></span>](mft-grayscale-sample.md)   | <span data-ttu-id="f532e-144">MAESTRA</span><span class="sxs-lookup"><span data-stu-id="f532e-144">MFT</span></span>                              | <span data-ttu-id="f532e-145">Efecto de vídeo de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="f532e-145">Grayscale video effect.</span></span> <span data-ttu-id="f532e-146">Muestra cómo escribir una MFT básica para el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f532e-146">Shows how to write a basic MFT for video processing.</span></span>                           |
| [<span data-ttu-id="f532e-147">MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="f532e-147">MPEG1Source</span></span>](mpeg1source-sample.md)        | <span data-ttu-id="f532e-148">Origen de medios</span><span class="sxs-lookup"><span data-stu-id="f532e-148">Media source</span></span>                     | <span data-ttu-id="f532e-149">Analiza los flujos de capas de sistemas MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f532e-149">Parses MPEG-1 systems-layer streams.</span></span> <span data-ttu-id="f532e-150">Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f532e-150">Shows how to write a custom media source and byte-stream handler.</span></span> |
| [<span data-ttu-id="f532e-151">WavSink</span><span class="sxs-lookup"><span data-stu-id="f532e-151">WavSink</span></span>](wavsink-sample.md)                | <span data-ttu-id="f532e-152">Receptor de medios</span><span class="sxs-lookup"><span data-stu-id="f532e-152">Media sink</span></span>                       | <span data-ttu-id="f532e-153">Un receptor de archivo que escribe archivos. wav.</span><span class="sxs-lookup"><span data-stu-id="f532e-153">An archive sink that writes .wav files.</span></span> <span data-ttu-id="f532e-154">Muestra cómo escribir un receptor de multimedia personalizado.</span><span class="sxs-lookup"><span data-stu-id="f532e-154">Shows how to write a custom media sink.</span></span>                        |
| [<span data-ttu-id="f532e-155">WavSource</span><span class="sxs-lookup"><span data-stu-id="f532e-155">WavSource</span></span>](wavsource-sample.md)            | <span data-ttu-id="f532e-156">Origen de medios</span><span class="sxs-lookup"><span data-stu-id="f532e-156">Media source</span></span>                     | <span data-ttu-id="f532e-157">Analiza los archivos. wav.</span><span class="sxs-lookup"><span data-stu-id="f532e-157">Parses .wav files.</span></span> <span data-ttu-id="f532e-158">Muestra cómo escribir un origen multimedia personalizado y un controlador de flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="f532e-158">Shows how to write a custom media source and byte-stream handler.</span></span>                   |



 

## <a name="source-reader-samples"></a><span data-ttu-id="f532e-159">Ejemplos de lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="f532e-159">Source Reader Samples</span></span>



| <span data-ttu-id="f532e-160">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-160">Sample</span></span>                                      | <span data-ttu-id="f532e-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-161">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f532e-162">Clip de audio</span><span class="sxs-lookup"><span data-stu-id="f532e-162">Audio Clip</span></span>](audio-clip-sample.md)         | <span data-ttu-id="f532e-163">Utiliza el [lector de origen](source-reader.md) para descodificar el audio de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="f532e-163">Uses the [Source Reader](source-reader.md) to decode audio from a media file.</span></span>      |
| [<span data-ttu-id="f532e-164">Videominiatura</span><span class="sxs-lookup"><span data-stu-id="f532e-164">VideoThumbnail</span></span>](videothumbnail-sample.md) | <span data-ttu-id="f532e-165">Utiliza el [lector de origen](source-reader.md) para obtener fotogramas individuales de un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f532e-165">Uses the [Source Reader](source-reader.md) to get single frames from a video file.</span></span> |



 

## <a name="video-capture"></a><span data-ttu-id="f532e-166">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f532e-166">Video Capture</span></span>



| <span data-ttu-id="f532e-167">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-167">Sample</span></span>                                        | <span data-ttu-id="f532e-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-168">Description</span></span>                                                                                 |
|-----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f532e-169">MFCaptureD3D</span><span class="sxs-lookup"><span data-stu-id="f532e-169">MFCaptureD3D</span></span>](mfcaptured3d-sample.md)       | <span data-ttu-id="f532e-170">Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo, usando Direct3D para representar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="f532e-170">Shows how to preview video from a video capture device, using Direct3D to render the video.</span></span> |
| [<span data-ttu-id="f532e-171">MFCaptureToFile</span><span class="sxs-lookup"><span data-stu-id="f532e-171">MFCaptureToFile</span></span>](mfcapturetofile-sample.md) | <span data-ttu-id="f532e-172">Muestra cómo capturar vídeo de una cámara de vídeo a un archivo.</span><span class="sxs-lookup"><span data-stu-id="f532e-172">Shows how to capture video from a video camera to a file.</span></span>                                   |



 

## <a name="miscellaneous-samples"></a><span data-ttu-id="f532e-173">Varios ejemplos</span><span class="sxs-lookup"><span data-stu-id="f532e-173">Miscellaneous Samples</span></span>



| <span data-ttu-id="f532e-174">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-174">Sample</span></span>                                         | <span data-ttu-id="f532e-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-175">Description</span></span>                                                                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f532e-176">ASFParser</span><span class="sxs-lookup"><span data-stu-id="f532e-176">ASFParser</span></span>](asfparser-sample.md)              | <span data-ttu-id="f532e-177">Muestra cómo analizar los datos de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="f532e-177">Shows how to parse data from an Advanced Systems Format (ASF) file.</span></span>                                                                                   |
| [<span data-ttu-id="f532e-178">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="f532e-178">DXVA-HD</span></span>](dxva-hd-sample.md)                  | <span data-ttu-id="f532e-179">Muestra cómo usar Microsoft DirectX video Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="f532e-179">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>                                                                      |
| [<span data-ttu-id="f532e-180">Videoproc DXVA2 \_</span><span class="sxs-lookup"><span data-stu-id="f532e-180">DXVA2\_VideoProc</span></span>](dxva2-videoproc-sample.md) | <span data-ttu-id="f532e-181">Usa la aceleración de vídeo de DirectX (DXVA) 2,0 para crear un flujo de vídeo 4:2:2 YUV.</span><span class="sxs-lookup"><span data-stu-id="f532e-181">Uses DirectX Video Acceleration (DXVA) 2.0 to create a stream of 4:2:2 YUV video.</span></span> <span data-ttu-id="f532e-182">En este ejemplo se muestra cómo usar las características de procesamiento de vídeo de DXVA.</span><span class="sxs-lookup"><span data-stu-id="f532e-182">This sample shows how to use the video processing features of DXVA.</span></span> |



 

## <a name="deprecated-or-obsolete-samples"></a><span data-ttu-id="f532e-183">Ejemplos desusados u obsoletos</span><span class="sxs-lookup"><span data-stu-id="f532e-183">Deprecated or Obsolete Samples</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f532e-184">Muestra</span><span class="sxs-lookup"><span data-stu-id="f532e-184">Sample</span></span></th>
<th><span data-ttu-id="f532e-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="f532e-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f532e-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span><span class="sxs-lookup"><span data-stu-id="f532e-186"><a href="mfplayer2-sample.md">MFPlayer2</a></span></span></td>
<td><span data-ttu-id="f532e-187">Muestra algunas características de reproducción avanzada de la API de <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> .</span><span class="sxs-lookup"><span data-stu-id="f532e-187">Demonstrates some advanced playback features of the <a href="using-mfplay-for-audio-video-playback.md">MFPlay</a> API.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f532e-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span><span class="sxs-lookup"><span data-stu-id="f532e-188"><a href="/previous-versions//bb970336(v=vs.85)">PlaybackFX</a></span></span></td>
<td><span data-ttu-id="f532e-189">Aplica un efecto de escala de grises a un vídeo.</span><span class="sxs-lookup"><span data-stu-id="f532e-189">Applies a grayscale effect to video.</span></span> <span data-ttu-id="f532e-190">Muestra cómo insertar MFTs en una topología de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f532e-190">Shows how to insert MFTs into a playback topology.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f532e-191">Este ejemplo ya no se incluye en el SDK de.</span><span class="sxs-lookup"><span data-stu-id="f532e-191">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f532e-192"><a href="playlist-sample.md">Lista de reproducción</a></span><span class="sxs-lookup"><span data-stu-id="f532e-192"><a href="playlist-sample.md">Playlist</a></span></span></td>
<td><span data-ttu-id="f532e-193">Reproduce una secuencia de archivos de audio mediante el origen del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="f532e-193">Plays a sequence of audio files using the sequencer source.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f532e-194">Este ejemplo ya no se incluye en el SDK de.</span><span class="sxs-lookup"><span data-stu-id="f532e-194">This sample is no longer included in the SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f532e-195"><a href="simplecapture-sample.md">SimpleCapture</a></span><span class="sxs-lookup"><span data-stu-id="f532e-195"><a href="simplecapture-sample.md">SimpleCapture</a></span></span></td>
<td><span data-ttu-id="f532e-196">Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo mediante la API de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f532e-196">Shows how to preview video from a video capture device, using the MFPlay API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f532e-197"><a href="simpleplay-sample.md">SimplePlay</a></span><span class="sxs-lookup"><span data-stu-id="f532e-197"><a href="simpleplay-sample.md">SimplePlay</a></span></span></td>
<td><span data-ttu-id="f532e-198">Muestra cómo reproducir un archivo multimedia mediante la API de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="f532e-198">Shows how to play a media file using the MFPlay API.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f532e-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f532e-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f532e-200">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f532e-200">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="f532e-201">Acerca de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f532e-201">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 
