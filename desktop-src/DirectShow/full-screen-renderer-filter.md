---
description: Filtro de representador de pantalla completa
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtro de representador de pantalla completa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d580442887896f271b0f5b7fea5f7a33553f53f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677053"
---
# <a name="full-screen-renderer-filter"></a>Filtro de representador de pantalla completa

El filtro de representador de pantalla completa proporciona representación de vídeo a pantalla completa en hardware más antiguo. Las tarjetas de vídeo más recientes pueden ampliar el vídeo de la manera más eficaz que el representador de pantalla completa no es necesario. Por lo tanto, el uso de este filtro ahora está en desuso.

No agregue manualmente este filtro al gráfico de filtros. Si una aplicación llama a [**IVideoWindow::p UT \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode), Filter Graph Manager selecciona automáticamente el representador de vídeo adecuado para el modo de pantalla completa. La selección es transparente para la aplicación. Con las tarjetas de vídeo actuales, no es probable que el administrador de gráficos de filtro seleccione el representador de pantalla completa.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFullScreenVideoEx**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de anclaje de salida                   | No aplicable                                                                                                                                                                                                                                     |
| Interfaces de clavija de salida                    | No aplicable                                                                                                                                                                                                                                     |
| Identificador CLSID                             | CLSID \_ ModexRenderer                                                                                                                                                                                                                               |
| CLSID de la página de propiedades                      | CLSID \_ ModexProperties                                                                                                                                                                                                                             |
| Executable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                                                                                                                                                                    |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

El representador de pantalla completa admite un conjunto estático de modos de presentación. No obstante, es posible que la tarjeta de vídeo del sistema del usuario no admita todos los modos. Para determinar si la tarjeta admite un modo determinado, llame al método [**IFullScreenVideoEx:: IsModeAvailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) . También puede deshabilitar un modo de presentación determinado mediante programación llamando a [**IFullScreenVideoEx:: setEnabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled). El representador de pantalla completa admite actualmente los modos de presentación que se muestran en la tabla siguiente:



|      |       |        |           |
|------|-------|--------|-----------|
| Mode | Ancho | Alto | Profundidad de bits |
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



 

(Todos los modos son RGB). Sin embargo, esta lista está sujeta a cambios. Use el método [**IFullScreenVideoEx:: GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) para obtener información sobre los modos. El representador de pantalla completa siempre elige el modo de resolución inferior disponible, limitado por una propiedad denominada *factor de recorte*, que determina la cantidad de vídeo que se permite recortar en el representador de pantalla completa. Para obtener más información, vea [**IFullScreenVideoEx:: GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Cuando la aplicación se ejecuta o pausa el gráfico de filtro, el representador de pantalla completa cambia al modo de presentación elegido. Cuando el gráfico se detiene, el representador de pantalla completa restaura el modo de presentación original.

El representador de pantalla completa solo puede funcionar como la ventana activa en primer plano. Si el usuario cambia a otra aplicación, el representador de pantalla completa oculta el vídeo al minimizar u ocultar la ventana de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



