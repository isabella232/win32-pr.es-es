---
description: Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserción.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexor MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c315d62fcfbda10bad0a4f269d9bbe9f000c0b93
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477010"
---
# <a name="mpeg-2-demultiplexer"></a>Demultiplexor MPEG-2

Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserción. A partir Windows XP, este filtro también admite secuencias de programa en modo de extracción (reproducción de archivos). En plataformas anteriores, use el filtro [divisor MPEG-2](mpeg-2-splitter.md) para secuencias de programa en modo de extracción. Este filtro se puede usar en cualquier tipo de gráfico de filtro, incluido un gráfico de filtros de tv digital BDA.

> [!Note]  
> El demultiplexor MPEG-2 no admite búsquedas precisas de fotogramas.

 




| | | Filtrar interfaces | Todos los modos:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><strong>ISpecifyPropertyPages</strong></li></ul>Solo modo de inserción:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_STREAM<br /> Subtipo:<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Para obtener más información, vea <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 Demultiplexer Media Types</strong></a>.<br /> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | Las secuencias elementales de audio y vídeo deben tener un tipo principal de MEDIATYPE_Audio o MEDIATYPE_Video.<br /> Para obtener más información, vea <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 Demultiplexer Media Types</strong></a>.<br /> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, solo modo de inserción <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource,</strong></a> <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Solo modo de extracción: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | | Filtrar clsid | CLSID_MPEG2Demultiplexer | | ClSID de página de propiedades | Disponible solo para pruebas. Use la <strong>interfaz ISpecifyPropertyPages</strong> para acceder a las páginas de propiedades | | Archivos ejecutables | mpg2splt.ax | | <a href="merit.md">Ventajas |</a> MERIT_NORMAL | | <a href="filter-categories.md">Filtrar categoría |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

Para generar secuencias elementales de audio y vídeo, demux debe recibir las secuencias PCR y SCR. En el lado de entrada, esto significa que una secuencia de transporte debe contener las tablas PAT y PMT que definen el PID para la secuencia PCR; y los flujos de programa deben contener al menos un encabezado pack.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




