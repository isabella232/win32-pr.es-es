---
description: Tipos de medios divisores MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de medios divisores MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909433"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="ed9c1-103">Tipos de medios divisores MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ed9c1-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="ed9c1-104">El [filtro divisor MPEG-2](mpeg-2-splitter.md) admite actualmente audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="ed9c1-105">Dolby AC-3 se admite como una subtransmisión, tal y como se define en DVD.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="ed9c1-106">El filtro también admite audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="ed9c1-107">Los tipos de medios dependen de si el divisor MPEG-2 está entregando paquetes PES o cargas PES.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="ed9c1-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="ed9c1-108">Video</span></span>

<span data-ttu-id="ed9c1-109">En el caso del vídeo MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="ed9c1-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="ed9c1-110">Label</span></span> | <span data-ttu-id="ed9c1-111">Value</span><span class="sxs-lookup"><span data-stu-id="ed9c1-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="ed9c1-112">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="ed9c1-112">PES output</span></span>                               | <span data-ttu-id="ed9c1-113">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="ed9c1-113">Payload output</span></span>                 |
| <span data-ttu-id="ed9c1-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ed9c1-114">Major Type</span></span>       | <span data-ttu-id="ed9c1-115">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="ed9c1-116">**Vídeo \_ DE MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="ed9c1-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="ed9c1-117">Subtype</span></span>          | <span data-ttu-id="ed9c1-118">**VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="ed9c1-119">**VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="ed9c1-120">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-120">Format Type</span></span>      | <span data-ttu-id="ed9c1-121">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="ed9c1-122">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="ed9c1-123">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-123">Format Structure</span></span> | [<span data-ttu-id="ed9c1-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="ed9c1-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="ed9c1-126">AC-3 Audio</span><span class="sxs-lookup"><span data-stu-id="ed9c1-126">AC-3 Audio</span></span>

<span data-ttu-id="ed9c1-127">Para el audio AC-3, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="ed9c1-128">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="ed9c1-128">Label</span></span> | <span data-ttu-id="ed9c1-129">Value</span><span class="sxs-lookup"><span data-stu-id="ed9c1-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="ed9c1-130">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="ed9c1-130">PES output</span></span>                           | <span data-ttu-id="ed9c1-131">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="ed9c1-131">Payload output</span></span>               |
| <span data-ttu-id="ed9c1-132">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ed9c1-132">Major Type</span></span>       | <span data-ttu-id="ed9c1-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="ed9c1-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="ed9c1-134">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="ed9c1-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="ed9c1-135">Subtype</span></span>          | <span data-ttu-id="ed9c1-136">MEDIASUBTYPE \_ DOLBY \_ AC3</span><span class="sxs-lookup"><span data-stu-id="ed9c1-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="ed9c1-137">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="ed9c1-138">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-138">Format Type</span></span>      | <span data-ttu-id="ed9c1-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="ed9c1-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="ed9c1-140">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="ed9c1-141">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-141">Format Structure</span></span> | <span data-ttu-id="ed9c1-142">[**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed9c1-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="ed9c1-143">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="ed9c1-144">El miembro **wFormatTag** de la estructura **DEFORMATEX** para AC-3 es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="ed9c1-145">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="ed9c1-145">MPEG-2 Audio</span></span>

<span data-ttu-id="ed9c1-146">En el caso del audio MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="ed9c1-147">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="ed9c1-147">Label</span></span> | <span data-ttu-id="ed9c1-148">Value</span><span class="sxs-lookup"><span data-stu-id="ed9c1-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="ed9c1-149">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="ed9c1-149">PES output</span></span>                    | <span data-ttu-id="ed9c1-150">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="ed9c1-150">Payload output</span></span>                 |
| <span data-ttu-id="ed9c1-151">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ed9c1-151">Major Type</span></span>       | <span data-ttu-id="ed9c1-152">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="ed9c1-153">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="ed9c1-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="ed9c1-154">Subtype</span></span>          | <span data-ttu-id="ed9c1-155">**AUDIO MPEG2 DE MEDIASUBTYE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="ed9c1-156">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="ed9c1-157">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-157">Format Type</span></span>      | <span data-ttu-id="ed9c1-158">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="ed9c1-159">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="ed9c1-160">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-160">Format Structure</span></span> | <span data-ttu-id="ed9c1-161">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="ed9c1-162">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="ed9c1-163">El miembro **wFormatTag** de la estructura **WAVEATEX** para MPEG-2 Audio es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="ed9c1-164">El divisor MPEG-2 supone que las secuencias D0 a DF se usan para la secuencia de extensión multicanal, como para el audio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="ed9c1-165">Por lo tanto, cada vez que se selecciona la secuencia C *x,* el divisor reenvía también los paquetes para la secuencia D *x.*</span><span class="sxs-lookup"><span data-stu-id="ed9c1-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="ed9c1-166">LPCM Audio</span><span class="sxs-lookup"><span data-stu-id="ed9c1-166">LPCM Audio</span></span>

<span data-ttu-id="ed9c1-167">En el caso del audio LPCM, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="ed9c1-168">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="ed9c1-168">Label</span></span> | <span data-ttu-id="ed9c1-169">Value</span><span class="sxs-lookup"><span data-stu-id="ed9c1-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="ed9c1-170">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="ed9c1-170">PES output</span></span>                         | <span data-ttu-id="ed9c1-171">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="ed9c1-171">Payload output</span></span>                     |
| <span data-ttu-id="ed9c1-172">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="ed9c1-172">Major Type</span></span>       | <span data-ttu-id="ed9c1-173">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="ed9c1-174">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="ed9c1-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="ed9c1-175">Subtype</span></span>          | <span data-ttu-id="ed9c1-176">**AUDIO \_ LPCM DE DVD DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="ed9c1-177">**AUDIO \_ LPCM DE DVD DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="ed9c1-178">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-178">Format Type</span></span>      | <span data-ttu-id="ed9c1-179">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="ed9c1-180">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="ed9c1-181">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="ed9c1-181">Format Structure</span></span> | <span data-ttu-id="ed9c1-182">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="ed9c1-183">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="ed9c1-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="ed9c1-184">El miembro **wFormatTag** de la estructura **WAVEATEX** para el audio LPCM es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="ed9c1-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed9c1-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed9c1-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed9c1-186">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ed9c1-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
