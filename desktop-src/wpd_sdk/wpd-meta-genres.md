---
description: El \_ \_ tipo de enumeración de meta géneros de WPD describe un tipo de género amplio de un archivo multimedia.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: Enumeración WPD_META_GENRES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699358"
---
# <a name="wpd_meta_genres-enumeration"></a>\_ \_ Enumeración de metagéneros de WPD

El tipo de enumeración de **\_ meta \_ géneros de WPD** describe un tipo de género amplio de un archivo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_meta Genre de WPD \_ \_ sin usar**
</dt> <dd>

No se ha establecido el género o no es aplicable.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_archivo de \_ \_ audio de \_ música \_ genérico de meta de metagénero de WPD \_**
</dt> <dd>

Se trata de un archivo de música genérico (solo audio).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_archivo de \_ \_ \_ \_ audio no musical \_ \_ genérico de metagénero de WPD**
</dt> <dd>

Se trata de un archivo de audio no musical genérico, por ejemplo, un libro de voz o de audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_archivos de \_ \_ libro de \_ audio de Word orales \_ de \_ metagénero \_ de WPD**
</dt> <dd>

Se trata de un archivo de libro de audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_meta de \_ metagénero de WPD archivos de \_ \_ Word archivos de palabras \_ no de \_ \_ audio \_**
</dt> <dd>

Se trata de un archivo de audio hablado que no es un libro de audio, por ejemplo, una entrevista o una voz.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_ \_ \_ \_ palabra \_ News de metagénero de WPD de WPD**
</dt> <dd>

Se trata de un archivo de audio o vídeo de noticias.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**META de metagénero de WPD de la \_ \_ voz de \_ \_ Word \_ Talk \_**
</dt> <dd>

Se trata de una grabación de audio de un programa de conversación.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_archivo de \_ \_ vídeo genérico \_ de meta de metagénero de WPD \_**
</dt> <dd>

Se trata de un archivo de vídeo genérico.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_archivo de vídeo de noticias de meta de \_ metagénero de \_ \_ WPD \_**
</dt> <dd>

Este es un archivo de vídeo de noticias.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_archivo de vídeo de música de meta de \_ metagénero de \_ \_ WPD \_**
</dt> <dd>

Se trata de un archivo de vídeo musical.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_archivo de \_ \_ vídeo principal \_ de meta Genre de WPD \_**
</dt> <dd>

Este es un archivo de vídeo principal.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**archivo de vídeo de película de la \_ \_ característica meta Genre \_ \_ \_ \_ de WPD**
</dt> <dd>

Se trata de un archivo de vídeo de película de características.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_archivo de vídeo de televisión de meta de \_ metagénero de \_ \_ WPD \_**
</dt> <dd>

Este es un archivo de vídeo de programa de televisión.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_archivo de \_ \_ \_ vídeo educativo de aprendizaje de \_ metagénero de \_ WPD**
</dt> <dd>

Se trata de un archivo de vídeo educativo.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_archivo de \_ \_ vídeo fotográfico \_ \_ meta de metagénero de WPD \_**
</dt> <dd>

Se trata de un archivo de vídeo que incluye un Collage fotográfico.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_meta de \_ metagénero de WPD genérico no \_ \_ \_ audio \_ sin \_ vídeo**
</dt> <dd>

Se trata de un archivo sin audio o vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_podcast de audio de meta Genre de WPD \_ \_ \_**
</dt> <dd>

Se trata de un podcast de audio.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast de vídeo de meta Genre de WPD \_ \_ \_**
</dt> <dd>

Este es un podcast de vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ podcast mezclado de meta Genre de WPD \_**
</dt> <dd>

Se trata de un podcast que contiene audio y vídeo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la [propiedad \_ \_ meta de \_ metadatos multimedia WPD](media-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




