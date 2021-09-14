---
description: Filtro de representador de mezcla de vídeo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro de representador de mezcla de vídeo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e20418aad6b9648835665fff98f894eeed1386
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272932"
---
# <a name="video-mixing-renderer-filter-9"></a>Filtro de representador de mezcla de vídeo 9

En DirectX 9, el filtro Video Mixing Renderer 9 (VMR-9) ofrece funcionalidades avanzadas de representación de vídeo en todas las plataformas compatibles con DirectX. Está totalmente integrado con funcionalidades 3D de DirectX 9. Por ejemplo, puede agregar fácilmente vídeo a juegos y otros entornos 3D o transformar imágenes de vídeo mediante los sombreadores de píxeles de Direct3D y otros efectos.

Este filtro no admite puertos de vídeo.

Para mantener la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema. Para usar este filtro, agrégrelo al gráfico de filtros explícitamente y configúrelo antes de conectar cualquiera de sus pines de entrada. VMR-9 usa su propio conjunto de interfaces, estructuras y enumeraciones, que no siempre son idénticos a los tipos de datos correspondientes usados con VMR-7.

VMR-9 admite hasta 16 monitores.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | VMR-9 admite varios modos de representación distintos. Admite un conjunto diferente de interfaces en función del modo de representación:<br /><ul><li>Todos los modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualityControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li><li>Modo sin representación: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li><li>Modo de ventana: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2,</strong></a> <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow,</strong></a> <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li><li>Modo sin ventana: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li></ul>Para establecer el modo de representación, llame <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>a IVMRFilterConfig9::SetRenderingMode</strong></a>. Para más información, consulte <a href="vmr-modes-of-operation.md">Modos de operación de VMR.</a><br /> | 
| Tipos de medios de pin de entrada | Los pines de entrada se conectarán con cualquier tipo compatible con el hardware de vídeo subyacente. | 
| Interfaces de pin de entrada | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a> | 
| Tipos de medios de pin de salida | No aplicable. | 
| Interfaces de pin de salida | No aplicable. | 
| Filtrar CLSID | CLSID_VideoMixingRenderer9 | 
| CLSID de la página de propiedades | N/D | 
| Executable | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

Una aplicación puede proporcionar un objeto allocator-presenter personalizado que expone las interfaces siguientes:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)

Para obtener más información sobre los asignadores y presentadores personalizados, vea Proporcionar un Allocator-Presenter [personalizado para VMR-9.](supplying-a-custom-allocator-presenter-for-vmr-9.md)

Una aplicación también puede proporcionar un compositor de complementos personalizado que expone la siguiente interfaz:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Para configurar vmr con un compositor personalizado, llame a [**IVMRFilterConfig9::SetImageCompositor.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




