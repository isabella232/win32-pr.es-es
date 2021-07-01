---
description: Tipos de medios divisores MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de medios divisores MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119980"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="4edac-103">Tipos de medios divisores MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4edac-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="4edac-104">El [filtro divisor MPEG-2](mpeg-2-splitter.md) admite actualmente audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="4edac-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="4edac-105">Dolby AC-3 se admite como una subtransmisión, tal y como se define en DVD.</span><span class="sxs-lookup"><span data-stu-id="4edac-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="4edac-106">El filtro también admite audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="4edac-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="4edac-107">Los tipos de medios dependen de si el divisor MPEG-2 entrega paquetes PES o cargas PES.</span><span class="sxs-lookup"><span data-stu-id="4edac-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="4edac-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="4edac-108">Video</span></span>

<span data-ttu-id="4edac-109">En el caso del vídeo MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4edac-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="4edac-110">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="4edac-110">PES output</span></span> | <span data-ttu-id="4edac-111">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="4edac-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="4edac-112">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="4edac-112">**Major type**</span></span>       | <span data-ttu-id="4edac-113">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="4edac-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="4edac-114">**Vídeo \_ DE MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="4edac-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="4edac-115">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="4edac-115">**Subtype**</span></span>          | <span data-ttu-id="4edac-116">**VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4edac-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="4edac-117">**VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4edac-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="4edac-118">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-118">**Format type**</span></span>      | <span data-ttu-id="4edac-119">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="4edac-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="4edac-120">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="4edac-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="4edac-121">**Estructura de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-121">**Format structure**</span></span> | [<span data-ttu-id="4edac-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="4edac-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="4edac-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="4edac-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="4edac-124">AC-3 Audio</span><span class="sxs-lookup"><span data-stu-id="4edac-124">AC-3 Audio</span></span>

<span data-ttu-id="4edac-125">Para el audio AC-3, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4edac-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="4edac-126">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="4edac-126">PES output</span></span> | <span data-ttu-id="4edac-127">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="4edac-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="4edac-128">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="4edac-128">**Major type**</span></span>       | <span data-ttu-id="4edac-129">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="4edac-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="4edac-130">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4edac-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="4edac-131">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="4edac-131">**Subtype**</span></span>          | <span data-ttu-id="4edac-132">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="4edac-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="4edac-133">**MEDIASUBTYPE \_ DOLBY \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="4edac-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="4edac-134">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-134">**Format type**</span></span>      | <span data-ttu-id="4edac-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="4edac-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="4edac-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4edac-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="4edac-137">**Estructura de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-137">**Format structure**</span></span> | <span data-ttu-id="4edac-138">[**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4edac-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="4edac-139">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="4edac-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="4edac-140">El miembro **wFormatTag** de la estructura **WAVEATEX** para AC-3 es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="4edac-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="4edac-141">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="4edac-141">MPEG-2 Audio</span></span>

<span data-ttu-id="4edac-142">En el caso del audio MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4edac-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="4edac-143">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="4edac-143">PES output</span></span> | <span data-ttu-id="4edac-144">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="4edac-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="4edac-145">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="4edac-145">**Major type**</span></span>       | <span data-ttu-id="4edac-146">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="4edac-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="4edac-147">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4edac-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="4edac-148">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="4edac-148">**Subtype**</span></span>          | <span data-ttu-id="4edac-149">**AUDIO MPEG2 DE MEDIASUBTYE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4edac-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="4edac-150">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="4edac-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="4edac-151">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-151">**Format type**</span></span>      | <span data-ttu-id="4edac-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4edac-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="4edac-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4edac-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="4edac-154">**Estructura de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-154">**Format structure**</span></span> | <span data-ttu-id="4edac-155">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="4edac-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="4edac-156">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="4edac-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="4edac-157">El miembro **wFormatTag** de la estructura **WAVEATEX** para MPEG-2 Audio es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="4edac-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="4edac-158">El divisor MPEG-2 supone que las secuencias D0 a DF se usan para la secuencia de extensión multicanal, como para el audio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="4edac-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="4edac-159">Por lo tanto, cada vez que se selecciona la secuencia C *x,* el divisor reenvía también los paquetes para la secuencia D *x.*</span><span class="sxs-lookup"><span data-stu-id="4edac-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="4edac-160">LPCM Audio</span><span class="sxs-lookup"><span data-stu-id="4edac-160">LPCM Audio</span></span>

<span data-ttu-id="4edac-161">En el caso del audio LPCM, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4edac-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="4edac-162">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="4edac-162">PES output</span></span> | <span data-ttu-id="4edac-163">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="4edac-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="4edac-164">**Tipo principal**</span><span class="sxs-lookup"><span data-stu-id="4edac-164">**Major type**</span></span>       | <span data-ttu-id="4edac-165">**MEDIATYPE \_ MPEG2 \_ PES**</span><span class="sxs-lookup"><span data-stu-id="4edac-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="4edac-166">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="4edac-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="4edac-167">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="4edac-167">**Subtype**</span></span>          | <span data-ttu-id="4edac-168">**AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4edac-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="4edac-169">**AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4edac-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="4edac-170">**Tipo de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-170">**Format type**</span></span>      | <span data-ttu-id="4edac-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4edac-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="4edac-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4edac-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="4edac-173">**Estructura de formato**</span><span class="sxs-lookup"><span data-stu-id="4edac-173">**Format structure**</span></span> | <span data-ttu-id="4edac-174">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="4edac-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="4edac-175">**FORMA DE ONDAATEX**</span><span class="sxs-lookup"><span data-stu-id="4edac-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="4edac-176">El miembro **wFormatTag** de la estructura **WAVEATEX** para el audio LPCM es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="4edac-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4edac-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4edac-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4edac-178">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4edac-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
