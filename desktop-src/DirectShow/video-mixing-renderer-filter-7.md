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
# <a name="video-mixing-renderer-filter-7"></a>Filtro de representador de mezcla de vídeo 7

Este tema se aplica a Windows XP o posterior.

En Windows XP y versiones posteriores, el representador de vídeo 7 (VMR-7) es el representador de vídeo predeterminado. Se denomina VMR-7 porque internamente usa DirectDraw 7. En DirectX 9, un filtro similar, pero independiente, de VMR-9, está disponible para la redistribución en sistemas que no son XP. VMR-9 usa Direct3D 9.

> [!Note]  
> VMR está disponible en Windows XP y versiones posteriores. No está disponible a través de DirectX Redistributable o en versiones anteriores de Windows. En la mayoría de los escenarios, las aplicaciones deben usar el [representador de combinación de vídeo 9](video-mixing-renderer-filter-9.md).

 

Las características de VMR incluyen:

-   Combinación alfa verdadera de hasta 16 flujos de entrada
-   Acceso a la imagen compuesta antes de que se represente
-   Un modelo de complemento que permite a terceros implementar efectos de vídeo personalizados.
-   Compatibilidad con hasta 15 monitores.

Durante la creación de gráficos en Windows XP y versiones posteriores, el administrador de gráficos de filtros no usará los filtros de representador de vídeo más antiguo ni los de la superposición, a menos que la aplicación los cree explícitamente y agregue al gráfico.

Para obtener más información, vea [usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td>Todos los modos:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
</ul>
Modo de ventana:<br/>
<ul>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modo sin ventanas:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modo no representativo:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
</ul>
Modo de mezclador:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
</ul>
Para obtener información sobre los distintos modos de VMR-7, vea <a href="vmr-modes-of-operation.md">modos de funcionamiento de VMR</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_VideoSubtype: depende del hardware de gráficos. Debe ser un vídeo sin comprimir.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (ver comentarios)</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li>
</ul></td>
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
<td>Hay dos CLSID asociados a este filtro:
<ul>
<li>CLSID_VideoMixingRenderer: crea la VMR-7. Si no hay suficientes recursos del sistema para crear el VMR-7, se produce un error en la llamada a <strong>CoCreateInstance</strong> .</li>
<li>CLSID_VideoRendererDefault: crea la VMR-7 si hay recursos del sistema disponibles, o bien crea el filtro de <a href="video-renderer-filter.md">representador de vídeo</a> antiguo.</li>
</ul>
Use CLSID_VideoMixingRenderer si necesita las capacidades específicas de VMR-7. De lo contrario, use CLSID_VideoRendererDefault, que es casi seguro que no se puede producir un error, porque recurre al filtro de representador de vídeo antiguo.<br/></td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>No es aplicable.</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

El PIN de entrada expone la interfaz **IOverlay** solo cuando el filtro VMR-7 está en modo de ventana. El único método **IOverlay** que implementa el PIN es **GetWindowHandle**, que permite que una aplicación obtenga un identificador de la ventana de vídeo del filtro. Todos los demás métodos de **IOverlay** devuelven E \_ NOTIMPL. En el modo sin ventanas, el filtro no crea una ventana de vídeo, por lo que el PIN no expone la interfaz.

Una aplicación puede proporcionar un objeto de presentador personalizado que exponga las siguientes interfaces:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)

Para obtener más información acerca de los presentadores personalizados, consulte [suministro de un Allocator-Presenter personalizado para VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Una aplicación también puede proporcionar un compositor de complementos personalizado que exponga la interfaz siguiente:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Para configurar la VMR con un compositor personalizado, llame a [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 




