---
description: Filtro de filtro de filtro M FILTER
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de filtro de filtro M FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910013"
---
# <a name="mjpeg-compressor-filter"></a>Filtro de filtro de filtro M FILTER

Este filtro comprime una secuencia de vídeo sin comprimir mediante la compresión JPEG de movimiento.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Este filtro codifica mediante el subtipo multimedia MEDIASUBTYPE MJPG, que corresponde al código \_ FOURCC "MJPG".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



