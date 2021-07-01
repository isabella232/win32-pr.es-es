---
description: Filtro de representador de pantalla completa
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtro de representador de pantalla completa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d331ff6f31d1c985c7e255b23381a289931da60
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120480"
---
# <a name="full-screen-renderer-filter"></a>Filtro de representador de pantalla completa

El filtro Representador de pantalla completa proporciona representación de vídeo a pantalla completa en hardware anterior. Las tarjetas de vídeo más recientes pueden ampliar el vídeo de forma lo suficientemente eficaz como para que el representador de pantalla completa no sea necesario. Por lo tanto, el uso de este filtro está ahora en desuso.

No agregue manualmente este filtro al gráfico de filtros. Si una aplicación llama a [**IVideoWindow::p ut \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode), el Administrador de gráficos de filtros selecciona automáticamente el representador de vídeo adecuado para el modo de pantalla completa. La selección es transparente para la aplicación. Con las tarjetas de vídeo actuales, es poco probable que el Administrador de gráficos de filtros seleccione el representador de pantalla completa.



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFullScreenVideoEx,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Tipos de medios de pin de entrada                    | VÍDEO \_ MEDIATYPE, MEDIASUBTYPE \_ Null                                                                                                                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de pin de salida                   | No aplicable                                                                                                                                                                                                                                     |
| Interfaces de pin de salida                    | No aplicable                                                                                                                                                                                                                                     |
| Filtrar CLSID                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| CLSID de la página de propiedades                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| Executable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NO PROBABLE \_ QUE SE PRODUZCAN LOS CASO                                                                                                                                                                                                                                    |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

El representador de pantalla completa admite un conjunto estático de modos de presentación. Sin embargo, es posible que la tarjeta de vídeo del sistema del usuario no admita todos los modos. Para determinar si la tarjeta admite un modo determinado, llame al [**método IFullScreenVideoEx::IsModeAvailable.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) También puede deshabilitar un modo de presentación determinado mediante programación, llamando a [**IFullScreenVideoEx::SetEnabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled). El representador de pantalla completa admite actualmente los modos de presentación que se muestran en la tabla siguiente:



| Mode | Ancho | Alto | Profundidad en bits |
|------|-------|--------|-----------|
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1024  | 768    | 16        |
| 11   | 1024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1280  | 1024   | 16        |
| 15   | 1280  | 1024   | 8         |



 

(Todos los modos son RGB). Sin embargo, esta lista está sujeta a cambios. Use el [**método IFullScreenVideoEx::GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) para obtener información sobre los modos. El representador de pantalla completa siempre elige el modo de resolución más bajo disponible, limitado por una propiedad denominada factor de *clip*, que determina la cantidad del vídeo que el representador de pantalla completa puede recortar. Para obtener más información, [**vea IFullScreenVideoEx::GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Cuando la aplicación ejecuta o pausa el gráfico de filtros, el representador de pantalla completa cambia al modo de presentación elegido. Cuando se detiene el gráfico, el representador de pantalla completa restaura el modo de presentación original.

El representador de pantalla completa solo puede funcionar como la ventana activa en primer plano. Si el usuario cambia a otra aplicación, el representador de pantalla completa oculta el vídeo minimizando u ocultando la ventana de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



