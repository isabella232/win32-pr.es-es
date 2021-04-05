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
# <a name="video-mixing-renderer-filter-9"></a>Filtro de representador de mezcla de vídeo 9

En DirectX 9, el filtro de mezclador de vídeo 9 (VMR-9) ofrece capacidades de representación de vídeo avanzadas en todas las plataformas compatibles con DirectX. Está totalmente integrado con las capacidades 3D de DirectX 9. Por ejemplo, puede Agregar vídeo fácilmente a juegos y otros entornos 3D, o bien transformar imágenes de vídeo con los sombreadores de píxeles de Direct3D y otros efectos.

Este filtro no admite puertos de vídeo.

Para mantener la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema. Para usar este filtro, agréguelo al gráfico de filtros explícitamente y configúrelo antes de conectar cualquiera de sus clavijas de entrada. VMR-9 usa su propio conjunto de interfaces, estructuras y enumeraciones, que no son siempre idénticas a los tipos de datos correspondientes que se usan con VMR-7.

VMR-9 admite hasta 16 monitores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td>VMR-9 admite varios modos de representación distintos. Admite un conjunto diferente de interfaces en función del modo de representación:<br/>
<ul>
<li>Todos los modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li>Modo no representativo: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li>Modo de ventana: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li>Modo sin ventanas: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul>
Para establecer el modo de representación, llame a <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: SetRenderingMode</strong></a>. Para obtener más información, vea <a href="vmr-modes-of-operation.md">modos de funcionamiento de VMR</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Los pin de entrada se conectarán con cualquier tipo compatible con el hardware de vídeo subyacente.</td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_VideoMixingRenderer9</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>N/D</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Una aplicación puede proporcionar un objeto de presentador personalizado que exponga las siguientes interfaces:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)

Para obtener más información acerca de los presentadores personalizados, consulte [suministro de un Allocator-Presenter personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Una aplicación también puede proporcionar un compositor de complementos personalizado que exponga la interfaz siguiente:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Para configurar la VMR con un compositor personalizado, llame a [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 




