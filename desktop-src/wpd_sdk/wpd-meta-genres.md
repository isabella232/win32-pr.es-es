---
description: El tipo de \_ enumeración WPD META \_ GENRES describe un amplio tipo de género de un archivo multimedia.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: WPD_META_GENRES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 679bc47e2e8439c7f4cd5c3bcf26e6d6897910cfbfcaaaae3fe6dec6c9e0b8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696525"
---
# <a name="wpd_meta_genres-enumeration"></a>Enumeración \_ META \_ GENRES de WPD

El **tipo de \_ enumeración WPD META \_ GENRES** describe un amplio tipo de género de un archivo multimedia.

## <a name="syntax"></a>Syntax


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

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**GÉNERO META \_ WPD \_ SIN \_ USAR**
</dt> <dd>

El género no se ha establecido o no es aplicable.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**ARCHIVO DE \_ AUDIO DE MÚSICA \_ \_ \_ GENÉRICO \_ \_ WPD META GENRE**
</dt> <dd>

Se trata de un archivo de música genérico (solo audio).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**ARCHIVO DE AUDIO GENÉRICO NO MUSIC \_ DE META \_ GENRE \_ \_ \_ \_ DE WPD \_**
</dt> <dd>

Se trata de un archivo de audio genérico que no es de música, por ejemplo, un audiolibrón o voz.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**ARCHIVOS DE \_ AUDIOLIBROS \_ DE PALABRAS \_ \_ HABLADAS DE \_ META-GÉNERO \_ \_ WPD**
</dt> <dd>

Se trata de un archivo de audiolibros.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ META \_ GENRE \_ SPOKEN \_ WORD \_ FILES \_ NON \_ AUDIO \_ BOOK**
</dt> <dd>

Se trata de un archivo de audio de palabra hablada que no es un audiolibrón, por ejemplo, una charla o una voz.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD \_ META \_ GENRE \_ SPOKEN \_ WORD \_ NEWS**
</dt> <dd>

Se trata de un archivo de audio o vídeo de noticias.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD \_ META \_ GENRE \_ SPOKEN \_ WORD \_ TALK \_ SHOWS**
</dt> <dd>

Se trata de una grabación de audio de un programa de presentación.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**ARCHIVO DE \_ VÍDEO GENÉRICO WPD META \_ GENRE \_ \_ \_**
</dt> <dd>

Se trata de un archivo de vídeo genérico.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**ARCHIVO DE \_ VÍDEO DE NOTICIAS DE GÉNERO META \_ \_ \_ \_ WPD**
</dt> <dd>

Se trata de un archivo de vídeo de noticias.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**ARCHIVO DE \_ VÍDEO DE MÚSICA DE META GENRE \_ \_ \_ DE \_ WPD**
</dt> <dd>

Se trata de un archivo de vídeo de música.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**ARCHIVO DE \_ VÍDEO PRINCIPAL WPD META \_ GENRE \_ \_ \_**
</dt> <dd>

Se trata de un archivo de vídeo principal.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**ARCHIVO DE \_ VÍDEO DE LA CARACTERÍSTICA DE GÉNERO \_ \_ META WPD \_ \_ \_**
</dt> <dd>

Se trata de un archivo de vídeo de películas de características.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**ARCHIVO DE \_ VÍDEO DE TELEVISIÓN \_ \_ WPD \_ META GENRE \_**
</dt> <dd>

Se trata de un archivo de vídeo del programa de televisión.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**ARCHIVO DE VÍDEO EDUCATIVO DE APRENDIZAJE DE META \_ \_ GENRE \_ \_ \_ DE \_ WPD**
</dt> <dd>

Se trata de un archivo de vídeo educativo.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**ARCHIVO DE \_ VÍDEO DE MONTAJE DE FOTOS \_ \_ WPD META \_ GENRE \_ \_**
</dt> <dd>

Se trata de un archivo de vídeo que incluye un montaje de fotos.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD \_ META \_ GENRE \_ GENERIC \_ NON \_ AUDIO \_ NON \_ VIDEO**
</dt> <dd>

Se trata de un archivo sin audio o vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**PODCAST DE \_ AUDIO WPD META \_ GENRE \_ \_**
</dt> <dd>

Se trata de un podcast de audio.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**PODCAST DE \_ VÍDEO DE WPD META \_ GENRE \_ \_**
</dt> <dd>

Se trata de un podcast de vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**PODCAST MIXTO \_ DE GÉNERO \_ META \_ WPD \_**
</dt> <dd>

Se trata de un podcast que contiene audio y vídeo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La propiedad META [GENRE de WPD MEDIA usa \_ \_ \_ esta](media-properties.md) enumeración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




