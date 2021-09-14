---
description: Filtro de origen de archivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origen de archivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255164"
---
# <a name="file-source-url-filter"></a>Filtro de origen de archivo (URL)

El filtro Origen del archivo URL es un filtro de origen asincrónico genérico que funciona con cualquier archivo de origen que se pueda identificar mediante un localizador uniforme de recursos (URL) y cuyo tipo principal de medio sea stream. Esto incluye archivos AVI, MOV, MPEG y WAV. Requiere que el filtro de bajada sea un analizador, como el divisor de [secuencias MPEG-1,](mpeg-1-stream-splitter-filter.md)el divisor [AVI](avi-splitter-filter.md)o el analizador de películas [quicktime.](quicktime-movie-parser-filter.md)



| Etiqueta | Value |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipos de medios de pin de entrada                    | No aplicable                                                                                                                       |
| Interfaces de pin de entrada                     | No aplicable                                                                                                                       |
| Tipos de medios de pin de salida                   | Secuencia \_ MEDIATYPE. El subtipo depende del formato multimedia. (MEDIASUBTYPE \_ NULL si el filtro no reconoce el formato).         |
| Interfaces de pin de salida                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtrar CLSID                             | CLSID \_ URLReader                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                           |
| [Mérito](merit.md)                       | NO ES \_ PROBABLE QUE SE PRODUZCAN                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>Observaciones

Este filtro usa URLMon y admite páginas de códigos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



