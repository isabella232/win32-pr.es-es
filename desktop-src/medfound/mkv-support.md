---
description: En esta sección se describe Media Foundation compatibilidad con archivos de Matroska Media Container (MKV).
title: Compatibilidad con Matroska Media Container (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aceb7a836b4a0409af3c359c8d81a0f232e6eb61082960cfb2b0705531de199c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102145"
---
# <a name="matroska-media-container-mkv-support"></a>Compatibilidad con Matroska Media Container (MKV)

En esta sección se describe Media Foundation compatibilidad con archivos de Matroska Media Container (MKV).

El formato MPEG puede admitir varios códecs de audio y vídeo, como H.264 y audio AAC. En general, los contenedores describen cómo se scriben los datos de vídeo y audio y qué información adicional se usa para describir esas secuencias de A/V. Los contenedores también pueden incluir datos que complementan las secuencias A/V, como el título, los idiomas de las secuencias de audio, las pistas de subtítulos o subtítulos, las fuentes para esos subtítulos, imágenes, información de capítulos y menús. CSV es un formato muy flexible que admite muchas de estas características de contenedor. Para obtener más información sobre el formato CSV, consulte [https://matroska.org](https://matroska.org/)


## <a name="mkv-container-feature-support"></a>Compatibilidad con características de contenedor DE TOR
Las características del contenedor DE SINC son compatibles con Media Foundation de las siguientes maneras:
- Si hay una o varias pistas de vídeo, se reproducirá la primera pista.
- Si hay una o varias pistas de audio, se reproducirá la primera pista.
- Se admiten pistas de título, pero no se seleccionan (se reproducen) de forma predeterminada.
- Si hay una o varias fuentes o imágenes, los títulos e imágenes no se representarán, aunque el archivo se cargará y reproducirá.
- La información del menú no se admite y no se mostrará, pero el archivo se cargará y reproducirá.
- Si los archivos con capítulos hacen referencia a archivos complementarios, los archivos complementarios no se reproducirán.
- Las imágenes en miniatura están disponibles al buscar archivos en unidades USB mediante el explorador de archivos.

Este conjunto de características debe permitir la reproducción de la mayoría de los archivos MPEG si contienen códecs admitidos.
Se admiten los archivos MPEG que contienen pistas de vídeo y audio codificadas con los códecs enumerados en la sección siguiente.

## <a name="supported-mkv-codecs"></a>Códecs MPEG admitidos

### <a name="video-codec-support-for-mkv"></a>Compatibilidad con códecs de vídeo para MPEG

Identificador de Matroska: V_MPEG4/ISO/AVC

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264
- Descripción: vídeo H.264
- Identificadores de FourCC o WAV: H264

Identificador de Matroska: V_MPEG2

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2
- Descripción: vídeo MPEG-2

Identificador de Matroska: V_MPEG1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1
- Descripción: vídeo MPEG-1
- Identificadores fourCC o WAV: MPG1

Identificador de Matroska: V_MPEG4/MS/V3

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43
- Descripción: Códec Microsoft MPEG 4 versión 3
- Identificadores fourCC o WAV: MP43

Identificador de Matroska: V_MPEG4/ISO/ASP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descripción: vídeo MPEG-4, parte 2
- Identificadores fourCC o WAV: MP4V

Identificador de Matroska: V_MS/VFW/FOURCC

- Descripción: Mapas a varios códecs que normalmente se admiten en el formato AVI que están disponibles en la consola.

Identificador de Matroska: V_THEORA

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora
- Descripción: Theora
- Identificadores fourCC o WAV: theo

Identificador de Matroska: V_MPEG4/ISO/SP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descripción: Perfil simple DE MPEG4 ISO (DivX4)
- Identificadores fourCC o WAV: MP4V

Identificador de Matroska: V_MPEG4/ISO/AP

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V
- Descripción: perfil sencillo avanzado MPEG4 ISO (DivX5, DivD, FFMPEG)
- Identificadores fourCC o WAV: MP4V


Identificador de Matroska: V_MPEGH/ISO/HEVC 

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC
- Descripción: HEVC/H.265
- Identificadores fourCC o WAV: 

Identificador de Matroska: V_VP8

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80
- Descripción: Formato de códec VP8
- Identificadores fourCC o WAV: VP80

Identificador de Matroska: V_VP9

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90
- Descripción: Formato de códec VP9
- Identificadores fourCC o WAV: VP90

Identificador de Matroska: V_MJPEG

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG
- Descripción: Motion JPEG
- Identificadores de FourCC o WAV: MJPG

Identificador de Matroska: V_AV1

- MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1
- Descripción: AOMedia Video 1
- Identificadores fourCC o WAV: AV01

### <a name="audio-codec-support-for-mkv"></a>Compatibilidad con códecs de audio para MPEG

Identificador de Matroska: A_AAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Descripción: Codificación de audio avanzada (AAC)
- Identificadores fourCC o WAV: WAVE_FORMAT_MPEG_HEAAC

Identificador de Matroska: A_AC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3
- Descripción: Dolby AC3
- Identificadores fourCC o WAV: WAVE_FORMAT_DOLBY_AC3_SPDIF

Identificador de Matroska: A_MPEG/L3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3
- Descripción: MPEG Audio Layer-3 (MP3)
- Identificadores fourCC o WAV: WAVE_FORMAT_MPEGLAYER3

Identificador de Matroska: A_MPEG/L1

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Descripción: Carga de audio MPEG-1
- Identificadores fourCC o WAV: WAVE_FORMAT_MPEG

Identificador de Matroska: A_PCM/INT/BIG

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descripción: Audio PCM sin comprimir
- Identificadores fourCC o WAV: WAVE_FORMAT_PCM

Identificador de Matroska: A_PCM/INT/LIT

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM
- Descripción: Audio PCM sin comprimir
- Identificadores fourCC o WAV: WAVE_FORMAT_PCM

Identificador de Matroska: A_PCM/FLOAT/IEEE

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float
- Descripción: audio de punto flotante IEEE sin comprimir
- Identificadores de FourCC o WAV: WAVE_FORMAT_IEEE_FLOAT

Identificador de Matroska: A_ALAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC
- Descripción: Códec de audio sin pérdida de Apple
- Identificadores de FourCC o WAV: 

Identificador de Matroska: A_MPEG/L2

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG
- Descripción: MPEG Audio 1, 2 Capa II
- Identificadores de FourCC o WAV: WAVE_FORMAT_MPEG

Identificador de Matroska: A_DTS

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD
- Descripción: Digital Theater System
- Identificadores de FourCC o WAV: WAVE_FORMAT_DTS

Identificador de Matroska: A_OPUS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus
- Descripción: Indeste
- Identificadores de FourCC o WAV: WAVE_FORMAT_OPUS

Identificador de Matroska: A_VORBIS

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis
- Descripción: Pombis
- Identificadores de FourCC o WAV: 

Identificador de Matroska: A_FLAC

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC
- Descripción: Códec de audio sin pérdida de datos gratuito
- Identificadores de FourCC o WAV: WAVE_FORMAT_FLAC

Identificador de Matroska: A_AAC/MAIN

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC
- Descripción: Codificación de audio avanzada (AAC)
- Identificadores de FourCC o WAV: WAVE_FORMAT_MPEG_HEAAC

Identificador de Matroska: A_EAC3

- MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus
- Descripción: AC-3 mejorado
- Identificadores de FourCC o WAV: 

Identificador de Matroska: A_TRUEHD

- MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD
- Descripción: Dolby TrueHD
- Identificadores de FourCC o WAV: 

Identificador de Matroska: A_MS/ACM

- MSFT Media Foundation MF_MT_SUBTYPE: Mapas a varios WAVE_FORMAT de audio definidos en mmreg.h


### <a name="subtitles-codec-support-for-mkv"></a>Compatibilidad con códecs de subtítulos para MPEG

Identificador de Matroska: S_TEXT/ASCII

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Descripción: texto ASCII

Identificador de Matroska: S_TEXT/UTF8

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT
- Descripción: Texto sin formato UTF-8

Identificador de Matroska: S_TEXT/SSA

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Descripción: Formato de subtítulos

Identificador de Matroska: S_TEXT/ASS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA
- Descripción: Formato avanzado de subtítulos

Identificador de Matroska: S_VOBSUB

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub
- Descripción: Subtítulos vobSub

Identificador de Matroska: S_HDMV/PGS

- MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS
- Descripción: Subtítulos de gráficos de presentación de HDMV (PGS)


## <a name="technical-details-regarding-codecs"></a>Detalles técnicos sobre códecs

Consulte lo siguiente para obtener detalles técnicos sobre códecs.

- [Matroska Codec Specs](http://www.matroska.org/technical/specs/codecid/index.html)
- [GUID de subtipo de audio](audio-subtype-guids.md)
- [GUID de subtipo de vídeo](video-subtype-guids.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de medios admitidos en Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 



