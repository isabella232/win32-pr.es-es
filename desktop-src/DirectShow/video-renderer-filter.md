---
description: Filtro de representador de vídeo
ms.assetid: 7719ed9d-e3b9-4c84-b587-4e120b5cabf8
title: Filtro de representador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71e72375a43a57ce94b38d01f48abba9309e603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275806"
---
# <a name="video-renderer-filter"></a>Filtro de representador de vídeo

El filtro de representador de vídeo es un representador de vídeo sólido y multiuso.

> [!Note]  
> En Windows XP y versiones posteriores, el representador de vídeo predeterminado es el [filtro de representador de combinación de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7). Las opciones VMR-7 y representador de vídeo tienen el nombre descriptivo "representador de vídeo". En las plataformas anteriores, el representador de vídeo es el representador predeterminado. Vea [elección del representador adecuado](choosing-the-right-renderer.md).

 

El representador de vídeo utiliza DirectDraw y superficies superpuestas, si la tarjeta de vídeo las admite. Filter Graph Manager expone la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , que permite a las aplicaciones establecer y recuperar propiedades en el representador de vídeo. Con las tarjetas de vídeo más recientes, el representador de vídeo admite la representación a pantalla completa. De lo contrario, el administrador de gráficos de filtros cambia automáticamente al filtro de [representador de pantalla completa](full-screen-renderer-filter.md) para el modo de pantalla completa. Consulte [**IVideoWindow::p UT \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode) para obtener más información.

-   \[! Aún\]  
    > Normalmente, la ventana de vídeo de este filtro procesa los mensajes en un subproceso de trabajo creado por el administrador de gráficos de filtro. Sin embargo, si una aplicación crea directamente el filtro mediante **CoCreateInstance**, la ventana de vídeo procesa los mensajes en el subproceso de la aplicación. En ese caso, el subproceso de la aplicación debe tener un bucle de mensajes para enviar mensajes a la ventana de vídeo. Además, el subproceso no debe salir hasta la última llamada de **versión** al representador de vídeo, que se produce cuando se cierra el administrador de gráficos de filtro. De lo contrario, la aplicación podría bloquearse.

     



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2), [**IDirectDrawVideo**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo), [**IKsPropertySet**](ikspropertyset.md), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) |
| Tipos de medios de anclaje de entrada                    | Formatos de vídeo sin comprimir.                                                                                                                                                                                                                                                                                                                                                                              |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                           |
| Tipos de medios de anclaje de salida                   | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| Interfaces de clavija de salida                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                          |
| Identificador CLSID                             | Videoprocesador CLSID \_                                                                                                                                                                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                                                                                                                                                                                                                                                                        |
| Executable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                                               |
| [Fundament](merit.md)                       | Windows XP y versiones posteriores: el mérito no es **\_ probable**                                                                                                                                                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

En la versión de depuración de Quartz.dll, si el \_ nivel de depuración de seguimiento de registros se establece en 5 o superior, el representador de vídeo muestra las marcas de tiempo de cada fotograma en la ventana de vídeo. Estos números no aparecen en la versión comercial de la DLL. Para obtener más información, vea [funciones de salida de depuración](debug-output-functions.md).

Los siguientes comentarios están destinados a los desarrolladores de filtros:

El representador de vídeo acepta formatos YUV si la tarjeta gráfica de vídeo admite superficies de superposición YUV. La primera vez que se conecta al filtro de nivel superior, sin embargo, el representador de vídeo requiere un formato RGB que coincida con la profundidad de color de la configuración del monitor actual. Por ejemplo, si la configuración de pantalla actual es color de 24 bits, el filtro de nivel superior debe ser capaz de proporcionar vídeo RGB de 24 bits. Cuando el gráfico de filtro cambia a un estado de la continuación, el representador de vídeo negocia un cambio de formato dinámico en el espacio de colores de YUV adecuado.

Al conectarse con un tipo RGB, el representador de vídeo garantiza que puede usar GDI en caso de que DirectDraw no esté disponible. Cambiará a GDI si otra aplicación está usando la memoria de vídeo, si el rectángulo de vídeo abarca dos monitores en un sistema de varios monitores, o si el rectángulo de vídeo está completamente oculto en otra ventana.

> [!Note]  
> El representador de mezcla de vídeo no realiza este tipo de cambio de formato dinámico y no requiere un tipo de medio RGB, porque nunca utiliza GDI para la representación.

 

Para negociar un cambio de formato, el representador de vídeo llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) con el nuevo tipo de archivo multimedia. Si el filtro de nivel superior devuelve S \_ correcto, el representador de vídeo conecta el nuevo medio a la siguiente muestra. El filtro de nivel superior debe llamar a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) en cada ejemplo. Si **GetMediaType** devuelve un valor distinto de **null** , indica un cambio de formato y el filtro de nivel superior debe responder mediante el cambio de los tipos de salida. (No cambie los tipos en el método **QueryAccept** ). El filtro de nivel superior debe aceptar al menos los tipos RGB principales y, idealmente, debe admitir los tipos YUV comunes. Durante el streaming, el representador de vídeo puede alternar entre los tipos YUV y RGB cualquier número de veces. El representador de vídeo no acepta los cambios de formato dinámico iniciados por el filtro de nivel superior.

Cuando el representador de vídeo se dibuja en una superficie superpuesta de DirectDraw, asigna un solo búfer para su PIN de entrada. Si el filtro de nivel superior intenta forzar una conexión con varios búferes, el representador de vídeo no podrá usar la superficie de superposición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



