---
description: Tipos de medios de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de medios de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689638"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="e7746-103">Tipos de medios de divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e7746-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="e7746-104">El filtro [de divisores MPEG-2](mpeg-2-splitter.md) admite actualmente audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7746-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="e7746-105">Dolby AC-3 se admite como subflujo, tal y como se define en DVD.</span><span class="sxs-lookup"><span data-stu-id="e7746-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="e7746-106">El filtro también admite audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e7746-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="e7746-107">Los tipos de medios dependen de si el separador MPEG-2 está entregando paquetes PES o cargas de PES.</span><span class="sxs-lookup"><span data-stu-id="e7746-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="e7746-108">Vídeo</span><span class="sxs-lookup"><span data-stu-id="e7746-108">Video</span></span>

<span data-ttu-id="e7746-109">Para vídeo MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7746-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="e7746-110">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="e7746-110">PES output</span></span>                               | <span data-ttu-id="e7746-111">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="e7746-111">Payload output</span></span>                 |
| <span data-ttu-id="e7746-112">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="e7746-112">Major Type</span></span>       | <span data-ttu-id="e7746-113">**\_PES MPEG2 \_ PE**</span><span class="sxs-lookup"><span data-stu-id="e7746-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="e7746-114">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="e7746-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="e7746-115">Subtype</span></span>          | <span data-ttu-id="e7746-116">**\_Vídeo MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="e7746-117">**\_Vídeo MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="e7746-118">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-118">Format Type</span></span>      | <span data-ttu-id="e7746-119">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="e7746-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="e7746-120">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="e7746-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="e7746-121">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-121">Format Structure</span></span> | [<span data-ttu-id="e7746-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="e7746-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="e7746-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="e7746-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="e7746-124">Audio AC-3</span><span class="sxs-lookup"><span data-stu-id="e7746-124">AC-3 Audio</span></span>

<span data-ttu-id="e7746-125">En el caso de audio AC-3, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7746-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="e7746-126">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="e7746-126">PES output</span></span>                           | <span data-ttu-id="e7746-127">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="e7746-127">Payload output</span></span>               |
| <span data-ttu-id="e7746-128">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="e7746-128">Major Type</span></span>       | <span data-ttu-id="e7746-129">\_PES MPEG2 \_ PE</span><span class="sxs-lookup"><span data-stu-id="e7746-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="e7746-130">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="e7746-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="e7746-131">Subtype</span></span>          | <span data-ttu-id="e7746-132">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="e7746-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="e7746-133">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="e7746-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="e7746-134">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-134">Format Type</span></span>      | <span data-ttu-id="e7746-135">DAR formato a \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="e7746-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="e7746-136">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e7746-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="e7746-137">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-137">Format Structure</span></span> | <span data-ttu-id="e7746-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7746-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="e7746-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e7746-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="e7746-140">El miembro **wFormatTag** de la estructura **WAVEFORMATEX** para AC-3 es actualmente el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="e7746-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="e7746-141">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e7746-141">MPEG-2 Audio</span></span>

<span data-ttu-id="e7746-142">En el caso de audio MPEG-2, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7746-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="e7746-143">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="e7746-143">PES output</span></span>                    | <span data-ttu-id="e7746-144">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="e7746-144">Payload output</span></span>                 |
| <span data-ttu-id="e7746-145">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="e7746-145">Major Type</span></span>       | <span data-ttu-id="e7746-146">**\_PES MPEG2 \_ PE**</span><span class="sxs-lookup"><span data-stu-id="e7746-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="e7746-147">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="e7746-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="e7746-148">Subtype</span></span>          | <span data-ttu-id="e7746-149">**\_Audio MPEG2 de MEDIASUBTYE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="e7746-150">**\_Audio MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="e7746-151">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-151">Format Type</span></span>      | <span data-ttu-id="e7746-152">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e7746-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="e7746-153">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e7746-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="e7746-154">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-154">Format Structure</span></span> | <span data-ttu-id="e7746-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e7746-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="e7746-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e7746-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="e7746-157">El miembro **wFormatTag** de la estructura **WAVEFORMATEX** para audio MPEG-2 es actualmente el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="e7746-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="e7746-158">El separador MPEG-2 supone que las secuencias d0 a DF se usan para el flujo de extensión multicanal, ya que son para audio MPEG-2 de DVD.</span><span class="sxs-lookup"><span data-stu-id="e7746-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="e7746-159">Por lo tanto, cada vez que se selecciona Stream C *x* , el divisor reenvía también los paquetes para Stream D *x* .</span><span class="sxs-lookup"><span data-stu-id="e7746-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="e7746-160">Audio LPCM</span><span class="sxs-lookup"><span data-stu-id="e7746-160">LPCM Audio</span></span>

<span data-ttu-id="e7746-161">En el caso de audio LPCM, los tipos de medios son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7746-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="e7746-162">Salida de PES</span><span class="sxs-lookup"><span data-stu-id="e7746-162">PES output</span></span>                         | <span data-ttu-id="e7746-163">Salida de carga</span><span class="sxs-lookup"><span data-stu-id="e7746-163">Payload output</span></span>                     |
| <span data-ttu-id="e7746-164">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="e7746-164">Major Type</span></span>       | <span data-ttu-id="e7746-165">**\_PES MPEG2 \_ PE**</span><span class="sxs-lookup"><span data-stu-id="e7746-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="e7746-166">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="e7746-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="e7746-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="e7746-167">Subtype</span></span>          | <span data-ttu-id="e7746-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="e7746-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="e7746-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="e7746-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="e7746-170">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-170">Format Type</span></span>      | <span data-ttu-id="e7746-171">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e7746-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="e7746-172">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="e7746-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="e7746-173">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="e7746-173">Format Structure</span></span> | <span data-ttu-id="e7746-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e7746-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="e7746-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e7746-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="e7746-176">Actualmente, el miembro **wFormatTag** de la estructura **WAVEFORMATEX** para audio LPCM es el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.</span><span class="sxs-lookup"><span data-stu-id="e7746-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7746-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7746-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7746-178">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e7746-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
