---
description: Filtro de origen de archivo (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origen de archivo (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494987"
---
# <a name="file-source-async-filter"></a>Filtro de origen de archivo (Async)

El filtro de origen de archivo asincrónico se abre y Lee los archivos locales de muchos formatos de datos diferentes y pasa los datos a un filtro de analizador.

Para descargar archivos multimedia de la web a través de HTTP, use el filtro de [origen de archivo (URL)](file-source--url--filter.md) . Para leer archivos ASF, use el filtro de [lector ASF de WM](wm-asf-reader-filter.md) .



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Tipos de medios de anclaje de entrada                    | No aplicable                                                                                                                       |
| Interfaces de PIN de entrada                     | No aplicable                                                                                                                       |
| Tipos de medios de anclaje de salida                   | **MEDIATYPE \_ Flujo**. El subtipo depende del formato del medio. (**MEDIASUBTYPE \_ null** si el filtro no reconoce el formato). |
| Interfaces de clavija de salida                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Identificador CLSID                             | **CLSID \_ AsyncReader**                                                                                                               |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                           |
| [Fundament](merit.md)                       | **MÉRITO \_ improbable**                                                                                                                  |
| [Categoría de filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



