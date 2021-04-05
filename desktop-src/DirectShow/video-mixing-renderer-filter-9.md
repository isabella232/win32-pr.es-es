---
description: Filtro de representador de mezcla de vídeo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro de representador de mezcla de vídeo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815254"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="78091-103">Filtro de representador de mezcla de vídeo 9</span><span class="sxs-lookup"><span data-stu-id="78091-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="78091-104">En DirectX 9, el filtro de mezclador de vídeo 9 (VMR-9) ofrece capacidades de representación de vídeo avanzadas en todas las plataformas compatibles con DirectX.</span><span class="sxs-lookup"><span data-stu-id="78091-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="78091-105">Está totalmente integrado con las capacidades 3D de DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="78091-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="78091-106">Por ejemplo, puede Agregar vídeo fácilmente a juegos y otros entornos 3D, o bien transformar imágenes de vídeo con los sombreadores de píxeles de Direct3D y otros efectos.</span><span class="sxs-lookup"><span data-stu-id="78091-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="78091-107">Este filtro no admite puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="78091-107">This filter does not support video ports.</span></span>

<span data-ttu-id="78091-108">Para mantener la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema.</span><span class="sxs-lookup"><span data-stu-id="78091-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="78091-109">Para usar este filtro, agréguelo al gráfico de filtros explícitamente y configúrelo antes de conectar cualquiera de sus clavijas de entrada.</span><span class="sxs-lookup"><span data-stu-id="78091-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="78091-110">VMR-9 usa su propio conjunto de interfaces, estructuras y enumeraciones, que no son siempre idénticas a los tipos de datos correspondientes que se usan con VMR-7.</span><span class="sxs-lookup"><span data-stu-id="78091-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="78091-111">VMR-9 admite hasta 16 monitores.</span><span class="sxs-lookup"><span data-stu-id="78091-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78091-112">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="78091-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="78091-113">VMR-9 admite varios modos de representación distintos.</span><span class="sxs-lookup"><span data-stu-id="78091-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="78091-114">Admite un conjunto diferente de interfaces en función del modo de representación:</span><span class="sxs-lookup"><span data-stu-id="78091-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="78091-115">Todos los modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="78091-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="78091-116">Modo no representativo: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="78091-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="78091-117">Modo de ventana: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="78091-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="78091-118">Modo sin ventanas: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="78091-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="78091-119">Para establecer el modo de representación, llame a <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: SetRenderingMode</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="78091-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="78091-120">Para obtener más información, vea <a href="vmr-modes-of-operation.md">modos de funcionamiento de VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="78091-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78091-121">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="78091-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="78091-122">Los pin de entrada se conectarán con cualquier tipo compatible con el hardware de vídeo subyacente.</span><span class="sxs-lookup"><span data-stu-id="78091-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78091-123">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="78091-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="78091-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="78091-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78091-125">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="78091-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="78091-126">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="78091-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78091-127">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="78091-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="78091-128">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="78091-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78091-129">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="78091-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="78091-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="78091-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78091-131">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="78091-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="78091-132">N/D</span><span class="sxs-lookup"><span data-stu-id="78091-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78091-133">Executable</span><span class="sxs-lookup"><span data-stu-id="78091-133">Executable</span></span></td>
<td><span data-ttu-id="78091-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="78091-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78091-135"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="78091-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="78091-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="78091-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78091-137"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="78091-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="78091-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="78091-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="78091-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78091-139">Remarks</span></span>

<span data-ttu-id="78091-140">Una aplicación puede proporcionar un objeto de presentador personalizado que exponga las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="78091-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="78091-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="78091-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="78091-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="78091-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="78091-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="78091-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="78091-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="78091-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="78091-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="78091-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="78091-146">Para obtener más información acerca de los presentadores personalizados, consulte [suministro de un Allocator-Presenter personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="78091-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="78091-147">Una aplicación también puede proporcionar un compositor de complementos personalizado que exponga la interfaz siguiente:</span><span class="sxs-lookup"><span data-stu-id="78091-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="78091-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="78091-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="78091-149">Para configurar la VMR con un compositor personalizado, llame a [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="78091-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78091-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78091-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78091-151">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="78091-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="78091-152">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="78091-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




