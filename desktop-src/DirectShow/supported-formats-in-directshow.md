---
description: Formatos admitidos en DirectShow
ms.assetid: cd8af779-2fb5-4724-a838-5d0c8244f0d3
title: Formatos admitidos en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a6c9a0c85a3ccdfd3db092ba2efce00a191493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688081"
---
# <a name="supported-formats-in-directshow"></a>Formatos admitidos en DirectShow

DirectShow es una arquitectura abierta, lo que significa que puede admitir cualquier formato, siempre y cuando haya filtros para analizarlos y descodificarlos. Los filtros proporcionados por Microsoft, ya sea como redistribuibles a través de DirectShow o como componentes del sistema operativo Windows, proporcionan compatibilidad predeterminada para los siguientes formatos de archivo y compresión.

Tipos de archivo:



| Tipo de archivo                                                                                        | Más información                                                                                                                  |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Advanced Systems Format (ASF), incluido Windows Media Audio (WMA) y Windows Media Video (WMV) | [Filtro de lector ASF de WM](about-the-wm-asf-reader-filter.md)<br/> [Filtro de escritor ASF de WM](wm-asf-writer-filter.md)<br/> |
| AIFF                                                                                             | [Filtro de WAVE parser](wave-parser-filter.md)                                                                                      |
| AU                                                                                               | [Filtro de WAVE parser](wave-parser-filter.md)                                                                                      |
| Audio y vídeo intercalado (AVI)                                                                    | [Filtro de AVI-MUX](avi-mux-filter.md)<br/> [Filtro de divisor de AVI](avi-splitter-filter.md)<br/>                         |
| MIDI                                                                                             | [Filtro de analizador MIDI](midi-parser-filter.md)<br/> [**Filtro de representador MIDI**](midi-renderer-filter.md)<br/>           |
| SND                                                                                              |                                                                                                                                   |
| WAV                                                                                              | [Filtro de WAVE parser](wave-parser-filter.md)                                                                                      |



 

Formatos de compresión:



| Formato                                        | Más información                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AAC                                           | [**Descodificador de audio MPEG-1/DD/AAC de Microsoft**](microsoft-mpeg-1-dd-audio-decoder.md)                                                                                                                                                              |
| Cinepak                                       |                                                                                                                                                                                                                                                 |
| Vídeo digital (DV)                            | [Filtro de descodificador de vídeo DV](dv-video-decoder-filter.md)<br/> [Filtro de codificador de vídeo DV](dv-video-encoder-filter.md)<br/>                                                                                                             |
| H.264                                         | [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)                                                                                                                                                                        |
| ISO MPEG-4 vídeo versión 1,0                  |                                                                                                                                                                                                                                                 |
| Microsoft MPEG-4 versión 3                    |                                                                                                                                                                                                                                                 |
| MJPEG                                         | [Filtro del compresor MJPEG](mjpeg-compressor-filter.md)<br/> [Filtro de descompresor de MJPEG](mjpeg-decompressor-filter.md)<br/>                                                                                                         |
| Capa de audio MPEG-3 (MP3) (solo descompresión) |                                                                                                                                                                                                                                                 |
| Audio MPEG-1 capa I y capa II             | [**Descodificador de audio MPEG-1/DD/AAC de Microsoft**](microsoft-mpeg-1-dd-audio-decoder.md)<br/> [Filtro de descodificador de audio MPEG-1](mpeg-1-audio-decoder-filter.md)<br/>                                                                         |
| Vídeo MPEG-1                                  | [Filtro de descodificador de vídeo MPEG-1](mpeg-1-video-decoder-filter.md)<br/> [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)<br/>                                                                                   |
| Audio MPEG-2                                  | [**Codificador de audio MPEG-2 de Microsoft**](microsoft-mpeg-2-audio-encoder.md)<br/> [**Codificador MPEG-2 de Microsoft**](microsoft-mpeg-2-encoder.md)<br/>                                                                                     |
| Vídeo MPEG-2                                  | [**Codificador MPEG-2 de Microsoft**](microsoft-mpeg-2-encoder.md)<br/> [**Descodificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-decoder.md)<br/> [**Codificador de vídeo MPEG-2 de Microsoft**](microsoft-mpeg-2-video-encoder.md)<br/> |



 

Para obtener información sobre la disponibilidad de determinados códecs de terceros para la redistribución con aplicaciones de DirectShow, póngase en contacto con el fabricante del códec.

 

 




