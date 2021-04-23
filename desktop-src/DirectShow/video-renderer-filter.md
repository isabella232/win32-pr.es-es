---
description: Filtro de representador de vídeo
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtro de representador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca3becb4fbdbb52a9968481aade07d14d963828
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908423"
---
# <a name="video-renderer-filter"></a>Filtro de representador de vídeo

El filtro Video Renderer es un representador de vídeo sólido y de uso general.

> [!Note]  
> En Windows XP y versiones posteriores, el representador de vídeo predeterminado es el filtro de representador de mezcla de vídeo [7](video-mixing-renderer-filter-7.md) (VMR-7). El VMR-7 y el representador de vídeo tienen el nombre descriptivo "Representador de vídeo". En plataformas anteriores, el representador de vídeo es el representador predeterminado. Consulte [Elección del representador derecho.](choosing-the-right-renderer.md)

 

El representador de vídeo usa DirectDraw y superficies superpuestas, si la tarjeta de vídeo las admite. El Administrador de gráficos de filtros expone la [**interfaz IVideoWindow,**](/windows/desktop/api/Control/nn-control-ivideowindow) que permite a las aplicaciones establecer y recuperar propiedades en el representador de vídeo. Con las tarjetas de vídeo más recientes, el representador de vídeo admite la representación a pantalla completa. De lo contrario, el Administrador de gráficos de filtros cambia automáticamente al [filtro Representador de pantalla](full-screen-renderer-filter.md) completa para el modo de pantalla completa. Vea [**IVideoWindow::p ut \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) para obtener más información.

-   \[! Importante\]  
    > Normalmente, la ventana de vídeo de este filtro procesa mensajes en un subproceso de trabajo creado por el Administrador de gráficos de filtros. Howerver, si una aplicación crea directamente el filtro mediante **CoCreateInstance**, la ventana de vídeo procesa los mensajes en el subproceso de la aplicación. En ese caso, el subproceso de aplicación debe tener un bucle de mensajes para enviar mensajes a la ventana de vídeo. Además, el subproceso no debe salir hasta la última llamada **de** versión al representador de vídeo, que se produce cuando se cierra el Administrador de gráficos de filtros. De lo contrario, la aplicación podría interbloqueo.

     



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) [**IBasicVideo2,**](/windows/desktop/api/Control/nn-control-ibasicvideo2) [**IDirectDrawVideo,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo) [**IKsPropertySet,**](ikspropertyset.md) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IQualProp,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Tipos de medios de pin de entrada                    | Formatos de vídeo sin comprimir.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IOverlay,**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Tipos de medios de pin de salida                   | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfaces de pin de salida                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| Filtrar CLSID                             | Representador de \_ vídeo CLSID                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                                                                                                                                                                                                                                                                        |
| Executable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Mérito](merit.md)                       | Windows XP y versiones posteriores: **UNLIKELY \_**                                                                                                                                                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentarios

En la versión de depuración de Quartz.dll, si el nivel de depuración LOG TRACE está establecido en 5 o superior, el representador de vídeo muestra las marcas de tiempo de cada fotograma en la ventana \_ de vídeo. Estos números no aparecen en la versión comercial del archivo DLL. Para obtener más información, vea [Depurar funciones de salida](debug-output-functions.md).

Los comentarios siguientes están destinados a los desarrolladores de filtros:

El representador de vídeo acepta formatos YUV si la tarjeta gráfica de vídeo admite superficies superpuestas de YUV. Sin embargo, la primera vez que se conecta al filtro ascendente, el representador de vídeo requiere un formato RGB que coincida con la profundidad de color de la configuración actual del monitor. Por ejemplo, si la configuración de pantalla actual es de color de 24 bits, el filtro ascendente debe ser capaz de proporcionar vídeo RGB de 24 bits. Cuando el gráfico de filtro cambia a un estado de ejecución, el representador de vídeo negocia un cambio de formato dinámico en el espacio de color YUV adecuado.

Al conectarse con un tipo RGB, el representador de vídeo garantiza que puede usar GDI en caso de que DirectDraw no esté disponible. Cambiará a GDI si otra aplicación usa la memoria de vídeo, si el rectángulo de vídeo se desfila dos monitores en un sistema de varios monitores o si el rectángulo de vídeo está completamente oculto por otra ventana.

> [!Note]  
> El representador de mezcla de vídeo no realiza este tipo de cambio de formato dinámico y no requiere un tipo de medio RGB, ya que nunca usa GDI para la representación.

 

Para negociar un cambio de formato, el representador de vídeo llama a [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) con el nuevo tipo de medio. Si el filtro ascendente devuelve S \_ OK, el representador de vídeo asocia el nuevo medio al ejemplo siguiente. El filtro ascendente debe llamar a [**IMediaSample::GetMediaType en**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) cada ejemplo. Si **GetMediaType** devuelve un valor distinto de **NULL,** indica un cambio de formato y el filtro ascendente debe responder cambiando los tipos de salida. (No cambie los tipos en el **método QueryAccept).** El filtro ascendente debe aceptar al menos los tipos RGB principales e idealmente debe admitir los tipos YUV comunes. Durante el streaming, el representador de vídeo puede cambiar entre los tipos YUV y RGB varias veces. El representador de vídeo no acepta cambios de formato dinámico iniciados por el filtro ascendente.

Cuando el representador de vídeo se dibuja en una superficie superpuesta de DirectDraw, asigna un único búfer para su pin de entrada. Si el filtro ascendente intenta forzar una conexión mediante varios búferes, el representador de vídeo no podrá usar la superficie superpuesta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



