---
description: Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserciones.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexador MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686342"
---
# <a name="mpeg-2-demultiplexer"></a>Demultiplexador MPEG-2

Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserciones. A partir de Windows XP, este filtro también admite secuencias de programa en el modo de extracción (reproducción de archivos). En plataformas anteriores, use el filtro de [divisor de MPEG-2](mpeg-2-splitter.md) para los flujos de programa en el modo de extracción. Este filtro se puede usar en cualquier tipo de gráfico de filtros, incluido un gráfico de filtros de TV digital BDA.

> [!Note]  
> El desmultiplexador MPEG-2 no admite búsquedas con precisión de fotogramas.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td>Todos los modos:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><strong>ISpecifyPropertyPages</strong></li>
</ul>
Solo modo de inserciones:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Tipo principal: MEDIATYPE_STREAM<br/> Subtipo<br/>
<ul>
<li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_PROGRAM</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT</li>
<li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li>
</ul>
Para obtener más información, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de medios de desmultiplexado MPEG-2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>Los flujos elementales de audio y vídeo deben tener un tipo principal de MEDIATYPE_Audio o MEDIATYPE_Video.<br/> Para obtener más información, consulte <a href="mpeg-2-demultiplexer-media-types.md"><strong>tipos de medios de desmultiplexado MPEG-2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>modo de solo envío: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br/> Solo el modo de extracción: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br/></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_MPEG2Demultiplexer</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Solo está disponible para pruebas. Usar la interfaz <strong>ISpecifyPropertyPages</strong> para tener acceso a las páginas de propiedades</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>mpg2splt.ax</td>
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

Para generar secuencias elementales de audio y vídeo, el Demux debe recibir los flujos PCR y SCR. En el lado de entrada, esto significa que una secuencia de transporte debe contener las tablas PAT y PMT que definen el PID para el flujo de PCR. los flujos de programa y deben contener al menos un encabezado de paquete.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




