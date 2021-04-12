---
description: Filtro de descompresor de MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompresor de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537995"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro de descompresor de MJPEG

Este filtro descodifica un flujo de vídeo de Motion JPEG a vídeo sin comprimir. Algunas cámaras de vídeo digital producen una secuencia de vídeo Motion JPEG.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipos de medios de anclaje de entrada                    | \_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de anclaje de salida                   | \_vídeo de MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                               |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Este filtro es compatible con el vídeo Motion JPEG que usa el código FOURCC "MJPG". No puede descodificar otras variedades de movimiento JPEG. Para ello, deberá usar un filtro de descodificador de terceros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



