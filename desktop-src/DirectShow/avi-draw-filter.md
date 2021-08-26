---
description: Filtro de dibujo de AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de dibujo de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003336a68bdc1591e6e9a3f8af139f4bf27ddc4d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471281"
---
# <a name="avi-draw-filter"></a>Filtro de dibujo de AVI

El filtro Descomprimir AVI Draw se extrae automáticamente en un gráfico de reproducción en lugar del [descomprimidor AVI](avi-decompressor-filter.md) cuando el vídeo se está generando en un monitor de televisión PLAYBACK externo.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_VideoSubtypes:<br /><ul><li>MEDIASUBTYPE_MJPG</li><li>MEDIASUBTYPE_TVMJ</li><li>MEDIASUBTYPE_WAKE</li><li>MEDIASUBTYPE_CFCC</li><li>MEDIASUBTYPE_IJPG</li><li>MEDIASUBTYPE_Plum</li><li>MEDIASUBTYPE_DVCS</li><li>MEDIASUBTYPE_DVSD</li><li>MEDIASUBTYPE_MDVF</li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | MEDIATYPE_Video, MEDIASUBTYPE_NULL | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_AVIDraw | | ClSID de página de propiedades | No hay ninguna página de propiedades. | | Archivos ejecutables | quartz.dll | | <a href="merit.md">|</a> MERIT_NORMAL + 100 | | <a href="filter-categories.md">Filtrar categoría |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

Puesto que el filtro de dibujo avi y el filtro de [captura vfw](vfw-capture-filter.md) se conectan al mismo hardware, no pueden estar en el mismo gráfico de filtros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




