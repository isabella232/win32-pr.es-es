---
description: Filtro de filtro de filtro M FILTER
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de filtro de filtro M FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7891a85aa32b0ec7572a8c3be08f216c75f8655a7782261a675521aa952bf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791395"
---
# <a name="mjpeg-compressor-filter"></a>Filtro de filtro de filtro M FILTER

Este filtro comprime una secuencia de vídeo sin comprimir mediante la compresión JPEG de movimiento.



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Este filtro codifica mediante el subtipo multimedia MEDIASUBTYPE MJPG, que corresponde al código \_ FOURCC "MJPG".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



