---
description: Filtro de representador de DirectSound
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: Filtro de representador de DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151997"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="bea2c-103">Filtro de representador de DirectSound</span><span class="sxs-lookup"><span data-stu-id="bea2c-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="bea2c-104">Este filtro representa el audio mediante DirectSound.</span><span class="sxs-lookup"><span data-stu-id="bea2c-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="bea2c-105">Este filtro es actualmente el representador de audio predeterminado para el sonido de la forma de onda.</span><span class="sxs-lookup"><span data-stu-id="bea2c-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="bea2c-106">Además de sus capacidades básicas de representación de sonido, este filtro puede procesar llamadas API de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="bea2c-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="bea2c-107">Use los métodos [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) para establecer y recuperar la ventana que controlará la reproducción del sonido.</span><span class="sxs-lookup"><span data-stu-id="bea2c-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="bea2c-108">DirectSound audio renderer es el filtro de representación de audio predeterminado para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bea2c-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bea2c-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="bea2c-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="bea2c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="bea2c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea2c-111">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="bea2c-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="bea2c-112">Tipo principal: MEDIATYPE_AudioSubtypes:</span><span class="sxs-lookup"><span data-stu-id="bea2c-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="bea2c-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="bea2c-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="bea2c-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="bea2c-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="bea2c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="bea2c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="bea2c-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="bea2c-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="bea2c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="bea2c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="bea2c-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="bea2c-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="bea2c-119">Tipo de formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="bea2c-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bea2c-120">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="bea2c-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="bea2c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="bea2c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea2c-122">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="bea2c-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="bea2c-123">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="bea2c-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bea2c-124">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="bea2c-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="bea2c-125">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="bea2c-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea2c-126">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="bea2c-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="bea2c-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="bea2c-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bea2c-128">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="bea2c-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="bea2c-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="bea2c-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea2c-130">Executable</span><span class="sxs-lookup"><span data-stu-id="bea2c-130">Executable</span></span></td>
<td><span data-ttu-id="bea2c-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="bea2c-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bea2c-132"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="bea2c-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="bea2c-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="bea2c-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea2c-134"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="bea2c-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="bea2c-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="bea2c-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="bea2c-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea2c-136">Remarks</span></span>

<span data-ttu-id="bea2c-137">Este filtro actúa como un contenedor para un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="bea2c-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="bea2c-138">Para enumerar los dispositivos de audio disponibles en el sistema del usuario, use la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) con la categoría de representador de audio (CLSID \_ AudioRendererCategory).</span><span class="sxs-lookup"><span data-stu-id="bea2c-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="bea2c-139">Para cada dispositivo de audio, la categoría representador de audio contiene dos instancias de filtro.</span><span class="sxs-lookup"><span data-stu-id="bea2c-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="bea2c-140">Uno de ellos corresponde al representador de DirectSound y el otro corresponde al filtro de [representador de audio (WaveOut)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="bea2c-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="bea2c-141">La instancia de DirectSound tiene el nombre descriptivo "DirectSound: *DeviceName*", donde *DeviceName* es el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bea2c-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="bea2c-142">La instancia de WaveOut tiene el nombre descriptivo *DeviceName*.</span><span class="sxs-lookup"><span data-stu-id="bea2c-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="bea2c-143">La categoría representador de audio contiene dos instancias de filtro adicionales, denominadas "dispositivo DirectSound predeterminado" y "dispositivo WaveOut predeterminado".</span><span class="sxs-lookup"><span data-stu-id="bea2c-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="bea2c-144">Estos se corresponden con el dispositivo de sonido predeterminado, elegido por el usuario a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="bea2c-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="bea2c-145">En realidad, se asignan a uno de los pares descritos en el párrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="bea2c-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="bea2c-146">Por ejemplo, si el sistema tiene dos dispositivos de audio, el dispositivo A y el dispositivo B, la categoría de representador de audio contendrá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bea2c-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="bea2c-147">Dispositivo A</span><span class="sxs-lookup"><span data-stu-id="bea2c-147">Device A</span></span>
-   <span data-ttu-id="bea2c-148">DirectSound: dispositivo A</span><span class="sxs-lookup"><span data-stu-id="bea2c-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="bea2c-149">Dispositivo B</span><span class="sxs-lookup"><span data-stu-id="bea2c-149">Device B</span></span>
-   <span data-ttu-id="bea2c-150">DirectSound: dispositivo B</span><span class="sxs-lookup"><span data-stu-id="bea2c-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="bea2c-151">Dispositivo DirectSound predeterminado</span><span class="sxs-lookup"><span data-stu-id="bea2c-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="bea2c-152">Dispositivo WaveOut predeterminado</span><span class="sxs-lookup"><span data-stu-id="bea2c-152">Default WaveOut Device</span></span>

<span data-ttu-id="bea2c-153">Si el usuario seleccionó el dispositivo A como el dispositivo predeterminado, el "dispositivo de DirectSound predeterminado" es equivalente a "DirectSound: dispositivo A" y "dispositivo WaveOut predeterminado" es equivalente a "dispositivo A".</span><span class="sxs-lookup"><span data-stu-id="bea2c-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="bea2c-154">Si el usuario selecciona el dispositivo B como dispositivo predeterminado, se cambiarán estas asignaciones.</span><span class="sxs-lookup"><span data-stu-id="bea2c-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="bea2c-155">El "dispositivo DirectSound predeterminado" tiene asignado el mérito de los MÉRITOs \_ preferidos.</span><span class="sxs-lookup"><span data-stu-id="bea2c-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="bea2c-156">Los demás tienen MÉRITOs \_ que \_ no \_ usan.</span><span class="sxs-lookup"><span data-stu-id="bea2c-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="bea2c-157">Por lo tanto, Intelligent Connect siempre elegirá el dispositivo DirectSound predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bea2c-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="bea2c-158">El filtro de representador de DirectSound admite el sonido 3D a través de las interfaces **IDirectSound3DBuffer** y **IDirectSound3dListener** de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="bea2c-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="bea2c-159">También puede consultar el filtro para las versiones actuales de estas interfaces, **IDirectSound3DBuffer8** y **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="bea2c-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="bea2c-160">Ejecute el gráfico antes de llamar a métodos en estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bea2c-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bea2c-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bea2c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bea2c-162">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="bea2c-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




