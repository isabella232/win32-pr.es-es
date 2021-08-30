---
description: Filtro del analizador WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro del analizador WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f225dcbde4f15af2c6da5e626ea335e7d88612fd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466572"
---
# <a name="wave-parser-filter"></a>Filtro del analizador WAVE

El filtro wave Parser analiza los datos de audio en formato WAV de los archivos .wav, .au o .aif. El filtro ascendente debe ser el filtro [Origen](file-source--async--filter.md) de archivo asincrónico, el Filtro de origen de archivo [URL](file-source--url--filter.md) o un filtro de origen asincrónico de terceros compatible que contenga datos de audio WAV. El flujo de salida son datos de audio, que se pueden conectar directamente a un filtro de representación de audio o a un filtro de transformación de audio que interviene.




| | | Filtrar interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a> | | Tipos de medios de pin de entrada | Tipo principal: MEDIATYPE_StreamThe los subtipos siguientes son válidos:<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de anclar salida | Tipo principal: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM u otro tipo de compresión. (Vea <a href="audio-subtypes.md"><strong>Subtipos de audio).</strong></a><br /> Tipo de formato: FORMAT_WaveFormatEx<br /> | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | Filtrar clsid | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | | ClSID de página de propiedades | No hay ninguna página de propiedades. | | Archivos ejecutables | quartz.dll | | <a href="merit.md">Ventajas |</a> MERIT_UNLIKELY | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

Este filtro admite los siguientes tipos de archivo:

-   WAVE (.wav)
-   AIFF y AIFF-C (.aif)
-   AU (.au)

Sin embargo, tiene las siguientes limitaciones en el formato de audio:

-   El audio debe ser PCM lineal de 8 o 16 bits.
-   En el caso de los archivos AIFF-C, el audio debe estar descomprimido, en orden de bytes big-endian (tipo de compresión "NONE").

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




