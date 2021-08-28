---
description: Filtro del convertidor de espacios de colores
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro del convertidor de espacios de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cadc3f980116f6745d578a06220639b181fe13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477371"
---
# <a name="color-space-converter-filter"></a>Filtro del convertidor de espacios de colores

Este filtro de transformación convierte de un tipo de color RGB a otro tipo RGB, como entre el color RGB de 24 bits y el de 8 bits. Dado que este tipo de conversión se suele controlar de forma más eficaz dentro de un descomprimidor de vídeo, el uso principal del convertidor de espacios de color es cuando el origen de la secuencia consta de marcos RGB sin comprimir.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de medios de pin de entrada | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de anclar salida | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_Colour | | ClSID de página de propiedades | No hay ninguna página de propiedades. | | Archivos ejecutables | quartz.dll | | <a href="merit.md">Ventajas |</a> MERIT_UNLIKELY | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




