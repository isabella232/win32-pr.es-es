---
description: En este tema, mostramos los formatos de medios que Microsoft Media Foundation admite de forma nativa.
ms.assetid: 69c12a28-4b58-4979-b4d8-ae37efa847fe
title: Formatos de medios admitidos en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ecbc5024ab70e9e0bdd07d6213ad9779c21e2b7f34f10f3e2d3fe538a784734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238194"
---
# <a name="supported-media-formats-in-media-foundation"></a>Formatos de medios admitidos en Media Foundation

En este tema, mostramos los formatos de medios que Microsoft Media Foundation admite de forma nativa. Los terceros pueden admitir formatos adicionales mediante la escritura de complementos personalizados.

## <a name="file-containers"></a>Contenedores de archivos



| Formato                                           | Extensiones de archivo          | Origen multimedia                                 | Receptor multimedia                                   | Requiere                                                              |
|--------------------------------------------------|--------------------------|----------------------------------------------|----------------------------------------------|-----------------------------------------------------------------------|
| 3GP                                              | .3g2, .3gp, .3gp2, .3gpp | [Origen de archivo MPEG-4](mpeg-4-file-source.md) | Receptor de archivos 3GP                                | Windows 7                                                             |
| Formato de streaming avanzado (ASF)                  | .asf, .wma, .wmv         | [Origen multimedia de ASF](asf-media-source.md)     | [Receptor de medios de ASF](asf-media-sinks.md)        | Windows Vista                                                         |
| Secuencia de transporte de datos de audio (ADTS).              | .aac, .adts              | Origen del archivo ADTS                             | None                                         | Windows 7                                                             |
| AVI                                              | .avi                     | Origen del archivo AVI                              | None                                         | Windows 7                                                             |
| MP3                                              | .mp3                     | [**Origen del archivo MP3**](mp3-file-source.md)   | Receptor de archivos MP3                                | Origen del archivo: Windows Vista<br/> Receptor de archivos: Windows 7<br/> |
| MPEG-4                                           | .m4a, .m4v, .mov, .mp4   | [Origen de archivo MPEG-4](mpeg-4-file-source.md) | [**Receptor de archivos MPEG-4**](mpeg-4-file-sink.md) | Windows 7                                                             |
| Intercambio multimedia accesible sincronizado (SAMI) | .sami, .smi              | [Origen multimedia SAMI](sami-media-source.md)   | None                                         | Windows Vista                                                         |
| Onda                                             | .wav                     | Origen del archivo AVI                              | None                                         | Windows 7                                                             |



 

## <a name="audio-codecs"></a>Códecs de audio



| Formato                                              | Descodificador                                                                                                                                                          | Codificador                                                                                                                                                          | Requiere      |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| μ código de ley                                        | Códec de μ de audio compression Manager (ACM)                                                                                                                      | None                                                                                                                                                             | Windows Vista |
| Adaptive Differential Pulse Code Adaptive Code Adaptive (ADPCM) | Códec ADPCM de ACM                                                                                                                                                  | None                                                                                                                                                             | Windows Vista |
| Codificación de audio avanzada (AAC)                         | [**Descodificador de AAC**](aac-decoder.md)                                                                                                                               | [**Codificador AAC**](aac-encoder.md)                                                                                                                               | Windows 7     |
| MP3                                                 | [**Windows Descodificador de MP3 multimedia**](windows-media-mp3-decoder.md)                                                                                                   | None                                                                                                                                                             | Windows Vista |
| GSM 6.10                                            | Códec ACM GSM 6.10                                                                                                                                               | None                                                                                                                                                             | Windows Vista |
| Audio de Windows Media (WMA)                           | [**Windows Descodificador de audio multimedia**](windowsmediaaudiodecoder.md)<br/> [**Windows Descodificador de voz de audio multimedia**](windowsmediaaudiovoicedecoder.md)<br/> | [**Windows Codificador de audio multimedia**](windowsmediaaudioencoder.md)<br/> [**Windows Codificador de voz de audio multimedia**](windowsmediaaudiovoiceencoder.md)<br/> | Windows Vista |



 

> [!Note]  
> Media Foundation proporciona contenedores para varios códecs de ACM, enumerados en la tabla anterior. Sin embargo, Media Foundation no admite códecs ACM arbitrarios.

 

## <a name="video-codecs"></a>Códecs de vídeo



| Formato                                                                                                         | Descodificador                                                                                                                                                                  | Codificador                                                                                                                             | Requiere      |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Vídeo DV                                                                                                       | [**Descodificador de vídeo DV**](dv-video-decoder.md)                                                                                                                             | None                                                                                                                                | Windows 7     |
| H.264                                                                                                          | [**Descodificador de vídeo H.264**](h-264-video-decoder.md)                                                                                                                       | [**Codificador de vídeo H.264**](h-264-video-encoder.md)                                                                                  | Windows 7     |
| H.263<br/> (Perfil de línea base H.264 que es compatible con el modo de encabezado de vídeo corto MPEG-4 Pt2)<br/> | [**Descodificador de vídeo MPEG-4, parte 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 8     |
| Mjpeg                                                                                                          | Descodificador M JPEG                                                                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4, parte 2                                                                                                  | [**Descodificador de vídeo MPEG-4, parte 2**](mpeg4part2videodecoder.md)                                                                                                            | None                                                                                                                                | Windows 7     |
| MPEG-4 v1/v2/v3                                                                                                | [**Windows Descodificador MPEG-4 V3 multimedia**](./windowsmediampeg4v3decoder.md)<br/> [**Windows Descodificador MPEG4 V1/V2 multimedia**](windowsmediampeg4decoder.md)<br/>         | None                                                                                                                                | Windows Vista |
| Vídeo de Windows Media (WMV)                                                                                      | [**Windows Descodificador de Vídeo multimedia 9**](windowsmediavideo9decoder.md)<br/> [**Windows Descodificador de pantalla de Vídeo multimedia 9**](windowsmediavideo9screendecoder.md)<br/> | Windows Codificador Media Video 9<br/> Windows Codificador de pantalla de Vídeo multimedia 9<br/> Windows Codificador Media Video 7/8<br/> | Windows Vista |



 

> [!Note]  
> La columna "Requiere" muestra el sistema operativo mínimo necesario para usar estos códecs dentro de una Media Foundation aplicación. Algunos de estos códecs se introdujeron antes de Windows Vista como objetos multimedia [DirectX](../directshow/directx-media-objects.md) (DDO). Si un códec admite DMO funcionalidad, se puede usar con DirectShow [o](../directshow/directshow.md) el SDK Windows [Media Format](../wmformat/windows-media-format-11-sdk.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> <dt>

[Orígenes multimedia y receptores](media-sources-and-sinks.md)
</dt> </dl>

 

 
