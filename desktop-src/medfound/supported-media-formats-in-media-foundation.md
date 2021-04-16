---
description: En este tema, mostramos los formatos de medios que Microsoft Media Foundation admite de forma nativa.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formatos de medios admitidos en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e8f698179d37fc6bde8d5d1dab25214727cd38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670085"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formatos de medios admitidos en Media Foundation

En este tema, mostramos los formatos de medios que Microsoft Media Foundation admite de forma nativa. Los terceros pueden admitir formatos adicionales escribiendo complementos personalizados.

## <a name="file-containers"></a>Contenedores de archivos



| Formato                                           | Extensiones de archivo          | Origen de medios                                 | Receptor de medios                                   | Requiere                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2,. 3GP,. 3GP2,. 3GPP | [Origen de archivo MPEG-4](mpeg-4-file-source.md) | Receptor de archivos 3GP                                | Windows 7                                                             |
| Formato de streaming avanzado (ASF)                  | . ASF,. WMA,. wmv         | [Origen de medios ASF](asf-media-source.md)     | [Receptor de medios ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Secuencia de transporte de datos de audio (ADTS).              | . AAC,. ADTS              | Origen de archivo ADTS                             | None                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Origen de archivo AVI                              | None                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Origen de archivo MP3**](mp3-file-source.md)   | Receptor de archivos MP3                                | Origen de archivo: Windows Vista<br/> Receptor de archivos: Windows 7<br/> |
| MPEG-4                                           | . m4a,. M4V,. mov,. MP4   | [Origen de archivo MPEG-4](mpeg-4-file-source.md) | [**Receptor de archivos MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Intercambio de multimedia accesible sincronizado (SAMI) | . sami,. SMI              | [Origen de medios SAMI](sami-media-source.md)   | None                                         | Windows Vista                                                         |
| ONDAS                                             | .wav                     | Origen de archivo AVI                              | None                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Códecs de audio



| Formato                                              | Descodificador                                                                                                                                                          | Codificador                                                                                                                                                          | Requiere      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ-código de ley                                        | Codec del administrador de compresión de audio (ACM) μ-law                                                                                                                      | None                                                                                                                                                             | Windows Vista |
| Modulación de código de impulso diferencial adaptable (ADPCM) | Codec ADPCM de ACM                                                                                                                                                  | None                                                                                                                                                             | Windows Vista |
| Codificación de audio avanzada (AAC)                         | [**Descodificador AAC**](aac-decoder.md)                                                                                                                               | [**Codificador AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Descodificador MP3 de Windows Media**](windows-media-mp3-decoder.md)                                                                                                   | None                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Códec ACM GSM 6,10                                                                                                                                               | None                                                                                                                                                             | Windows Vista |
| Audio de Windows Media (WMA)                           | [**Descodificador de Windows Media Audio**](windowsmediaaudiodecoder.md)<br/> [**Descodificador de Windows Media Audio Voice**](windowsmediaaudiovoicedecoder.md)<br/> | [**Codificador Windows Media Audio**](windowsmediaaudioencoder.md)<br/> [**Codificador de voz Windows Media Audio**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation proporciona contenedores para varios códecs ACM, enumerados en la tabla anterior. Sin embargo, Media Foundation no admite códecs ACM arbitrarios.

 

## <a name="video-codecs"></a>Códecs de vídeo



| Formato                                                                                                         | Descodificador                                                                                                                                                                  | Codificador                                                                                                                             | Requiere      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vídeo DV                                                                                                       | [**Descodificador de vídeo DV**](dv-video-decoder.md)                                                                                                                             | None                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Descodificador de vídeo H. 264**](h-264-video-decoder.md)                                                                                                                       | [**Codificador de vídeo H. 264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Perfil de línea base H. 264 que es compatible con el modo de encabezado de vídeo corto de MPEG-4 PT2)<br/> | [**Descodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 8     |
| MJPEG                                                                                                          | Descodificador MJPEG                                                                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4, parte 2                                                                                                  | [**Descodificador de vídeo MPEG-4 parte 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4 V1/V2/V3                                                                                                | [**Descodificador MPEG-4 V3 de Windows Media**](./windowsmediampeg4v3decoder.md)<br/> [**Descodificador MPEG4 v1/v2 de Windows Media**](windowsmediampeg4decoder.md)<br/>         | None                                                                                                                                | Windows Vista |
| Vídeo de Windows Media (WMV)                                                                                      | [**Descodificador de Windows Media Video 9**](windowsmediavideo9decoder.md)<br/> [**Descodificador de pantalla de Windows Media Video 9**](windowsmediavideo9screendecoder.md)<br/> | Codificador de Windows Media Video 9<br/> Codificador de pantalla de Windows Media Video 9<br/> Codificador Windows Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> La columna "requires" muestra el sistema operativo mínimo necesario para usar estos códecs dentro de una aplicación Media Foundation. Algunos de estos códecs se introdujeron antes de Windows Vista como [objetos multimedia de DirectX](../directshow/directx-media-objects.md) (DMOs). Si un códec admite la funcionalidad de DMO, se puede usar con [DirectShow](../directshow/directshow.md) o con el [SDK de Windows Media Format](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Orígenes y receptores de medios](media-sources-and-sinks.md)
</dt> </dl>

 

 
