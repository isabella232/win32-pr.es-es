---
description: Filtro descodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro descodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468232"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtro descodificador de vídeo MPEG-1

Descodifica vídeo MPEG-1.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Tipos de medios de pin de entrada | MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Los subtipos siguientes son válidos:<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a> | | Tipos de medios de pin de salida | Tipo principal: <strong>MEDIATYPE_Video</strong>,<br /> Tipo de formato: <strong>FORMAT_VideoInfo</strong> o <strong>FORMAT_VideoInfo2</strong><br /> Subtipos:<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | <strong>CLSID_CMpegVideoCodec</strong> | | Página de propiedades CLSID | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | Archivos ejecutables | quartz.dll | | <a href="merit.md">|</a> 0x40000001 | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

Este filtro se puede descodificar en una superficie directdraw. El filtro usa MMX si la máquina admite MMX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




