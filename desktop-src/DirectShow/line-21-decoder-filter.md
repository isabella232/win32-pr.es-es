---
description: Filtro descodificador de línea 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro descodificador de línea 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0668d4b71b8dcccf4ceacf7f5428fa7a65ad52
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468242"
---
# <a name="line-21-decoder-filter"></a>Filtro descodificador de línea 21

Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

Este filtro descodificador de línea 21 descodifica los datos de la línea 21 y dibuja el texto del título en mapas de bits.

El pin de entrada se conecta a cualquier proveedor de datos de línea 21, normalmente un descodificador de vídeo de DVD o el [filtro cc decoder.](cc-decoder-filter.md) El descodificador CC proporciona datos de la línea 21 de la VBI de una señal de televisión análoga. El pin de salida se conecta a un pin secundario en el panel de [Mixer](overlay-mixer-filter.md) o a otro representador de vídeo, como VMR.

Este filtro acepta datos de la línea 21 en el formato de par de bytes estándar o, para DVD, como un paquete para todo el grupo de imágenes (GOP). Para cada GOP de la secuencia de vídeo de DVD, puede haber un paquete de datos de usuario que tenga la información de encabezado y los datos de la línea 21 de GOP concretos. El formato de los pares de bytes se define en el estándar EIA/CEA-608-B; Consulte ese estándar para obtener más información.

Hay disponibles dos versiones de este filtro:



| Filtrar            | CLSID                 |
|-------------------|-----------------------|
| Descodificador de línea 21   | CLSID \_ Line21Decoder  |
| Descodificador de línea 21 2 | CLSID \_ Line21Decoder2 |



 

El filtro de la versión 1 se usa en las plataformas Microsoft® Windows® 95/98/Me y Windows 2000. El filtro de la versión 2 está disponible en Microsoft Windows XP y versiones posteriores, y se usa siempre que el representador de mezcla de vídeo está en el gráfico.

La información de la tabla siguiente se aplica a ambas versiones del filtro:




| | | Filtrar interfaces | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_AUXLine21DataSubtype:<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (línea estándar 21)</li><li>MEDIASUBTYPE_Line21_GOPPacket (línea de DVD 21)</li></ul>Tipo de formato: FORMAT_VideoInfo o GUID_NULL<br /> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | Tipo principal: MEDIATYPE_VideoSubtype:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>Tipo de formato: FORMAT_VideoInfo<br /> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | Consulte la tabla anterior | | ClSID de página de propiedades | Ninguna | | Archivos ejecutables | qdvd.dll | | <a href="merit.md">Ventajas |</a> Descodificador de línea 21: MERIT_NORMALLine 21 Descodificador 2: MERIT_NORMAL + 2<br /> | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Subtítulos y teletexto](closed-captions-and-teletext.md)
</dt> <dt>

[Configuración del filtro de DVD Graph DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




