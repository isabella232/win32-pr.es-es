---
description: Filtro de multiplexor DV
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro de multiplexor DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806698"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="6ce0d-103">Filtro de multiplexor DV</span><span class="sxs-lookup"><span data-stu-id="6ce0d-103">DV Muxer Filter</span></span>

<span data-ttu-id="6ce0d-104">Este filtro combina una secuencia de vídeo codificada en vídeo digital (DV) con uno o dos flujos de audio para producir una secuencia DV intercalada.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="6ce0d-105">Para escribir el flujo en un archivo AVI, conecte este filtro al filtro de [AVI-MUX](avi-mux-filter.md) y conecte el filtro de escritura de *AVI* al filtro del escritor de [archivos](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6ce0d-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="6ce0d-106">Para obtener más información, vea [vídeo digital en DirectShow](digital-video-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="6ce0d-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce0d-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="6ce0d-107">Filter Interfaces</span></span>                        | <span data-ttu-id="6ce0d-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="6ce0d-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="6ce0d-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="6ce0d-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="6ce0d-110">**Vídeo**: mediatype \_ vídeo, MEDIASUBTYPE \_ DVSD, formato \_ videoinfo **audio**: mediatype \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="6ce0d-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="6ce0d-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="6ce0d-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6ce0d-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6ce0d-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="6ce0d-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="6ce0d-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="6ce0d-114">MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, format \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="6ce0d-115">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="6ce0d-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6ce0d-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6ce0d-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="6ce0d-117">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="6ce0d-117">Filter CLSID</span></span>                             | <span data-ttu-id="6ce0d-118">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="6ce0d-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="6ce0d-119">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="6ce0d-119">Property Page CLSID</span></span>                      | <span data-ttu-id="6ce0d-120">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="6ce0d-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="6ce0d-121">Executable</span><span class="sxs-lookup"><span data-stu-id="6ce0d-121">Executable</span></span>                               | <span data-ttu-id="6ce0d-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="6ce0d-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="6ce0d-123">Fundament</span><span class="sxs-lookup"><span data-stu-id="6ce0d-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="6ce0d-124">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="6ce0d-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="6ce0d-125">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="6ce0d-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6ce0d-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6ce0d-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="6ce0d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ce0d-127">Remarks</span></span>

<span data-ttu-id="6ce0d-128">La multiplexor DV puede crear dos clavijas de entrada de audio.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="6ce0d-129">Admite los formatos de audio que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="6ce0d-130">PIN de audio 1</span><span class="sxs-lookup"><span data-stu-id="6ce0d-130">Audio Pin 1</span></span>

<span data-ttu-id="6ce0d-131">PIN de audio 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-131">Audio Pin 2</span></span>

<span data-ttu-id="6ce0d-132">Formato de salida</span><span class="sxs-lookup"><span data-stu-id="6ce0d-132">Output Format</span></span>

<span data-ttu-id="6ce0d-133">Frecuencia de muestreo (kHz)</span><span class="sxs-lookup"><span data-stu-id="6ce0d-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="6ce0d-134">Bits/ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-134">Bits/Sample</span></span>

<span data-ttu-id="6ce0d-135">Canales</span><span class="sxs-lookup"><span data-stu-id="6ce0d-135">Channels</span></span>

<span data-ttu-id="6ce0d-136">Velocidad de muestreo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-136">Sample Rate</span></span>

<span data-ttu-id="6ce0d-137">Bits/ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-137">Bits/Sample</span></span>

<span data-ttu-id="6ce0d-138">Canales</span><span class="sxs-lookup"><span data-stu-id="6ce0d-138">Channels</span></span>

<span data-ttu-id="6ce0d-139">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-139">32</span></span>

<span data-ttu-id="6ce0d-140">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-140">16</span></span>

<span data-ttu-id="6ce0d-141">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-141">Mono</span></span>

<span data-ttu-id="6ce0d-142">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-142">Unconnected</span></span>

<span data-ttu-id="6ce0d-143">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-143">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-144">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-144">32</span></span>

<span data-ttu-id="6ce0d-145">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-145">16</span></span>

<span data-ttu-id="6ce0d-146">Estéreo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-146">Stereo</span></span>

<span data-ttu-id="6ce0d-147">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-147">Unconnected</span></span>

<span data-ttu-id="6ce0d-148">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="6ce0d-148">SD 4 Channel</span></span>

<span data-ttu-id="6ce0d-149">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="6ce0d-149">44.1 or 48</span></span>

<span data-ttu-id="6ce0d-150">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-150">16</span></span>

<span data-ttu-id="6ce0d-151">Estéreo o mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-151">Stereo or Mono</span></span>

<span data-ttu-id="6ce0d-152">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-152">Unconnected</span></span>

<span data-ttu-id="6ce0d-153">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-153">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-154">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-154">Unconnected</span></span>

<span data-ttu-id="6ce0d-155">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-155">32</span></span>

<span data-ttu-id="6ce0d-156">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-156">16</span></span>

<span data-ttu-id="6ce0d-157">Estéreo o mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-157">Stereo or Mono</span></span>

<span data-ttu-id="6ce0d-158">No permitida.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-158">Disallowed</span></span>

<span data-ttu-id="6ce0d-159">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-159">Unconnected</span></span>

<span data-ttu-id="6ce0d-160">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="6ce0d-160">44.1 or 48</span></span>

<span data-ttu-id="6ce0d-161">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-161">16</span></span>

<span data-ttu-id="6ce0d-162">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-162">Mono</span></span>

<span data-ttu-id="6ce0d-163">No permitida.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-163">Disallowed</span></span>

<span data-ttu-id="6ce0d-164">No conectado</span><span class="sxs-lookup"><span data-stu-id="6ce0d-164">Unconnected</span></span>

<span data-ttu-id="6ce0d-165">44,1 o 48</span><span class="sxs-lookup"><span data-stu-id="6ce0d-165">44.1 or 48</span></span>

<span data-ttu-id="6ce0d-166">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-166">16</span></span>

<span data-ttu-id="6ce0d-167">Estéreo</span><span class="sxs-lookup"><span data-stu-id="6ce0d-167">Stereo</span></span>

<span data-ttu-id="6ce0d-168">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-168">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-169">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-169">32</span></span>

<span data-ttu-id="6ce0d-170">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-170">16</span></span>

<span data-ttu-id="6ce0d-171">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-171">Mono</span></span>

<span data-ttu-id="6ce0d-172">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-172">32</span></span>

<span data-ttu-id="6ce0d-173">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-173">16</span></span>

<span data-ttu-id="6ce0d-174">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-174">Mono</span></span>

<span data-ttu-id="6ce0d-175">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-175">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-176">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-176">32</span></span>

<span data-ttu-id="6ce0d-177">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-177">16</span></span>

<span data-ttu-id="6ce0d-178">Estéreo o mono\*</span><span class="sxs-lookup"><span data-stu-id="6ce0d-178">Stereo or Mono\*</span></span>

<span data-ttu-id="6ce0d-179">32</span><span class="sxs-lookup"><span data-stu-id="6ce0d-179">32</span></span>

<span data-ttu-id="6ce0d-180">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-180">16</span></span>

<span data-ttu-id="6ce0d-181">Estéreo o mono\*</span><span class="sxs-lookup"><span data-stu-id="6ce0d-181">Stereo or Mono\*</span></span>

<span data-ttu-id="6ce0d-182">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="6ce0d-182">SD 4 Channel</span></span>

<span data-ttu-id="6ce0d-183">44,1</span><span class="sxs-lookup"><span data-stu-id="6ce0d-183">44.1</span></span>

<span data-ttu-id="6ce0d-184">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-184">16</span></span>

<span data-ttu-id="6ce0d-185">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-185">Mono</span></span>

<span data-ttu-id="6ce0d-186">44,1</span><span class="sxs-lookup"><span data-stu-id="6ce0d-186">44.1</span></span>

<span data-ttu-id="6ce0d-187">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-187">16</span></span>

<span data-ttu-id="6ce0d-188">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-188">Mono</span></span>

<span data-ttu-id="6ce0d-189">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-189">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-190">48</span><span class="sxs-lookup"><span data-stu-id="6ce0d-190">48</span></span>

<span data-ttu-id="6ce0d-191">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-191">16</span></span>

<span data-ttu-id="6ce0d-192">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-192">Mono</span></span>

<span data-ttu-id="6ce0d-193">48</span><span class="sxs-lookup"><span data-stu-id="6ce0d-193">48</span></span>

<span data-ttu-id="6ce0d-194">16</span><span class="sxs-lookup"><span data-stu-id="6ce0d-194">16</span></span>

<span data-ttu-id="6ce0d-195">Mono</span><span class="sxs-lookup"><span data-stu-id="6ce0d-195">Mono</span></span>

<span data-ttu-id="6ce0d-196">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="6ce0d-196">SD 2 Channel</span></span>

<span data-ttu-id="6ce0d-197">\* Si al menos un PIN de entrada es estéreo.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="6ce0d-198">En esta tabla, el PIN de audio 1 se define como el primer PIN de entrada conectado a una fuente de audio, y el PIN de audio 2 se define como el segundo PIN de entrada conectado a un origen de audio.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="6ce0d-199">Una vez conectado un PIN de audio, este esquema de numeración permanece en vigor a menos que ambos pines de audio estén desconectados.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="6ce0d-200">Por ejemplo, si conecta ambos PIN de audio y, a continuación, desconecta el PIN de audio 1, el PIN restante todavía se considera pin 2.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="6ce0d-201">El audio proporcionado al pin 1 se graba en el primer bloque de audio de los fotogramas DV (CH1), y el audio proporcionado al pin 2 se graba en el segundo bloque de audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="6ce0d-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="6ce0d-202">Excepción: Si el filtro tiene una sola entrada estéreo a 44,1 kHz o 48 kHz, el canal de audio izquierdo se graba en el primer bloque de audio y el canal de audio derecho se graba en el segundo bloque de audio.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="6ce0d-203">Para la salida de canal SD 4: Si la entrada es estéreo, la pista de la izquierda se registra en CHa o CHc y la pista adecuada se registra en CHb o CHd.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="6ce0d-204">Si la entrada es mono, el audio se graba en CHa o CHc, y CHb y CHd son silenciosos.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="6ce0d-205">Al conectar y desconectar el PIN de audio 1, es posible llegar a un formato no permitido.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="6ce0d-206">En ese caso, el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro devuelve VFW \_ E \_ not \_ connected.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="6ce0d-207">Esta limitación evita una situación en la que el primer bloque de audio no tiene audio, pero el segundo bloque de audio tiene audio.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="6ce0d-208">El segundo bloque solo debe tener audio si el primer bloque también tiene audio.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="6ce0d-209">La multiplexor DV no permite entradas de audio con diferentes velocidades de muestreo.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="6ce0d-210">Sin embargo, los métodos de creación de gráficos como [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) agregarán normalmente el filtro [contenedor ACM](acm-wrapper-filter.md) , que convertirá la segunda secuencia de audio para que coincida con la velocidad de muestreo de la primera secuencia.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="6ce0d-211">Si la entrada de audio es 48 kHz o 32 kHz, la salida de audio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="6ce0d-212">(No es posible bloquear audio de 44,1 kHz).</span><span class="sxs-lookup"><span data-stu-id="6ce0d-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="6ce0d-213">Si no hay ningún PIN de audio conectado, la salida contiene los datos de audio de los fotogramas DV entrantes.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="6ce0d-214">Esto podría ser el silencio o los datos de audio válidos.</span><span class="sxs-lookup"><span data-stu-id="6ce0d-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce0d-215">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ce0d-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce0d-216">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6ce0d-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="6ce0d-217">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="6ce0d-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



