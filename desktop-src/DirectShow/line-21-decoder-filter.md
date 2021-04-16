---
description: Filtro de descodificador de línea 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro de descodificador de línea 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677051"
---
# <a name="line-21-decoder-filter"></a>Filtro de descodificador de línea 21

Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

Este filtro de descodificador de línea 21 descodifica los datos de línea 21 y dibuja el texto de la leyenda en mapas de bits.

El PIN de entrada se conecta a cualquier proveedor de datos de línea 21, normalmente un descodificador de vídeo de DVD o el filtro del [descodificador de CC](cc-decoder-filter.md) . El descodificador de CC proporciona datos de línea 21 procedentes de los VBI de una señal de televisión analógica. El PIN de salida se conecta a un PIN secundario en el [mezclador de superposición](overlay-mixer-filter.md) o a otro representador de vídeo, como VMR.

Este filtro acepta datos de la línea 21 en el formato de par de bytes estándar o, para DVD, como un paquete para todo el grupo de imágenes (GOP). Para cada GOP del flujo de vídeo de DVD, puede haber un paquete de datos de usuario que tenga la información de encabezado y la línea 21 de un GOP concreto. El formato de los pares de bytes se define en el estándar EIA/CEA-no-B; Consulte ese estándar para obtener más información.

Hay disponibles dos versiones de este filtro:



| Filter            | CLSID                 |
|-------------------|-----------------------|
| Descodificador de línea 21   | CLSID \_ Line21Decoder  |
| Descodificador de línea 21 2 | CLSID \_ Line21Decoder2 |



 

El filtro de la versión 1 se usa en las plataformas de Microsoft® Windows® 95/98/me y Windows 2000. El filtro de la versión 2 está disponible en Microsoft Windows XP y versiones posteriores, y se usa siempre que el representador de mezcla de vídeo está en el gráfico.

La información de la tabla siguiente se aplica a ambas versiones del filtro:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_AUXLine21DataSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (línea 21 estándar)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (línea 21 de DVD)</li>
</ul>
Tipo de formato: FORMAT_VideoInfo o GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>Tipo principal: MEDIATYPE_VideoSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Tipo de formato: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>Vea la tabla anterior</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>None</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>Descodificador de línea 21: MERIT_NORMALLine 21 descodificador 2: MERIT_NORMAL + 2<br/></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Subtítulos y teletexto](closed-captions-and-teletext.md)
</dt> <dt>

[Configuración del gráfico de filtros de DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




