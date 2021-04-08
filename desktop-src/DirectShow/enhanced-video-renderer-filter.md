---
description: El filtro de representador de vídeo mejorado (EVR) es un representador y mezclador de vídeo de 16 canales. Tiene la misma funcionalidad principal y el mismo modelo de complemento que el Media Foundation receptor de medios EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de representador de vídeo mejorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079978"
---
# <a name="enhanced-video-renderer-filter"></a><span data-ttu-id="2b2d7-104">Filtro de representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="2b2d7-104">Enhanced Video Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="2b2d7-105">Este tema se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-105">This topic applies to Windows Vista and later.</span></span>

 

<span data-ttu-id="2b2d7-106">El filtro de representador de vídeo mejorado (EVR) es un representador y mezclador de vídeo de 16 canales.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-106">The Enhanced Video Renderer (EVR) filter is a 16-channel video mixer and renderer.</span></span> <span data-ttu-id="2b2d7-107">Tiene la misma funcionalidad principal y el mismo modelo de complemento que el Media Foundation receptor de medios EVR.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-107">It has the same core functionality and plug-in model as the Media Foundation EVR media sink.</span></span>

<span data-ttu-id="2b2d7-108">El filtro EVR de DirectShow se documenta en la documentación del SDK de Media Foundation; para obtener más información, vea [representador de vídeo mejorado](../medfound/enhanced-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="2b2d7-108">The DirectShow EVR filter is documented in the Media Foundation SDK documentation; for more information, see [Enhanced Video Renderer](../medfound/enhanced-video-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b2d7-109">Interfaces de filtro (a través de <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="2b2d7-109">Filter Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="2b2d7-110">Interfaces de DirectShow:</span><span class="sxs-lookup"><span data-stu-id="2b2d7-110">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="2b2d7-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-111"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-112"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-114"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-118"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
</ul>
<span data-ttu-id="2b2d7-119">Interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="2b2d7-119">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="2b2d7-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-120"><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-121"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-122"><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-123"><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b2d7-124">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="2b2d7-124">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="2b2d7-125">Variable, dependiendo del controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-125">Variable, depending on the graphics driver.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b2d7-126">Interfaces de PIN de entrada (a través de <strong>QueryInterface</strong>)</span><span class="sxs-lookup"><span data-stu-id="2b2d7-126">Input Pin Interfaces (through <strong>QueryInterface</strong>)</span></span></td>
<td><span data-ttu-id="2b2d7-127">Interfaces de DirectShow:</span><span class="sxs-lookup"><span data-stu-id="2b2d7-127">DirectShow interfaces:</span></span>
<ul>
<li><span data-ttu-id="2b2d7-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-128"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-130"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="2b2d7-131">Interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="2b2d7-131">Media Foundation interfaces:</span></span><br/>
<ul>
<li><span data-ttu-id="2b2d7-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-132"><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-133"><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></span></span></li>
<li><span data-ttu-id="2b2d7-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-134"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b2d7-135">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="2b2d7-135">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="2b2d7-136">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-136">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b2d7-137">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="2b2d7-137">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="2b2d7-138">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-138">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b2d7-139">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="2b2d7-139">Filter CLSID</span></span></td>
<td><span data-ttu-id="2b2d7-140">CLSID_EnhancedVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="2b2d7-140">CLSID_EnhancedVideoRenderer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b2d7-141">Executable</span><span class="sxs-lookup"><span data-stu-id="2b2d7-141">Executable</span></span></td>
<td><span data-ttu-id="2b2d7-142">evr.dll</span><span class="sxs-lookup"><span data-stu-id="2b2d7-142">evr.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b2d7-143"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-143"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="2b2d7-144">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="2b2d7-144">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b2d7-145"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="2b2d7-145"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="2b2d7-146">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2b2d7-146">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2b2d7-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b2d7-147">Remarks</span></span>

<span data-ttu-id="2b2d7-148">Además de las interfaces expuestas a través de **QueryInterface**, el EVR expone otras interfaces a través del método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) .</span><span class="sxs-lookup"><span data-stu-id="2b2d7-148">In addition to the interfaces exposed through **QueryInterface**, the EVR exposes other interfaces through the [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span> <span data-ttu-id="2b2d7-149">Algunas de estas interfaces las implementa el presentador EVR o el mezclador EVR, en lugar del propio EVR.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-149">Some of these interfaces are implemented by the EVR presenter or the EVR mixer, rather than the EVR itself.</span></span> <span data-ttu-id="2b2d7-150">Si la aplicación establece un presentador o mezclador personalizado en EVR, las versiones personalizadas podrían exponer un conjunto de interfaces diferente.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-150">If the application sets a custom presenter or mixer on the EVR, the custom versions might expose a different set of interfaces.</span></span>



| <span data-ttu-id="2b2d7-151">Object</span><span class="sxs-lookup"><span data-stu-id="2b2d7-151">Object</span></span>     | <span data-ttu-id="2b2d7-152">Identificador de servicio</span><span class="sxs-lookup"><span data-stu-id="2b2d7-152">Service Identifier</span></span>                                              | <span data-ttu-id="2b2d7-153">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2b2d7-153">Interfaces</span></span>                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2d7-154">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="2b2d7-154">EVR filter</span></span> | <span data-ttu-id="2b2d7-155">\_ \_ \_ Servicio de representación de vídeo Mr (consultas EVR o Presenter)</span><span class="sxs-lookup"><span data-stu-id="2b2d7-155">MR\_VIDEO\_RENDER\_SERVICE(Queries EVR or presenter)</span></span><br/> | [<span data-ttu-id="2b2d7-156">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-156">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="2b2d7-157">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-157">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [<span data-ttu-id="2b2d7-158">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-158">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="2b2d7-159">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-159">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| <span data-ttu-id="2b2d7-160">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="2b2d7-160">EVR filter</span></span> | <span data-ttu-id="2b2d7-161">\_Servicio de aceleración de vídeo Mr \_ \_ (presentador de consultas)</span><span class="sxs-lookup"><span data-stu-id="2b2d7-161">MR\_VIDEO\_ACCELERATION\_SERVICE(Queries presenter)</span></span><br/>  | [<span data-ttu-id="2b2d7-162">**IDirect3DDeviceManager9**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-162">**IDirect3DDeviceManager9**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2b2d7-163">Filtro de EVR</span><span class="sxs-lookup"><span data-stu-id="2b2d7-163">EVR filter</span></span> | <span data-ttu-id="2b2d7-164">\_Servicio de mezclador de vídeo Mr \_ \_ (mezclador de consultas)</span><span class="sxs-lookup"><span data-stu-id="2b2d7-164">MR\_VIDEO\_MIXER\_SERVICE(Queries mixer)</span></span><br/>             | [<span data-ttu-id="2b2d7-165">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-165">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [<span data-ttu-id="2b2d7-166">**IMFVideoMixerBitmap**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-166">**IMFVideoMixerBitmap**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [<span data-ttu-id="2b2d7-167">**IMFVideoMixerControl**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-167">**IMFVideoMixerControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [<span data-ttu-id="2b2d7-168">**IMFVideoPositionMapper**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-168">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [<span data-ttu-id="2b2d7-169">**IMFVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-169">**IMFVideoProcessor**</span></span>](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| <span data-ttu-id="2b2d7-170">Clavijas de entrada</span><span class="sxs-lookup"><span data-stu-id="2b2d7-170">Input pins</span></span> | <span data-ttu-id="2b2d7-171">\_servicio de \_ aceleración de vídeo Mr \_</span><span class="sxs-lookup"><span data-stu-id="2b2d7-171">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>                                | [<span data-ttu-id="2b2d7-172">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="2b2d7-172">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

<span data-ttu-id="2b2d7-173">EVR puede mezclar hasta 16 secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-173">The EVR can mix up to 16 video streams.</span></span> <span data-ttu-id="2b2d7-174">El primer flujo de entrada (pin 0) se denomina *flujo de referencia*.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-174">The first input stream (pin 0) is called the *reference stream*.</span></span> <span data-ttu-id="2b2d7-175">El flujo de referencia siempre aparece primero en el orden z.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-175">The reference stream always appears first in the z-order.</span></span> <span data-ttu-id="2b2d7-176">Los flujos adicionales se denominan subsecuencias y se mezclan en la parte superior de la secuencia de referencia.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-176">Any additional streams are called substreams, and are mixed on top of the reference stream.</span></span> <span data-ttu-id="2b2d7-177">La aplicación puede cambiar el orden z de las subsecuencias, pero no puede haber ningún subflujo en primer lugar en el orden z.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-177">The application can change the z-order of the substreams, but no substream can be first in the z-order.</span></span>

<span data-ttu-id="2b2d7-178">El controlador de gráficos determina qué formatos de vídeo se admiten, pero normalmente se limitan a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b2d7-178">The graphics driver determines which video formats are supported, but typically they are limited to the following:</span></span>

-   <span data-ttu-id="2b2d7-179">Secuencia de referencia: YUV progresivo o entrelazado sin alfa por píxel (como NV12 o YUY2); o RGB progresivo.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-179">Reference stream: Progressive or interlaced YUV with no per-pixel alpha (such as NV12 or YUY2); or progressive RGB.</span></span>
-   <span data-ttu-id="2b2d7-180">Subsecuencias: YUV progresivo con alfa por píxel, como AYUV o AI44.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-180">Substreams: Progressive YUV with per-pixel-alpha, such as AYUV or AI44.</span></span>

<span data-ttu-id="2b2d7-181">Los formatos de subflujo disponibles pueden depender del formato del flujo de referencia.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-181">The available substream formats might depend on the format of the reference stream.</span></span>

<span data-ttu-id="2b2d7-182">EVR reenvía los comandos de búsqueda hacia arriba a través del PIN 0.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-182">The EVR forwards seek commands upstream through pin 0.</span></span> <span data-ttu-id="2b2d7-183">Los pin de subsecuencia no reenvían los comandos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-183">The substream pins do not forward seek commands.</span></span> <span data-ttu-id="2b2d7-184">Es responsabilidad del filtro de origen o divisor mantener las subsecuencias sincronizadas con la secuencia de referencia.</span><span class="sxs-lookup"><span data-stu-id="2b2d7-184">It is the responsibility of the source or splitter filter to keep the substreams synchronized with the reference stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2d7-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b2d7-185">Requirements</span></span>



| <span data-ttu-id="2b2d7-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2d7-186">Requirement</span></span> | <span data-ttu-id="2b2d7-187">Value</span><span class="sxs-lookup"><span data-stu-id="2b2d7-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b2d7-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b2d7-188">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2d7-189">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b2d7-189">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b2d7-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b2d7-190">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2d7-191">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b2d7-191">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b2d7-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b2d7-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2d7-193">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="2b2d7-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

