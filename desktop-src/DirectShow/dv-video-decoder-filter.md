---
description: Filtro de descodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de descodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536501"
---
# <a name="dv-video-decoder-filter"></a>Filtro de descodificador de vídeo DV

Este filtro descodifica una secuencia de vídeo digital (DV) en vídeo sin comprimir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo, FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td><strong>Tipo principal</strong>:<strong>subtipos</strong>de MEDIATYPE_Video:<br/>
<ul>
<li>MEDIASUBTYPE_YUY2</li>
<li>MEDIASUBTYPE_UYVY</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
<li>MEDIASUBTYPE_ARGB32</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_Y41P</li>
</ul>
<strong>Tipos de formato</strong>:<br/> Format_VideoInfo, Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>CLSID_DVDecPropertiesPage</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Use la interfaz [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para establecer la resolución de descodificación en Full, Half size, Quarter size o un tamaño de un octavo.

**Entrelazado**: las versiones anteriores del descodificador siempre desentrelazan el vídeo. A partir de DirectX 9,0, el descodificador de vídeo DV puede conservar el entrelazado. Esto permite que el vídeo entrelazado esté desentrelazado por el procesador de mezcla de vídeo (VMR), para mejorar la calidad de representación. Para usar esta característica, el filtro de nivel inferior debe admitir formatos de [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indicados por ese formato \_ de valor VideoInfo2 en el miembro **formatType** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . En la salida de la resolución completa, las marcas de desentrelazado (**dwInterlace**) de la estructura **VIDEOINFOHEADER2** se establecen en `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , que indica campos entrelazados. A media resolución o inferior, **dwInterlace** se establece en cero, lo que indica fotogramas progresivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




