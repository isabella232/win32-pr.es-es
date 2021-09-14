---
description: Filtro de descodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de descodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12aead5f8238064198c31566a1e2ca1fde75931
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246609"
---
# <a name="dv-video-decoder-filter"></a>Filtro de descodificador de vídeo DV

Este filtro descodifica una secuencia de vídeo digital (DV) en vídeo sin comprimir.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | 
| Tipos de medios de pin de entrada | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo, FORMAT_DvInfo</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | <strong>Tipo principal:</strong>MEDIATYPE_Video<strong>subtipos</strong>:<br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>Tipos de formato:</strong><br /> Format_VideoInfo, Format_VideoInfo2<br /> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_DVVideoCodec | 
| CLSID de la página de propiedades | CLSID_DVDecPropertiesPage | 
| Executable | qdv.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

Use la [**interfaz IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para establecer la resolución de lacoding en tamaño completo, de tamaño medio, de trimestre o de un octavo tamaño.

**Entrelazado:** las versiones anteriores del descodificador siempre desenlazar el vídeo. A partir de DirectX 9.0, el descodificador de vídeo DV puede conservar el entrelazado. Esto permite que el representador de mezcla de vídeo (VMR) desinterese el vídeo entrelazado para mejorar la calidad de la representación. Para usar esta característica, el filtro de nivel inferior debe admitir formatos [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) indicados por ese valor Format VideoInfo2 en el miembro formattype de la estructura \_ AM MEDIA [**\_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)  En la salida de resolución completa, las marcas de desenlace (**dwInterlace**) de la estructura **VIDEOINFOHEADER2** se establecen en , lo que indica campos `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` entrelazados. A media resolución o inferior, **dwInterlace** se establece en cero, lo que indica fotogramas progresivas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




