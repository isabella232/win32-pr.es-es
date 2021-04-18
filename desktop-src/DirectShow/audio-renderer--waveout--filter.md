---
description: Filtro de representador de audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro de representador de audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686406"
---
# <a name="audio-renderer-waveout-filter"></a><span data-ttu-id="b487a-103">Filtro de representador de audio (WaveOut)</span><span class="sxs-lookup"><span data-stu-id="b487a-103">Audio Renderer (WaveOut) Filter</span></span>

<span data-ttu-id="b487a-104">Este filtro usa la API de waveOut \* para representar el audio de una onda.</span><span class="sxs-lookup"><span data-stu-id="b487a-104">This filter uses the waveOut\* API to render waveform audio.</span></span> <span data-ttu-id="b487a-105">Sin embargo, el [filtro de representador de DirectSound](directsound-renderer-filter.md) proporciona la misma funcionalidad mediante DirectSound.</span><span class="sxs-lookup"><span data-stu-id="b487a-105">However, the [DirectSound Renderer Filter](directsound-renderer-filter.md) provides the same functionality using DirectSound.</span></span> <span data-ttu-id="b487a-106">De forma predeterminada, Filter Graph Manager usa el representador de DirectSound en lugar de este filtro.</span><span class="sxs-lookup"><span data-stu-id="b487a-106">By default, the Filter Graph Manager uses the DirectSound Renderer instead of this filter.</span></span> <span data-ttu-id="b487a-107">La mezcla de audio está deshabilitada en el representador de audio waveOut, por lo que si necesita mezclar varias transmisiones de audio durante la reproducción, use el representador de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="b487a-107">Audio mixing is disabled in the waveOut Audio Renderer, so if you need to mix multiple audio streams during playback, use the DirectSound renderer.</span></span>

<span data-ttu-id="b487a-108">Este filtro no comprueba el subtipo de la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b487a-108">This filter does not check the audio stream's subtype.</span></span> <span data-ttu-id="b487a-109">La estructura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) pasada en el formato contiene la información necesaria para la conexión.</span><span class="sxs-lookup"><span data-stu-id="b487a-109">The [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure passed in the format contains the information needed for the connection.</span></span>

<span data-ttu-id="b487a-110">Este filtro admite un intervalo de frecuencias de muestreo que depende del controlador de audio.</span><span class="sxs-lookup"><span data-stu-id="b487a-110">This filter supports a range of sample rates that depends on the audio driver.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b487a-111">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="b487a-111">Filter Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="b487a-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></span></span></li>
<li><span data-ttu-id="b487a-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></span></span></li>
<li><span data-ttu-id="b487a-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-114"><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></span></span></li>
<li><span data-ttu-id="b487a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></span></span></li>
<li><span data-ttu-id="b487a-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="b487a-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-117"><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></span></span></li>
<li><span data-ttu-id="b487a-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-118"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="b487a-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-119"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="b487a-120">IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b487a-120">IPersistPropertyBag</span></span></li>
<li><span data-ttu-id="b487a-121">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="b487a-121">IPersistStream</span></span></li>
<li><span data-ttu-id="b487a-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="b487a-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b487a-124">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="b487a-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="b487a-125"><strong>MEDIATYPE_Audio</strong></span><span class="sxs-lookup"><span data-stu-id="b487a-125"><strong>MEDIATYPE_Audio</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b487a-126">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="b487a-126">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="b487a-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-127"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="b487a-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-128"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="b487a-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b487a-129"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b487a-130">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="b487a-130">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="b487a-131">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="b487a-131">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b487a-132">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="b487a-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="b487a-133">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="b487a-133">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b487a-134">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="b487a-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="b487a-135"><strong>CLSID_AudioRender</strong></span><span class="sxs-lookup"><span data-stu-id="b487a-135"><strong>CLSID_AudioRender</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b487a-136">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="b487a-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="b487a-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span><span class="sxs-lookup"><span data-stu-id="b487a-137"><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b487a-138">Executable</span><span class="sxs-lookup"><span data-stu-id="b487a-138">Executable</span></span></td>
<td><span data-ttu-id="b487a-139">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b487a-139">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b487a-140"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="b487a-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b487a-141"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="b487a-141"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b487a-142"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="b487a-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b487a-143"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="b487a-143"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b487a-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b487a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b487a-145">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="b487a-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
