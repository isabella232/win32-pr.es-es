---
description: Filtro de representador de mezcla de vídeo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro de representador de mezcla de vídeo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac39dfeab90fe97085c97b3a767f06d348a0f02
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466042"
---
# <a name="video-mixing-renderer-filter-7"></a>Filtro de representador de mezcla de vídeo 7

Este tema se aplica a Windows XP o posterior.

En Windows XP y versiones posteriores, el representador de mezcla de vídeo 7 (VMR-7) es el representador de vídeo predeterminado. Se denomina VMR-7 porque internamente usa DirectDraw 7. En DirectX 9, hay disponible un filtro similar pero independiente, VMR-9, para la redistribución en sistemas que no son XP. VMR-9 usa Direct3D 9.

> [!Note]  
> VmR está disponible en Windows XP y versiones posteriores. No está disponible a través de DirectX redistribuible ni en versiones anteriores de Windows. En la mayoría de los escenarios, las aplicaciones deben usar [el representador de mezcla de vídeo 9](video-mixing-renderer-filter-9.md).

 

Entre las características de VMR se incluyen las siguientes:

-   Mezcla alfa verdadera de hasta 16 flujos de entrada
-   Acceso a la imagen compuesta antes de representarla
-   Un modelo de complemento que permite a terceros implementar efectos de vídeo personalizados.
-   Compatibilidad con hasta 15 monitores.

Durante la creación de grafos en Windows XP y versiones posteriores, el Administrador de filtros de Graph no usará los filtros antiguos representador de vídeo o superposición Mixer, a menos que la aplicación los cree explícitamente y los agrega al gráfico.

Para obtener más información, [vea Usar el representador de mezcla de vídeo.](using-the-video-mixing-renderer.md)




| | | Filtrar interfaces | Todos los modos:<ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li></ul>Modo de ventana:<br /><ul><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modo sin ventanas:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li></ul>Modo sin representación:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li></ul>Mixer modo de configuración:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li></ul>Para obtener información sobre los distintos modos de VMR-7, consulte <a href="vmr-modes-of-operation.md">Modos de funcionamiento de VMR.</a><br /> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_VideoSubtype: depende del hardware gráfico. Debe ser un vídeo sin comprimir.<br /> | | Interfaces de pin de entrada | <ul><li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (vea Comentarios)</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li></ul> | | Tipos de medios de pin de salida | No aplicable. | | Interfaces de pin de salida | No aplicable. | | Filtrar clsid | Hay dos CLSID asociados a este filtro:<ul><li>CLSID_VideoMixingRenderer: crea vmr-7. Si no hay suficientes recursos del sistema para crear vmr-7, se produce un error en la <strong>llamada a CoCreateInstance.</strong></li><li>CLSID_VideoRendererDefault: crea vmr-7 si hay recursos del sistema disponibles o, de lo contrario, se crea el filtro <a href="video-renderer-filter.md">de representador de</a> vídeo antiguo.</li></ul>Use CLSID_VideoMixingRenderer si necesita las funcionalidades específicas de VMR-7. De lo contrario, CLSID_VideoRendererDefault, que es casi seguro que no se producirá un error, porque vuelve al filtro antiguo representador de vídeo.<br /> | | Página de propiedades CLSID | No aplicable. | | Archivos ejecutables | Quartz.dll | | <a href="merit.md">|</a> MERIT_PREFERRED + 1 | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

El pin de entrada expone la **interfaz IOverlay** solo cuando el filtro VMR-7 está en modo de ventana. El único **método de IOverlay** que implementa el pin es **GetWindowHandle,** que permite a una aplicación obtener un identificador para la ventana de vídeo del filtro. Todos los demás **métodos de IOverlay** devuelven E \_ NOTIMPL. En el modo sin ventanas, el filtro no crea una ventana de vídeo, por lo que el pin no expone la interfaz.

Una aplicación puede proporcionar un objeto allocator-presenter personalizado que expone las interfaces siguientes:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)

Para obtener más información sobre los asignadores-presentadores personalizados, vea Suministro de un Allocator-Presenter personalizado [para VMR-7.](supplying-a-custom-allocator-presenter-for-vmr-7.md)

Una aplicación también puede proporcionar un compositor de complemento personalizado que expone la siguiente interfaz:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Para configurar vmr con un compositor personalizado, llame a [**IVMRFilterConfig::SetImageCompositor.**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




