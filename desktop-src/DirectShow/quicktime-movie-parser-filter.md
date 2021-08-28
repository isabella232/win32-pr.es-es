---
description: Filtro del analizador de películas de QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro del analizador de películas de QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476721"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro del analizador de películas de QuickTime

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

El filtro QuickTime Movie Parser divide los datos ® QuickTime de Apple® en secuencias de audio y vídeo. Admite QuickTime 2.0 y versiones anteriores. El pin de entrada se conecta a un filtro de origen, como el filtro [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) o [el filtro URL File Source (Origen del archivo url).](file-source--url--filter.md) El analizador usa el filtro [de descompresión AVI](avi-decompressor-filter.md) o [qt decompressor](qt-decompressor-filter.md) para descomprimir archivos QuickTime. El filtro crea un pin de salida para la secuencia de vídeo y un pin de salida para la secuencia de audio.




| | | Filtrar interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de medios de pin de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de anclar salida | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_QuickTimeParser | | ClSID de página de propiedades | No hay ninguna página de propiedades. | | Archivos ejecutables | quartz.dll | | <a href="merit.md">Ventajas |</a> MERIT_NORMAL | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



