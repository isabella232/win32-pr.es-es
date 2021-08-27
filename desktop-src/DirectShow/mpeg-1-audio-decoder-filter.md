---
description: Filtro de descodificador de audio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro de descodificador de audio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa6e72d52d7dc25abd137f98a83b8ffce4359c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471261"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtro de descodificador de audio MPEG-1

Descodifica audio mpeg-1 capa I y capa II a PCM.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Tipos de medios de pin de entrada | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | | Interfaces de pin de salida | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_CMpegAudioCodec | | Página de propiedades CLSID | CLSID_MpegAudioDecoderPropertyPage | | Archivos ejecutables | quartz.dll | | <a href="merit.md">|</a> 0x03680001 | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




