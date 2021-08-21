---
description: Formatos admitidos en DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formatos admitidos en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10e42079f29ce89ba66fcd0c03a6520769a91538eb1a9b8901115b6895420d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633235"
---
# <a name="supported-formats-in-directshow"></a>Formatos admitidos en DirectShow

DirectShow es una arquitectura abierta, lo que significa que puede admitir cualquier formato siempre que haya filtros para analizarlo y descodificarlo. Los filtros proporcionados por Microsoft, ya sea como redistribuibles DirectShow o como componentes del sistema operativo Windows, proporcionan compatibilidad predeterminada con los siguientes formatos de archivo y compresión.

Tipos de archivo:



| Tipo de archivo                                                                                        | Más información                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF), que incluye Windows Media Audio (WMA) y Windows Media Video (WMV) | [Filtro de lector de ASF de WM](about-the-wm-asf-reader-filter.md)<br/> [Filtro de escritor de ASF de WM](wm-asf-writer-filter.md)<br/> |
| Aiff                                                                                             | [Filtro del analizador WAVE](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtro del analizador WAVE](wave-parser-filter.md)                                                                                      |
| Audio y vídeo intercalado (AVI)                                                                    | [Filtro Mux de AVI](avi-mux-filter.md)<br/> [Filtro divisor avi](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtro del analizador de MIDI](midi-parser-filter.md)<br/> [**Filtro de representador de MIDI**](midi-renderer-filter.md)<br/>           |
| Snd                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtro del analizador WAVE](wave-parser-filter.md)                                                                                      |



 

Formatos de compresión:



| Formato                                        | Más información                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Descodificador de audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Vídeo digital (DV)                            | [Filtro de descodificador de vídeo DV](dv-video-decoder-filter.md)<br/> [Filtro de codificador de vídeo DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| Iso MPEG-4, versión 1.0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 versión 3                    |                                                                                                                                                                                                                                                 |
| Mjpeg                                         | [Filtro de filtro de filtro de M SCROLLEG](mjpeg-compressor-filter.md)<br/> [Filtro de descompresión M FILTER](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| Mpeg Audio Layer-3 (MP3) (solo descompresión) |                                                                                                                                                                                                                                                 |
| Audio mpeg-1 capa I y capa II             | [**Descodificador de audio Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtro de descodificador de audio MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Vídeo MPEG-1                                  | [Filtro descodificador de vídeo MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Audio MPEG-2                                  | [**Microsoft MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Codificador Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Vídeo MPEG-2                                  | [**Codificador Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md)<br/> [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)<br/> [**Codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Para obtener información sobre la disponibilidad de determinados códecs de terceros para su redistribución DirectShow aplicaciones, póngase en contacto con el fabricante del códec.

 

 




