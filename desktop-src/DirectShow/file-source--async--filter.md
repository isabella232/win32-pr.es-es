---
description: Filtro de origen de archivo (asincrónico)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origen de archivo (asincrónico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255165"
---
# <a name="file-source-async-filter"></a>Filtro de origen de archivo (asincrónico)

El filtro Async File Source (Origen de archivo asincrónico) se abre y lee archivos locales de muchos formatos de datos diferentes y pasa los datos a un filtro de analizador.

Para descargar archivos multimedia desde la web a través de HTTP, use el filtro [Origen de archivo (URL).](file-source--url--filter.md) Para leer archivos ASF, use el filtro [WM ASF Reader.](wm-asf-reader-filter.md)



| Etiqueta | Value |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Tipos de medios de pin de entrada                    | No aplicable                                                                                                                       |
| Interfaces de pin de entrada                     | No aplicable                                                                                                                       |
| Tipos de medios de pin de salida                   | **MEDIATYPE \_ Transmitir**. El subtipo depende del formato multimedia. **(MEDIASUBTYPE \_ NULL** si el filtro no reconoce el formato). |
| Interfaces de pin de salida                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtrar CLSID                             | **CLSID \_ AsyncReader**                                                                                                               |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                     |
| Executable                               | quartz.dll                                                                                                                           |
| [Mérito](merit.md)                       | **NO ES \_ PROBABLE QUE SE PRODUZCAN**                                                                                                                  |
| [Categoría de filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



