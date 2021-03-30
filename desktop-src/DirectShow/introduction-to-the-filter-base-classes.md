---
description: Introducción a las clases base de filtro
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Introducción a las clases base de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44c104d8fe155a7c9f0edba72770a508c8ec43d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422738"
---
# <a name="introduction-to-the-filter-base-classes"></a>Introducción a las clases base de filtro

En este artículo se describe la biblioteca de clases base de Microsoft DirectShow. Esta biblioteca está pensada para los programadores de filtros, pero los escritores de aplicaciones podrían encontrar útiles algunas de las clases auxiliares y las utilidades de depuración. No obstante, la biblioteca de clases base no es necesaria para la programación con DirectShow.

En las secciones siguientes se resumen las clases base más importantes de la biblioteca.

**Clases de objetos COM**

Las clases siguientes admiten la creación de objetos COM:



| Clase                              | Descripción                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | Clase de objeto base.                     |
| [**CUnknown**](cunknown.md)       | Implementa la interfaz **IUnknown** . |



 

La mayoría de las clases de DirectShow derivan de **CBaseObject**. Esta clase proporciona ayuda para la depuración manteniendo un recuento de todos los objetos activos en el archivo DLL en tiempo de ejecución. En las compilaciones de depuración, el archivo DLL valida si se descarga mientras el recuento de objetos es mayor que cero. Esto facilita el seguimiento de las fugas producidas por problemas de recuento de referencias.

Todas las clases base que admiten interfaces COM derivan de **CUnknown**, que hereda **CBaseObject**. La clase **CUnknown** admite el recuento de referencias, **QueryInterface** y agregación. Para obtener más información, vea [How to implement IUnknown](how-to-implement-iunknown.md).

**Filtrar y anclar clases**

Las siguientes clases admiten la creación de objetos de filtro y anclaje de DirectShow:



| Clase                                    | Descripción                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | Clase base para los filtros. Implementa la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .                                                                            |
| [**CBasePin**](cbasepin.md)             | Clase base para los pin. Implementa las interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) y [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | Clase base para los pin de entrada que usan el transporte de memoria local. Implementa la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Esta clase se deriva de **CBasePin**. |
| [**CBaseOutputPin**](cbaseoutputpin.md) | Clase base para los clavijas de salida que usan conexiones **IMemInputPin** . Esta clase se deriva de **CBasePin**.                                                         |



 

Las clases siguientes son útiles para crear tipos de filtros más especializados:



| Clase                                                  | Descripción                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Clase base para los filtros de origen. Esta clase está diseñada para crear orígenes de inserciones. No es adecuado para orígenes de extracción, como lectores de archivos. Para crear clavijas de salida para esta clase, use la clase [**CSourceStream**](csourcestream.md) .                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | Clase base para los filtros de transformación. Esta clase realiza una copia de los datos. Los pin de esta clase son [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin**](ctransformoutputpin.md).                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | Clase base para los filtros de transformación que no copian datos. Esta clase realiza el procesamiento de datos directamente en los datos de entrada antes de pasarlo a nivel inferior. Los pin de esta clase son [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) y [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md). |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | Clase base para los filtros de transformación de vídeo. Esta clase deriva de **CTransformFilter** y agrega compatibilidad con el control de calidad.                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | Clase base para los filtros de representador. El PIN de entrada de esta clase es [**CRendererInputPin**](crendererinputpin.md).                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | Clase base para los representadores de vídeo. Esta clase se deriva de **CBaseRenderer**.                                                                                                                                                                                                                                |



 

Para usar estas clases, debe derivar su propia clase y escribir código para admitir la funcionalidad específica del filtro. Cuanto más especializado sea la clase base, menos código tendrá que escribir en la clase derivada.

**Objetos auxiliares**

Las siguientes clases implementan objetos auxiliares que los filtros y los pin usan. La mayoría de estas clases se pueden usar sin derivar nuevas clases de ellas:



| Clase                                              | Descripción                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | Objeto auxiliar para clavijas de entrada en filtros de analizador. Admite conexiones [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) con orígenes de extracción.                                       |
| [**COutputQueue**](coutputqueue.md)               | Objeto auxiliar para los pines de salida que ponen en cola ejemplos para la entrega en un subproceso de trabajo.                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | Objeto de ayuda para implementar búsquedas en un filtro de origen con exactamente un PIN de salida. (Esta clase no está diseñada para los filtros con varios PIN, como los analizadores). |
| [**CEnumPins**](cenumpins.md)                     | Objeto enumerador para enumerar los pin de un filtro. Implementa la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Objeto enumerador para enumerar los tipos de medios preferidos en un PIN. Implementa la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .                             |
| [**CMemAllocator**](cmemallocator.md)             | Objeto de asignador de memoria. Implementa la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .                                                                          |
| [**CMediaSample**](cmediasample.md)               | Objeto de ejemplo multimedia. Implementa la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) .                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | Clase base para los relojes de referencia. Implementa la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) .                                                              |
| [**CMediaType**](cmediatype.md)                   | Objeto auxiliar para manipular estructuras de [**\_ \_ tipo medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .                                                                                |



 

 

 



