---
description: Filtro de descompresión M FILTER
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompresión M FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684945"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro de descompresión M FILTER

Este filtro descodifica una secuencia de vídeo del movimiento JPEG al vídeo sin comprimir. Algunas cámaras de vídeo digitales generan una secuencia de vídeo JPEG de movimiento.



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                               |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ MshuegDec                                                                                                                                    |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                         |
| [Mérito](merit.md)                       | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Comentarios

Este filtro es compatible con el vídeo JPEG de movimiento que usa el código FOURCC "MJPG". No puede descodificar otras variedades de JPEG de movimiento. Para ello, deberá usar un filtro de descodificador de terceros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



