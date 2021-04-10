---
description: Filtro de origen de archivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origen de archivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152531"
---
# <a name="file-source-url-filter"></a>Filtro de origen de archivo (URL)

El filtro de origen del archivo de la dirección URL es un filtro de origen asíncrono genérico que funciona con cualquier archivo de código fuente que se puede identificar mediante un localizador uniforme de recursos (URL) y cuyo tipo de medio principal es Stream. Esto incluye los archivos AVI, MOV, MPEG y WAV. Requiere que el filtro de nivel inferior sea un analizador, como el [separador de secuencias MPEG-1](mpeg-1-stream-splitter-filter.md), el [divisor AVI](avi-splitter-filter.md)o el [analizador de películas QuickTime](quicktime-movie-parser-filter.md).



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipos de medios de anclaje de entrada                    | No aplicable                                                                                                                       |
| Interfaces de PIN de entrada                     | No aplicable                                                                                                                       |
| Tipos de medios de anclaje de salida                   | \_Secuencia MEDIATYPE. El subtipo depende del formato del medio. (MEDIASUBTYPE \_ ES NULL si el filtro no reconoce el formato).         |
| Interfaces de clavija de salida                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Identificador CLSID                             | CLSID \_ URLReader                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>Observaciones

Este filtro usa URLMon y admite páginas de códigos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



