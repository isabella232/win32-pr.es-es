---
description: Filtro de representador de mezcla de vídeo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro de representador de mezcla de vídeo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543774"
---
# <a name="video-mixing-renderer-filter-7"></a><span data-ttu-id="0149a-103">Filtro de representador de mezcla de vídeo 7</span><span class="sxs-lookup"><span data-stu-id="0149a-103">Video Mixing Renderer Filter 7</span></span>

<span data-ttu-id="0149a-104">Este tema se aplica a Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="0149a-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="0149a-105">En Windows XP y versiones posteriores, el representador de vídeo 7 (VMR-7) es el representador de vídeo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0149a-105">In Windows XP and later, the Video Mixing Renderer 7 (VMR-7) is the default video renderer.</span></span> <span data-ttu-id="0149a-106">Se denomina VMR-7 porque internamente usa DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="0149a-106">It is called the VMR-7 because internally it uses DirectDraw 7.</span></span> <span data-ttu-id="0149a-107">En DirectX 9, un filtro similar, pero independiente, de VMR-9, está disponible para la redistribución en sistemas que no son XP.</span><span class="sxs-lookup"><span data-stu-id="0149a-107">In DirectX 9, a similar but separate filter, the VMR-9, is available for redistribution on non-XP systems.</span></span> <span data-ttu-id="0149a-108">VMR-9 usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0149a-108">The VMR-9 uses Direct3D 9.</span></span>

> [!Note]  
> <span data-ttu-id="0149a-109">VMR está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0149a-109">The VMR is available on Windows XP and later.</span></span> <span data-ttu-id="0149a-110">No está disponible a través de DirectX Redistributable o en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="0149a-110">It is not available through the DirectX redistributable, or on previous versions of Windows.</span></span> <span data-ttu-id="0149a-111">En la mayoría de los escenarios, las aplicaciones deben usar el [representador de combinación de vídeo 9](video-mixing-renderer-filter-9.md).</span><span class="sxs-lookup"><span data-stu-id="0149a-111">For most scenarios, applications should use the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md).</span></span>

 

<span data-ttu-id="0149a-112">Las características de VMR incluyen:</span><span class="sxs-lookup"><span data-stu-id="0149a-112">Features of the VMR include:</span></span>

-   <span data-ttu-id="0149a-113">Combinación alfa verdadera de hasta 16 flujos de entrada</span><span class="sxs-lookup"><span data-stu-id="0149a-113">True alpha blending of up to 16 input streams</span></span>
-   <span data-ttu-id="0149a-114">Acceso a la imagen compuesta antes de que se represente</span><span class="sxs-lookup"><span data-stu-id="0149a-114">Access to the composited image before it is rendered</span></span>
-   <span data-ttu-id="0149a-115">Un modelo de complemento que permite a terceros implementar efectos de vídeo personalizados.</span><span class="sxs-lookup"><span data-stu-id="0149a-115">A plug-in model that enables third-parties to implement custom video effects.</span></span>
-   <span data-ttu-id="0149a-116">Compatibilidad con hasta 15 monitores.</span><span class="sxs-lookup"><span data-stu-id="0149a-116">Support for up to 15 monitors.</span></span>

<span data-ttu-id="0149a-117">Durante la creación de gráficos en Windows XP y versiones posteriores, el administrador de gráficos de filtros no usará los filtros de representador de vídeo más antiguo ni los de la superposición, a menos que la aplicación los cree explícitamente y agregue al gráfico.</span><span class="sxs-lookup"><span data-stu-id="0149a-117">During graph building on Windows XP and later, the Filter Graph Manager will not use the older Video Renderer or Overlay Mixer filters, unless the application explicitly creates them and adds to the graph.</span></span>

<span data-ttu-id="0149a-118">Para obtener más información, vea [usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="0149a-118">For more information, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0149a-119">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="0149a-119">Filter Interfaces</span></span></td>
<td><span data-ttu-id="0149a-120">Todos los modos:</span><span class="sxs-lookup"><span data-stu-id="0149a-120">All modes:</span></span>
<ul>
<li><span data-ttu-id="0149a-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></span></span></li>
<li><span data-ttu-id="0149a-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-122"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="0149a-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-123"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="0149a-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-124"><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></span></span></li>
<li><span data-ttu-id="0149a-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-125"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></span></span></li>
<li><span data-ttu-id="0149a-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></li>
<li><span data-ttu-id="0149a-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="0149a-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-128"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></li>
<li><span data-ttu-id="0149a-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-129"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="0149a-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-130"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="0149a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="0149a-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-132"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
</ul>
<span data-ttu-id="0149a-133">Modo de ventana:</span><span class="sxs-lookup"><span data-stu-id="0149a-133">Windowed mode:</span></span><br/>
<ul>
<li><span data-ttu-id="0149a-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-134"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></span></span></li>
<li><span data-ttu-id="0149a-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-135"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></li>
<li><span data-ttu-id="0149a-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-136"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></li>
<li><span data-ttu-id="0149a-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-137"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="0149a-138">Modo sin ventanas:</span><span class="sxs-lookup"><span data-stu-id="0149a-138">Windowless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="0149a-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-139"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
<li><span data-ttu-id="0149a-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-140"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></span></span></li>
</ul>
<span data-ttu-id="0149a-141">Modo no representativo:</span><span class="sxs-lookup"><span data-stu-id="0149a-141">Renderless mode:</span></span><br/>
<ul>
<li><span data-ttu-id="0149a-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-142"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
</ul>
<span data-ttu-id="0149a-143">Modo de mezclador:</span><span class="sxs-lookup"><span data-stu-id="0149a-143">Mixer mode:</span></span><br/>
<ul>
<li><span data-ttu-id="0149a-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-144"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
</ul>
<span data-ttu-id="0149a-145">Para obtener información sobre los distintos modos de VMR-7, vea <a href="vmr-modes-of-operation.md">modos de funcionamiento de VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="0149a-145">For information about the various VMR-7 modes, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0149a-146">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="0149a-146">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="0149a-147">Tipo principal: MEDIATYPE_VideoSubtype: depende del hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="0149a-147">Major type: MEDIATYPE_VideoSubtype: Depends on the graphics hardware.</span></span> <span data-ttu-id="0149a-148">Debe ser un vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="0149a-148">Must be uncompressed video.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0149a-149">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="0149a-149">Input Pin Interfaces</span></span></td>
<td><ul>
<li><span data-ttu-id="0149a-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-150"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></span></span></li>
<li><span data-ttu-id="0149a-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-151"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></li>
<li><span data-ttu-id="0149a-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (ver comentarios)</span><span class="sxs-lookup"><span data-stu-id="0149a-152"><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (see Remarks)</span></span></li>
<li><span data-ttu-id="0149a-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-153"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></span></span></li>
<li><span data-ttu-id="0149a-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-154"><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></span></span></li>
<li><span data-ttu-id="0149a-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-155"><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></li>
<li><span data-ttu-id="0149a-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="0149a-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0149a-157">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="0149a-157">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="0149a-158">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="0149a-158">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0149a-159">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="0149a-159">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="0149a-160">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="0149a-160">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0149a-161">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="0149a-161">Filter CLSID</span></span></td>
<td><span data-ttu-id="0149a-162">Hay dos CLSID asociados a este filtro:</span><span class="sxs-lookup"><span data-stu-id="0149a-162">There are two CLSIDs associated with this filter:</span></span>
<ul>
<li><span data-ttu-id="0149a-163">CLSID_VideoMixingRenderer: crea la VMR-7.</span><span class="sxs-lookup"><span data-stu-id="0149a-163">CLSID_VideoMixingRenderer: Creates the VMR-7.</span></span> <span data-ttu-id="0149a-164">Si no hay suficientes recursos del sistema para crear el VMR-7, se produce un error en la llamada a <strong>CoCreateInstance</strong> .</span><span class="sxs-lookup"><span data-stu-id="0149a-164">If there are not enough system resources to create the VMR-7, the call to <strong>CoCreateInstance</strong> fails.</span></span></li>
<li><span data-ttu-id="0149a-165">CLSID_VideoRendererDefault: crea la VMR-7 si hay recursos del sistema disponibles, o bien crea el filtro de <a href="video-renderer-filter.md">representador de vídeo</a> antiguo.</span><span class="sxs-lookup"><span data-stu-id="0149a-165">CLSID_VideoRendererDefault: Creates the VMR-7 if system resources are available, or else creates the old <a href="video-renderer-filter.md">Video Renderer</a> filter.</span></span></li>
</ul>
<span data-ttu-id="0149a-166">Use CLSID_VideoMixingRenderer si necesita las capacidades específicas de VMR-7.</span><span class="sxs-lookup"><span data-stu-id="0149a-166">Use CLSID_VideoMixingRenderer if you need the specific capabilities of the VMR-7.</span></span> <span data-ttu-id="0149a-167">De lo contrario, use CLSID_VideoRendererDefault, que es casi seguro que no se puede producir un error, porque recurre al filtro de representador de vídeo antiguo.</span><span class="sxs-lookup"><span data-stu-id="0149a-167">Otherwise, use CLSID_VideoRendererDefault, which is almost certain not to fail, because it falls back to the old Video Renderer filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0149a-168">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0149a-168">Property Page CLSID</span></span></td>
<td><span data-ttu-id="0149a-169">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="0149a-169">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0149a-170">Executable</span><span class="sxs-lookup"><span data-stu-id="0149a-170">Executable</span></span></td>
<td><span data-ttu-id="0149a-171">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0149a-171">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0149a-172"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="0149a-172"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="0149a-173">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="0149a-173">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0149a-174"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="0149a-174"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="0149a-175">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0149a-175">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0149a-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0149a-176">Remarks</span></span>

<span data-ttu-id="0149a-177">El PIN de entrada expone la interfaz **IOverlay** solo cuando el filtro VMR-7 está en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="0149a-177">The input pin exposes the **IOverlay** interface only when the VMR-7 filter is in windowed mode.</span></span> <span data-ttu-id="0149a-178">El único método **IOverlay** que implementa el PIN es **GetWindowHandle**, que permite que una aplicación obtenga un identificador de la ventana de vídeo del filtro.</span><span class="sxs-lookup"><span data-stu-id="0149a-178">The only **IOverlay** method that the pin implements is **GetWindowHandle**, which enables an application to obtain a handle to the filter's video window.</span></span> <span data-ttu-id="0149a-179">Todos los demás métodos de **IOverlay** devuelven E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="0149a-179">All other **IOverlay** methods return E\_NOTIMPL.</span></span> <span data-ttu-id="0149a-180">En el modo sin ventanas, el filtro no crea una ventana de vídeo, por lo que el PIN no expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0149a-180">In windowless mode, the filter does not create a video window, so the pin does not expose the interface.</span></span>

<span data-ttu-id="0149a-181">Una aplicación puede proporcionar un objeto de presentador personalizado que exponga las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="0149a-181">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="0149a-182">**IVMRImagePresenter**</span><span class="sxs-lookup"><span data-stu-id="0149a-182">**IVMRImagePresenter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   <span data-ttu-id="0149a-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)</span><span class="sxs-lookup"><span data-stu-id="0149a-183">[**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (optional)</span></span>
-   <span data-ttu-id="0149a-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)</span><span class="sxs-lookup"><span data-stu-id="0149a-184">[**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (optional)</span></span>
-   [<span data-ttu-id="0149a-185">**IVMRSurfaceAllocator**</span><span class="sxs-lookup"><span data-stu-id="0149a-185">**IVMRSurfaceAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   <span data-ttu-id="0149a-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)</span><span class="sxs-lookup"><span data-stu-id="0149a-186">[**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (optional)</span></span>

<span data-ttu-id="0149a-187">Para obtener más información acerca de los presentadores personalizados, consulte [suministro de un Allocator-Presenter personalizado para VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span><span class="sxs-lookup"><span data-stu-id="0149a-187">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).</span></span>

<span data-ttu-id="0149a-188">Una aplicación también puede proporcionar un compositor de complementos personalizado que exponga la interfaz siguiente:</span><span class="sxs-lookup"><span data-stu-id="0149a-188">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="0149a-189">**IVMRImageCompositor**</span><span class="sxs-lookup"><span data-stu-id="0149a-189">**IVMRImageCompositor**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

<span data-ttu-id="0149a-190">Para configurar la VMR con un compositor personalizado, llame a [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="0149a-190">To configure the VMR with a custom compositor, call [**IVMRFilterConfig::SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0149a-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0149a-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0149a-192">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="0149a-192">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




