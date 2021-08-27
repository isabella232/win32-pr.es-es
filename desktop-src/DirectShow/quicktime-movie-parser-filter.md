---
description: Filtro de analizador de películas de QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro de analizador de películas de QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0028b604efe31749144ca98cb80057685ed0c1db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983618"
---
# <a name="quicktime-movie-parser-filter"></a>Filtro de analizador de películas de QuickTime

Este componente se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

El filtro QuickTime Movie Parser divide los datos de Apple® QuickTime® en secuencias de audio y vídeo. Admite QuickTime 2.0 y versiones anteriores. El pin de entrada se conecta a un filtro de origen, como el filtro [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) o [el filtro URL File Source (Origen de archivo](file-source--url--filter.md) de dirección URL). El analizador usa el filtro [de descompresión AVI](avi-decompressor-filter.md) o [QT Decompressor](qt-decompressor-filter.md) para descomprimir archivos QuickTime. El filtro crea un pin de salida para la secuencia de vídeo y un pin de salida para la secuencia de audio.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| Tipos de medios de pin de entrada | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_QuickTimeParser | 
| CLSID de la página de propiedades | No hay ninguna página de propiedades. | 
| Executable | quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



