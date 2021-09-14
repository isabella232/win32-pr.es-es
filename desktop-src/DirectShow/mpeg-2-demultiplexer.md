---
description: Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserción.
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: Demultiplexor MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21898cb4fa3c16b07508dc3370c519d3edfbced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251114"
---
# <a name="mpeg-2-demultiplexer"></a>Demultiplexor MPEG-2

Este filtro desmultiplexa los flujos de transporte y programa MPEG-2 que se entregan en modo de inserción. A partir Windows XP, este filtro también admite secuencias de programa en modo de extracción (reproducción de archivos). En plataformas anteriores, use el filtro [divisor MPEG-2](mpeg-2-splitter.md) para secuencias de programa en modo de extracción. Este filtro se puede usar en cualquier tipo de gráfico de filtro, incluido un gráfico de filtros de TV digital BDA.

> [!Note]  
> El demultiplexador MPEG-2 no admite búsquedas precisas de fotogramas.

 




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | Todos los modos:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><strong>ISpecifyPropertyPages</strong></li></ul>Solo modo de inserción:<br /><ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_STREAM<br /> Subtipo:<br /><ul><li>KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT</li><li>MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</li></ul>Para obtener más información, <a href="mpeg-2-demultiplexer-media-types.md"><strong>vea Mpeg-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | Las secuencias elementales de audio y vídeo deben tener un tipo principal de MEDIATYPE_Audio o MEDIATYPE_Video.<br /> Para obtener más información, <a href="mpeg-2-demultiplexer-media-types.md"><strong>vea Mpeg-2 Demultiplexer Media Types</strong></a>.<br /> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, solo en modo push <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl:</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a><br /> Solo modo de extracción: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a><br /> | 
| Filtrar CLSID | CLSID_MPEG2Demultiplexer | 
| CLSID de la página de propiedades | Disponible solo para pruebas. Uso de <strong>la interfaz ISpecifyPropertyPages</strong> para acceder a las páginas de propiedades | 
| Executable | mpg2splt.ax | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

Para generar secuencias elementales de audio y vídeo, demux debe recibir las secuencias PCR y SCR. En el lado de entrada, esto significa que una secuencia de transporte debe contener las tablas PAT y PMT que definen el PID para la secuencia PCR; y los flujos de programa deben contener al menos un encabezado pack.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003 R2<br/>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




