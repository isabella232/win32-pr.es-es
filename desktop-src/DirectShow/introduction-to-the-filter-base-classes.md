---
description: Introducción a las clases base de filtro
ms.assetid: db6324d7-1914-44a8-a202-dff752b61c1a
title: Introducción a las clases base de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c0682a5ba9f6a051506911cf143474d9958f1caa926464d9a4c236366e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952564"
---
# <a name="introduction-to-the-filter-base-classes"></a>Introducción a las clases base de filtro

En este artículo se describe la biblioteca de DirectShow base de Microsoft. Esta biblioteca está pensada para desarrolladores de filtros, pero los escritores de aplicaciones pueden encontrar útiles algunas de las clases auxiliares y utilidades de depuración. Sin embargo, la biblioteca de clases base no es necesaria DirectShow programación.

En las secciones siguientes se resumen las clases base más importantes de la biblioteca.

**Clases de objetos COM**

Las clases siguientes admiten la creación de objetos COM:



| Clase                              | Descripción                            |
|------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject.md) | Clase de objeto base.                     |
| [**CUnknown**](cunknown.md)       | Implementa la **interfaz IUnknown.** |



 

La mayoría de las DirectShow derivan de **CBaseObject**. Esta clase proporciona asistencia para la depuración manteniendo un recuento de todos los objetos activos en el archivo DLL en tiempo de ejecución. En las compilaciones de depuración, el archivo DLL declara si se descarga mientras el número de objetos es mayor que cero. Esto facilita el seguimiento de las pérdidas causadas por problemas de recuento de referencias.

Todas las clases base que admiten interfaces COM derivan de **CUnknown**, que hereda **CBaseObject**. La **clase CUnknown** admite el recuento de referencias, **QueryInterface** y aggregration. Para obtener más información, [vea How to Implement IUnknown](how-to-implement-iunknown.md).

**Filtrar y anclar clases**

Las clases siguientes admiten la creación de DirectShow y anclar objetos:



| Clase                                    | Descripción                                                                                                                                                     |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBaseFilter**](cbasefilter.md)       | Clase base para filtros. Implementa la [**interfaz IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                            |
| [**CBasePin**](cbasepin.md)             | Clase base para los pines. Implementa las [**interfaces IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**e IQualityControl.**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| [**CBaseInputPin**](cbaseinputpin.md)   | Clase base para los pines de entrada que usan transporte de memoria local. Implementa la [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Esta clase se deriva de **CBasePin**. |
| [**CBaseOutputPin**](cbaseoutputpin.md) | Clase base para los pines de salida que usan **conexiones IMemInputPin.** Esta clase se deriva de **CBasePin**.                                                         |



 

Las clases siguientes son útiles para crear tipos de filtros más especializados:



| Clase                                                  | Descripción                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CSource**](csource.md)                             | Clase base para filtros de origen. Esta clase está diseñada para crear orígenes de inserción. No es adecuado para orígenes de extracción, como lectores de archivos. Para crear pasadores de salida para esta clase, use la [**clase CSourceStream.**](csourcestream.md)                                                                   |
| [**CTransformFilter**](ctransformfilter.md)           | Clase base para los filtros de transformación. Esta clase realiza una copia en los datos. Los pines de esta clase son [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin.**](ctransformoutputpin.md)                                                                                            |
| [**CTransInPlaceFilter**](ctransinplacefilter.md)     | Clase base para los filtros de transformación que no copian datos. Esta clase realiza el procesamiento de datos directamente en los datos de entrada antes de pasarlo de bajada. Los pines de esta clase son [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) y [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md). |
| [**CVideoTransformFilter**](cvideotransformfilter.md) | Clase base para filtros de transformación de vídeo. Esta clase se deriva de **CTransformFilter** y agrega compatibilidad con el control de calidad.                                                                                                                                                                                |
| [**CBaseRenderer**](cbaserenderer.md)                 | Clase base para filtros de representador. El pin de entrada de esta clase es [**CRendererInputPin.**](crendererinputpin.md)                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer.md)       | Clase base para representadores de vídeo. Esta clase se deriva de **CBaseRenderer.**                                                                                                                                                                                                                                |



 

Para usar estas clases, debe derivar su propia clase y escribir código para admitir la funcionalidad específica del filtro. Entre más especializada sea la clase base, menos código tendrá que escribir en la clase derivada.

**Objetos auxiliares**

Las clases siguientes implementan objetos auxiliares que usan los filtros y los pines. La mayoría de estas clases se pueden usar sin derivar clases nuevas de ellas:



| Clase                                              | Descripción                                                                                                                                                        |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPullPin**](cpullpin.md)                       | Objeto auxiliar para los pines de entrada en los filtros del analizador. Admite [**conexiones IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) con orígenes de extracción.                                       |
| [**COutputQueue**](coutputqueue.md)               | Objeto auxiliar para los pines de salida que ponen en cola ejemplos para la entrega en un subproceso de trabajo.                                                                                  |
| [**CSourceSeeking**](csourceseeking.md)           | Objeto de ayuda para implementar búsquedas en un filtro de origen con exactamente un pin de salida. (Esta clase no está diseñada para filtros con varios pines, como analizadores). |
| [**CEnumPins**](cenumpins.md)                     | Objeto enumerador para enumerar los pines de un filtro. Implementa la [**interfaz IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)                                                       |
| [**CEnumMediaTypes**](cenummediatypes.md)         | Objeto enumerador para enumerar los tipos de medios preferidos en un pin. Implementa la [**interfaz IEnumMediaTypes.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)                             |
| [**CMemAllocator**](cmemallocator.md)             | Objeto de asignador de memoria. Implementa la [**interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)                                                                          |
| [**CMediaSample**](cmediasample.md)               | Objeto de ejemplo multimedia. Implementa la [**interfaz IMediaSample2.**](/windows/desktop/api/Strmif/nn-strmif-imediasample2)                                                                              |
| [**CBaseReferenceClock**](cbasereferenceclock.md) | Clase base para los relojes de referencia. Implementa la [**interfaz IReferenceClock.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)                                                              |
| [**CMediaType**](cmediatype.md)                   | Objeto auxiliar para manipular estructuras [**de AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                |



 

 

 



