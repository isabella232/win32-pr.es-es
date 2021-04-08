---
description: Administración de calidad de vídeo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Administración de calidad de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001439"
---
# <a name="video-quality-management"></a><span data-ttu-id="2bd73-103">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="2bd73-103">Video Quality Management</span></span>

<span data-ttu-id="2bd73-104">En este tema se describen algunas mejoras de la canalización de vídeo en Windows 7, tanto para Microsoft Media Foundation como para Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2bd73-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="2bd73-105">En un mundo perfecto, el vídeo nunca se encontraría sin problemas, independientemente de la resolución de vídeo o la carga de CPU/GPU.</span><span class="sxs-lookup"><span data-stu-id="2bd73-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="2bd73-106">En realidad, por supuesto, la canalización de vídeo debe ser capaz de hacer frente a los recursos de hardware finitos y debe adaptar de modo adaptable la reproducción al entorno del sistema.</span><span class="sxs-lookup"><span data-stu-id="2bd73-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="2bd73-107">Los objetivos de administración de calidad de vídeo son:</span><span class="sxs-lookup"><span data-stu-id="2bd73-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="2bd73-108">Reduzca los problemas (fotogramas descartados o de última hora).</span><span class="sxs-lookup"><span data-stu-id="2bd73-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="2bd73-109">Reduzca el uso de memoria, especialmente en la GPU.</span><span class="sxs-lookup"><span data-stu-id="2bd73-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="2bd73-110">Reduzca el consumo de energía, especialmente en equipos portátiles que funcionen con batería.</span><span class="sxs-lookup"><span data-stu-id="2bd73-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="2bd73-111">Obtenga la mejor calidad de imagen posible, dadas las restricciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bd73-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="2bd73-112">Mantenga el vídeo sincronizado con audio.</span><span class="sxs-lookup"><span data-stu-id="2bd73-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="2bd73-113">Algunos de estos objetivos son contrario, especialmente en los sistemas de low-end.</span><span class="sxs-lookup"><span data-stu-id="2bd73-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="2bd73-114">Por lo general, hay un equilibrio entre la velocidad y la calidad.</span><span class="sxs-lookup"><span data-stu-id="2bd73-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="2bd73-115">El problema es más objeción que las reducciones moderadas en la calidad visual.</span><span class="sxs-lookup"><span data-stu-id="2bd73-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="2bd73-116">La importancia relativa del consumo de energía varía en función del entorno; en un portátil que funciona con batería, es muy importante.</span><span class="sxs-lookup"><span data-stu-id="2bd73-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="2bd73-117">En Windows 7, el representador de vídeo mejorado (EVR) ofrece una mejor compatibilidad con la administración de calidad de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="2bd73-118">Tanto la canalización de Media Foundation como la canalización de DirectShow se han actualizado para aprovechar estas capacidades.</span><span class="sxs-lookup"><span data-stu-id="2bd73-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="2bd73-119">Se usa un enfoque de dos puntas:</span><span class="sxs-lookup"><span data-stu-id="2bd73-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="2bd73-120">Antes de que se inicie la reproducción, la canalización puede realizar optimizaciones estáticas, en función de la configuración de la administración de energía del usuario y de la información sobre el hardware.</span><span class="sxs-lookup"><span data-stu-id="2bd73-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="2bd73-121">Una vez iniciada la reproducción, la canalización puede aplicar optimizaciones dinámicas en función del rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2bd73-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="2bd73-122">Administración de calidad en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bd73-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="2bd73-123">Para habilitar las optimizaciones estáticas, establezca el atributo de [ \_ \_ \_ \_ optimizaciones de reproducción estática de la topología MF](mf-topology-static-playback-optimizations.md) en la topología parcial antes de resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="2bd73-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="2bd73-124">El cargador de topología consulta este atributo en su método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="2bd73-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="2bd73-125">Si habilita las optimizaciones estáticas, debe establecer otros dos atributos en la topología:</span><span class="sxs-lookup"><span data-stu-id="2bd73-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="2bd73-126">Atributo</span><span class="sxs-lookup"><span data-stu-id="2bd73-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="2bd73-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd73-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2bd73-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_DiMS de reproducción de topologías \_ \_ máx \_ .</span><span class="sxs-lookup"><span data-stu-id="2bd73-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="2bd73-129">Especifica el tamaño máximo de la ventana de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="2bd73-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>velocidad de reproducción de \_ topología MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd73-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="2bd73-131">Especifica la frecuencia de actualización del monitor.</span><span class="sxs-lookup"><span data-stu-id="2bd73-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="2bd73-132">Estos dos atributos ayudan a la canalización a calcular el valor más eficaz para la administración de calidad.</span><span class="sxs-lookup"><span data-stu-id="2bd73-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="2bd73-133">El administrador de calidad realiza las optimizaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2bd73-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="2bd73-134">No es necesario hacer nada para habilitar el administrador de calidad. se habilita automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2bd73-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="2bd73-135">El administrador de calidad existía en Windows Vista; en Windows 7, EVR puede responder mejor a los mensajes del administrador de calidad.</span><span class="sxs-lookup"><span data-stu-id="2bd73-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="2bd73-136">Administración de calidad en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2bd73-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="2bd73-137">DirectShow admite las optimizaciones estáticas y dinámicas para la reproducción de DVD.</span><span class="sxs-lookup"><span data-stu-id="2bd73-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="2bd73-138">Para habilitar estas optimizaciones en una aplicación de reproducción de DVD, establezca las marcas siguientes en el parámetro *dwFlags* del método **IDvdGraphBuilder:: RenderDvdVideoVolume** :</span><span class="sxs-lookup"><span data-stu-id="2bd73-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="2bd73-139">Marca</span><span class="sxs-lookup"><span data-stu-id="2bd73-139">Flag</span></span>                  | <span data-ttu-id="2bd73-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd73-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="2bd73-141">gráfico de la \_ adaptación del DVD \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd73-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="2bd73-142">Habilita las optimizaciones estáticas.</span><span class="sxs-lookup"><span data-stu-id="2bd73-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="2bd73-143">\_ \_ QoS EVR de \_ DVD</span><span class="sxs-lookup"><span data-stu-id="2bd73-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="2bd73-144">Habilita las optimizaciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2bd73-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="2bd73-145">Otras aplicaciones de DirectShow pueden habilitar las optimizaciones dinámicas llamando al método [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) directamente en el filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="2bd73-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="2bd73-146">Especifique la **marca \_ EnableQoS de EVRFilterConfigPrefs** .</span><span class="sxs-lookup"><span data-stu-id="2bd73-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="2bd73-147">Las optimizaciones estáticas en DirectShow se limitan a la reproducción de DVD.</span><span class="sxs-lookup"><span data-stu-id="2bd73-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="2bd73-148">Administración de calidad en EVR</span><span class="sxs-lookup"><span data-stu-id="2bd73-148">Quality Management in the EVR</span></span>

<span data-ttu-id="2bd73-149">EVR admite algunas nuevas marcas de configuración para la administración de la calidad.</span><span class="sxs-lookup"><span data-stu-id="2bd73-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="2bd73-150">Si habilita las optimizaciones de administración de calidad descritas anteriormente, no es necesario establecer estas marcas directamente.</span><span class="sxs-lookup"><span data-stu-id="2bd73-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="2bd73-151">Sin embargo, están documentadas para las aplicaciones que quieren un control más granular sobre el EVR.</span><span class="sxs-lookup"><span data-stu-id="2bd73-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="2bd73-152">Establezca las marcas siguientes en el mezclador EVR llamando al método [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :</span><span class="sxs-lookup"><span data-stu-id="2bd73-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd73-153">Marcas</span><span class="sxs-lookup"><span data-stu-id="2bd73-153">Flags</span></span></th>
<th><span data-ttu-id="2bd73-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd73-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2bd73-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="2bd73-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="2bd73-157">Omitir el segundo campo de cada fotograma entrelazado.</span><span class="sxs-lookup"><span data-stu-id="2bd73-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="2bd73-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="2bd73-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="2bd73-160">Use el desentrelazado de Bob, incluso si el controlador admite un modo de desentrelazado de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="2bd73-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2bd73-161">Establezca las marcas siguientes en el presentador EVR llamando al método [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :</span><span class="sxs-lookup"><span data-stu-id="2bd73-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bd73-162">Marcas</span><span class="sxs-lookup"><span data-stu-id="2bd73-162">Flags</span></span></th>
<th><span data-ttu-id="2bd73-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bd73-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2bd73-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="2bd73-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="2bd73-166">Limite la salida para que coincida con el ancho de banda de GPU.</span><span class="sxs-lookup"><span data-stu-id="2bd73-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="2bd73-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="2bd73-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="2bd73-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="2bd73-169">Llamadas presentes de Direct3D por lotes.</span><span class="sxs-lookup"><span data-stu-id="2bd73-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="2bd73-170">Esta optimización permite al sistema entrar en Estados inactivos con más frecuencia, lo que puede reducir el consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="2bd73-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2bd73-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="2bd73-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="2bd73-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="2bd73-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="2bd73-173">Realice la combinación de vídeo con un rectángulo más pequeño que el rectángulo de salida.</span><span class="sxs-lookup"><span data-stu-id="2bd73-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="2bd73-174">Escale el resultado al tamaño de salida correcto.</span><span class="sxs-lookup"><span data-stu-id="2bd73-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2bd73-175">Además, el receptor de medios EVR admite atributos de configuración que se corresponden con cada una de estas marcas:</span><span class="sxs-lookup"><span data-stu-id="2bd73-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="2bd73-176">EVRConfig \_ AllowBatching</span><span class="sxs-lookup"><span data-stu-id="2bd73-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="2bd73-177">EVRConfig \_ AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="2bd73-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="2bd73-178">EVRConfig \_ AllowDropToHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="2bd73-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="2bd73-179">EVRConfig \_ AllowScaling</span><span class="sxs-lookup"><span data-stu-id="2bd73-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="2bd73-180">EVRConfig \_ AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="2bd73-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="2bd73-181">EVRConfig \_ ForceBatching</span><span class="sxs-lookup"><span data-stu-id="2bd73-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="2bd73-182">EVRConfig \_ ForceBob</span><span class="sxs-lookup"><span data-stu-id="2bd73-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="2bd73-183">EVRConfig \_ ForceHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="2bd73-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="2bd73-184">EVRConfig \_ ForceScaling</span><span class="sxs-lookup"><span data-stu-id="2bd73-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="2bd73-185">EVRConfig \_ ForceThrottle</span><span class="sxs-lookup"><span data-stu-id="2bd73-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="2bd73-186">Antes de que se inicie la reproducción, puede establecer estos atributos directamente en el receptor de medios EVR, como alternativa a la llamada a los métodos [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) y [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="2bd73-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="2bd73-187">Para establecer estos atributos, consulte el receptor de medios EVR para [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="2bd73-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bd73-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bd73-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd73-189">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="2bd73-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




