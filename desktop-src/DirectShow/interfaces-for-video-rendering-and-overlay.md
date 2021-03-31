---
description: Interfaces para la representación y superposición de vídeo
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Interfaces para la representación y superposición de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806476"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a><span data-ttu-id="02dfd-103">Interfaces para la representación y superposición de vídeo</span><span class="sxs-lookup"><span data-stu-id="02dfd-103">Interfaces for Video Rendering and Overlay</span></span>

<span data-ttu-id="02dfd-104">Estas interfaces admiten el control de aplicaciones a través de la representación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-104">These interfaces support application control over video rendering.</span></span> <span data-ttu-id="02dfd-105">Tenga en cuenta que algunas de estas interfaces ahora están en desuso, ya que el filtro de representador de combinación de vídeo proporciona un control superior de representación y superposición.</span><span class="sxs-lookup"><span data-stu-id="02dfd-105">Note that some of these interfaces are now deprecated, because the Video Mixing Renderer filter provides superior rendering and overlay control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02dfd-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="02dfd-106">Interface</span></span></th>
<th><span data-ttu-id="02dfd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="02dfd-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02dfd-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-108"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-109">Proporciona acceso a la información y a la configuración de los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="02dfd-109">Provides access to closed-captioned information and settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-111">Aplique efectos superpuestos a la superficie de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-111">Apply overlay effects to the video surface.</span></span> <span data-ttu-id="02dfd-112">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-112">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-113"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-114">Controle el modo en que DirectShow escala una imagen de vídeo si la ventana de vídeo es más pequeña que el tamaño nativo del vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-114">Control how DirectShow scales a video image if the video window is smaller than the native size of the video.</span></span> <span data-ttu-id="02dfd-115">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-115">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-116"><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-117">Establecer propiedades de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-117">Set video properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-118"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-119">Representar vídeo en el modo de pantalla completa de Microsoft DirectDraw exclusivo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-119">Render video in Microsoft DirectDraw exclusive full-screen mode.</span></span> <span data-ttu-id="02dfd-120">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-120">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-121"><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-122">Interfaz de devolución de llamada para recibir notificaciones sobre los cambios en la posición, el tamaño y la visibilidad de la superposición.</span><span class="sxs-lookup"><span data-stu-id="02dfd-122">Callback interface to receive notification about changes to the overlay position, size, and visibility.</span></span> <span data-ttu-id="02dfd-123">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-123">(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-124"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-125">Deshabilitar las funcionalidades de DirectDraw especificadas.</span><span class="sxs-lookup"><span data-stu-id="02dfd-125">Disable specified DirectDraw capabilities.</span></span> <span data-ttu-id="02dfd-126">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-126">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-127"><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-128">Acceder a una superficie de DirectDraw asignada por el filtro de <a href="overlay-mixer-filter.md">mezclador de superposición</a> . (Desusado).</span><span class="sxs-lookup"><span data-stu-id="02dfd-128">Access a DirectDraw surface allocated by the <a href="overlay-mixer-filter.md">Overlay Mixer</a> filter.(Deprecated.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-129"><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-130">Implementado en el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="02dfd-130">Implemented on the Overlay Mixer.</span></span> <span data-ttu-id="02dfd-131">Permite a los clientes sin ventanas, como los controles de® ActiveX, obtener y establecer las propiedades del rectángulo de vídeo y avisar al filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="02dfd-131">Enables windowless clients such as ActiveX® controls to get and set properties of the video rectangle and advise the filter of events.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-132"><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-133">Implementado por clientes sin ventanas y llamado por el mezclador de superposición para enviar notificaciones de eventos que afectan al rectángulo de presentación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-133">Implemented by windowless clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-134"><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-135">Establecer controles de color de vídeo en el filtro de mezclador de superposición al mezclar varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-135">Set video color controls on the Overlay Mixer filter when mixing multiple video streams.</span></span> <span data-ttu-id="02dfd-136">(En desuso).</span><span class="sxs-lookup"><span data-stu-id="02dfd-136">(Deprecated.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02dfd-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-137"><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-138">Consulte un representador de vídeo para obtener información sobre el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="02dfd-138">Query a video renderer for performance information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02dfd-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-139"><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></span></span></td>
<td><span data-ttu-id="02dfd-140">Establecer propiedades de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02dfd-140">Set video window properties.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="02dfd-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-141"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-142"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-143"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-144"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-145"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-146"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-147"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-148"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-149"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-150"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-151"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-152"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-153"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-154"><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="02dfd-155">Vídeo que mezcla el representador 9 interfaces.</span><span class="sxs-lookup"><span data-stu-id="02dfd-155">Video Mixing Renderer 9 interfaces.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="02dfd-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-156"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-157"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-158"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-159"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-160"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-161"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-162"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-163"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-164"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-165"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></span></span></li>
<li><span data-ttu-id="02dfd-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="02dfd-166"><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="02dfd-167">Vídeo en el que se combinan las interfaces del representador 7.</span><span class="sxs-lookup"><span data-stu-id="02dfd-167">Video Mixing Renderer 7 interfaces.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="02dfd-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02dfd-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02dfd-169">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="02dfd-169">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



