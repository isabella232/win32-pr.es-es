---
description: Filtro del compresor MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro del compresor MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677177"
---
# <a name="mjpeg-compressor-filter"></a>Filtro del compresor MJPEG

Este filtro comprime una secuencia de vídeo sin comprimir, usando la compresión Motion JPEG.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipos de medios de anclaje de entrada                    | \_vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de medios de anclaje de salida                   | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfaces de clavija de salida                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Este filtro codifica mediante el subtipo de medio MEDIASUBTYPE \_ MJPG, que corresponde al código FourCC "MJPG".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



