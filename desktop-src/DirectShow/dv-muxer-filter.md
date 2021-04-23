---
description: DV Muxer Filter
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908603"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="d703b-103">DV Muxer Filter</span><span class="sxs-lookup"><span data-stu-id="d703b-103">DV Muxer Filter</span></span>

<span data-ttu-id="d703b-104">Este filtro combina una secuencia de vídeo digital (DV) codificada con una o dos secuencias de audio para generar una secuencia DV intercalada.</span><span class="sxs-lookup"><span data-stu-id="d703b-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="d703b-105">Para escribir la secuencia en un archivo AVI, conecte este filtro al filtro [AVI Mux](avi-mux-filter.md) y conecte avi *Mux* al filtro [File Writer.](file-writer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d703b-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="d703b-106">Para obtener más información, vea [Vídeo digital en DirectShow.](digital-video-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="d703b-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="d703b-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="d703b-107">Label</span></span> | <span data-ttu-id="d703b-108">Value</span><span class="sxs-lookup"><span data-stu-id="d703b-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d703b-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="d703b-109">Filter Interfaces</span></span>                        | <span data-ttu-id="d703b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="d703b-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="d703b-111">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="d703b-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="d703b-112">**Vídeo:** MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio**: MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="d703b-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="d703b-113">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="d703b-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d703b-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d703b-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="d703b-115">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="d703b-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="d703b-116">MEDIATYPE \_ Intercalado, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="d703b-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="d703b-117">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="d703b-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d703b-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d703b-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="d703b-119">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="d703b-119">Filter CLSID</span></span>                             | <span data-ttu-id="d703b-120">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="d703b-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="d703b-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="d703b-121">Property Page CLSID</span></span>                      | <span data-ttu-id="d703b-122">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="d703b-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="d703b-123">Executable</span><span class="sxs-lookup"><span data-stu-id="d703b-123">Executable</span></span>                               | <span data-ttu-id="d703b-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="d703b-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="d703b-125">Mérito</span><span class="sxs-lookup"><span data-stu-id="d703b-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="d703b-126">NO ES \_ PROBABLE QUE SE PRODUZCA UN GRAN</span><span class="sxs-lookup"><span data-stu-id="d703b-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="d703b-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="d703b-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d703b-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="d703b-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d703b-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d703b-129">Remarks</span></span>

<span data-ttu-id="d703b-130">Dv Muxer puede crear dos pines de entrada de audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="d703b-131">Admite los formatos de audio que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d703b-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="d703b-132">Patilla de audio 1</span><span class="sxs-lookup"><span data-stu-id="d703b-132">Audio Pin 1</span></span>

<span data-ttu-id="d703b-133">Patilla de audio 2</span><span class="sxs-lookup"><span data-stu-id="d703b-133">Audio Pin 2</span></span>

<span data-ttu-id="d703b-134">Formato de salida</span><span class="sxs-lookup"><span data-stu-id="d703b-134">Output Format</span></span>

<span data-ttu-id="d703b-135">Frecuencia de muestreo (kHz)</span><span class="sxs-lookup"><span data-stu-id="d703b-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="d703b-136">Bits/ejemplo</span><span class="sxs-lookup"><span data-stu-id="d703b-136">Bits/Sample</span></span>

<span data-ttu-id="d703b-137">Canales</span><span class="sxs-lookup"><span data-stu-id="d703b-137">Channels</span></span>

<span data-ttu-id="d703b-138">Velocidad de muestreo</span><span class="sxs-lookup"><span data-stu-id="d703b-138">Sample Rate</span></span>

<span data-ttu-id="d703b-139">Bits/ejemplo</span><span class="sxs-lookup"><span data-stu-id="d703b-139">Bits/Sample</span></span>

<span data-ttu-id="d703b-140">Canales</span><span class="sxs-lookup"><span data-stu-id="d703b-140">Channels</span></span>

<span data-ttu-id="d703b-141">32</span><span class="sxs-lookup"><span data-stu-id="d703b-141">32</span></span>

<span data-ttu-id="d703b-142">16</span><span class="sxs-lookup"><span data-stu-id="d703b-142">16</span></span>

<span data-ttu-id="d703b-143">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-143">Mono</span></span>

<span data-ttu-id="d703b-144">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-144">Unconnected</span></span>

<span data-ttu-id="d703b-145">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-145">SD 2 Channel</span></span>

<span data-ttu-id="d703b-146">32</span><span class="sxs-lookup"><span data-stu-id="d703b-146">32</span></span>

<span data-ttu-id="d703b-147">16</span><span class="sxs-lookup"><span data-stu-id="d703b-147">16</span></span>

<span data-ttu-id="d703b-148">Estéreo</span><span class="sxs-lookup"><span data-stu-id="d703b-148">Stereo</span></span>

<span data-ttu-id="d703b-149">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-149">Unconnected</span></span>

<span data-ttu-id="d703b-150">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="d703b-150">SD 4 Channel</span></span>

<span data-ttu-id="d703b-151">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="d703b-151">44.1 or 48</span></span>

<span data-ttu-id="d703b-152">16</span><span class="sxs-lookup"><span data-stu-id="d703b-152">16</span></span>

<span data-ttu-id="d703b-153">Estéreo o Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-153">Stereo or Mono</span></span>

<span data-ttu-id="d703b-154">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-154">Unconnected</span></span>

<span data-ttu-id="d703b-155">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-155">SD 2 Channel</span></span>

<span data-ttu-id="d703b-156">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-156">Unconnected</span></span>

<span data-ttu-id="d703b-157">32</span><span class="sxs-lookup"><span data-stu-id="d703b-157">32</span></span>

<span data-ttu-id="d703b-158">16</span><span class="sxs-lookup"><span data-stu-id="d703b-158">16</span></span>

<span data-ttu-id="d703b-159">Estéreo o Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-159">Stereo or Mono</span></span>

<span data-ttu-id="d703b-160">No permitida.</span><span class="sxs-lookup"><span data-stu-id="d703b-160">Disallowed</span></span>

<span data-ttu-id="d703b-161">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-161">Unconnected</span></span>

<span data-ttu-id="d703b-162">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="d703b-162">44.1 or 48</span></span>

<span data-ttu-id="d703b-163">16</span><span class="sxs-lookup"><span data-stu-id="d703b-163">16</span></span>

<span data-ttu-id="d703b-164">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-164">Mono</span></span>

<span data-ttu-id="d703b-165">No permitida.</span><span class="sxs-lookup"><span data-stu-id="d703b-165">Disallowed</span></span>

<span data-ttu-id="d703b-166">Desconectado</span><span class="sxs-lookup"><span data-stu-id="d703b-166">Unconnected</span></span>

<span data-ttu-id="d703b-167">44.1 o 48</span><span class="sxs-lookup"><span data-stu-id="d703b-167">44.1 or 48</span></span>

<span data-ttu-id="d703b-168">16</span><span class="sxs-lookup"><span data-stu-id="d703b-168">16</span></span>

<span data-ttu-id="d703b-169">Estéreo</span><span class="sxs-lookup"><span data-stu-id="d703b-169">Stereo</span></span>

<span data-ttu-id="d703b-170">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-170">SD 2 Channel</span></span>

<span data-ttu-id="d703b-171">32</span><span class="sxs-lookup"><span data-stu-id="d703b-171">32</span></span>

<span data-ttu-id="d703b-172">16</span><span class="sxs-lookup"><span data-stu-id="d703b-172">16</span></span>

<span data-ttu-id="d703b-173">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-173">Mono</span></span>

<span data-ttu-id="d703b-174">32</span><span class="sxs-lookup"><span data-stu-id="d703b-174">32</span></span>

<span data-ttu-id="d703b-175">16</span><span class="sxs-lookup"><span data-stu-id="d703b-175">16</span></span>

<span data-ttu-id="d703b-176">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-176">Mono</span></span>

<span data-ttu-id="d703b-177">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-177">SD 2 Channel</span></span>

<span data-ttu-id="d703b-178">32</span><span class="sxs-lookup"><span data-stu-id="d703b-178">32</span></span>

<span data-ttu-id="d703b-179">16</span><span class="sxs-lookup"><span data-stu-id="d703b-179">16</span></span>

<span data-ttu-id="d703b-180">Estéreo o Mono\*</span><span class="sxs-lookup"><span data-stu-id="d703b-180">Stereo or Mono\*</span></span>

<span data-ttu-id="d703b-181">32</span><span class="sxs-lookup"><span data-stu-id="d703b-181">32</span></span>

<span data-ttu-id="d703b-182">16</span><span class="sxs-lookup"><span data-stu-id="d703b-182">16</span></span>

<span data-ttu-id="d703b-183">Estéreo o Mono\*</span><span class="sxs-lookup"><span data-stu-id="d703b-183">Stereo or Mono\*</span></span>

<span data-ttu-id="d703b-184">Canal SD 4</span><span class="sxs-lookup"><span data-stu-id="d703b-184">SD 4 Channel</span></span>

<span data-ttu-id="d703b-185">44.1</span><span class="sxs-lookup"><span data-stu-id="d703b-185">44.1</span></span>

<span data-ttu-id="d703b-186">16</span><span class="sxs-lookup"><span data-stu-id="d703b-186">16</span></span>

<span data-ttu-id="d703b-187">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-187">Mono</span></span>

<span data-ttu-id="d703b-188">44.1</span><span class="sxs-lookup"><span data-stu-id="d703b-188">44.1</span></span>

<span data-ttu-id="d703b-189">16</span><span class="sxs-lookup"><span data-stu-id="d703b-189">16</span></span>

<span data-ttu-id="d703b-190">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-190">Mono</span></span>

<span data-ttu-id="d703b-191">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-191">SD 2 Channel</span></span>

<span data-ttu-id="d703b-192">48</span><span class="sxs-lookup"><span data-stu-id="d703b-192">48</span></span>

<span data-ttu-id="d703b-193">16</span><span class="sxs-lookup"><span data-stu-id="d703b-193">16</span></span>

<span data-ttu-id="d703b-194">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-194">Mono</span></span>

<span data-ttu-id="d703b-195">48</span><span class="sxs-lookup"><span data-stu-id="d703b-195">48</span></span>

<span data-ttu-id="d703b-196">16</span><span class="sxs-lookup"><span data-stu-id="d703b-196">16</span></span>

<span data-ttu-id="d703b-197">Mono</span><span class="sxs-lookup"><span data-stu-id="d703b-197">Mono</span></span>

<span data-ttu-id="d703b-198">Canal SD 2</span><span class="sxs-lookup"><span data-stu-id="d703b-198">SD 2 Channel</span></span>

<span data-ttu-id="d703b-199">\* Si al menos un pin de entrada es estéreo.</span><span class="sxs-lookup"><span data-stu-id="d703b-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="d703b-200">Para esta tabla, el pin de audio 1 se define como el primer pin de entrada conectado a un origen de audio y el pin de audio 2 se define como el segundo pin de entrada conectado a un origen de audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="d703b-201">Una vez conectada una clavija de audio, este esquema de numeración permanece en vigor a menos que se desconecten ambas clavijas de audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="d703b-202">Por ejemplo, si conecta ambas clavijas de audio y, a continuación, desconecta el pin de audio 1, el pin restante todavía se considera el pin 2.</span><span class="sxs-lookup"><span data-stu-id="d703b-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="d703b-203">El audio proporcionado para anclar 1 se graba en el primer bloque de audio de los marcos DV (CH1) y el audio proporcionado para anclar 2 se graba en el segundo bloque de audio (CH2).</span><span class="sxs-lookup"><span data-stu-id="d703b-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="d703b-204">Excepción: si el filtro tiene una única entrada estéreo a 44,1 kHz o 48 kHz, el canal de audio izquierdo se graba en el primer bloque de audio y el canal de audio derecho se graba en el segundo bloque de audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="d703b-205">Para la salida sd de 4 canales: si la entrada es estéreo, la pista izquierda se registra en CHa o CHc y la pista derecha se registra en CHb o CHd.</span><span class="sxs-lookup"><span data-stu-id="d703b-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="d703b-206">Si la entrada es mono, el audio se graba en CHa o CHc, y CHb y CHd son silenciosos.</span><span class="sxs-lookup"><span data-stu-id="d703b-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="d703b-207">Al conectar y desconectar el pin de audio 1, es posible alcanzar un formato no permitido.</span><span class="sxs-lookup"><span data-stu-id="d703b-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="d703b-208">En ese caso, el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro devuelve VFW \_ E NOT \_ \_ CONNECTED.</span><span class="sxs-lookup"><span data-stu-id="d703b-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="d703b-209">Esta limitación evita una situación en la que el primer bloque de audio no tiene audio, pero el segundo bloque de audio sí tiene audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="d703b-210">El segundo bloque solo debe tener audio si el primer bloque también tiene audio.</span><span class="sxs-lookup"><span data-stu-id="d703b-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="d703b-211">Dv Muxer no permite entradas de audio con diferentes velocidades de muestreo.</span><span class="sxs-lookup"><span data-stu-id="d703b-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="d703b-212">Sin embargo, los métodos de creación de grafos como [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) normalmente agregarán el filtro contenedor [de ACM,](acm-wrapper-filter.md) que convertirá la segunda secuencia de audio para que coincida con la velocidad de muestreo de la primera secuencia.</span><span class="sxs-lookup"><span data-stu-id="d703b-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="d703b-213">Si la entrada de audio es de 48 kHz o 32 kHz, la salida de audio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="d703b-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="d703b-214">(No es posible bloquear el audio de 44,1 kHz).</span><span class="sxs-lookup"><span data-stu-id="d703b-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="d703b-215">Si no hay ningún pin de audio conectado, la salida contiene los datos de audio de los fotogramas DV entrantes.</span><span class="sxs-lookup"><span data-stu-id="d703b-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="d703b-216">Esto puede ser silencio o datos de audio válidos.</span><span class="sxs-lookup"><span data-stu-id="d703b-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d703b-217">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d703b-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d703b-218">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d703b-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d703b-219">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d703b-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



