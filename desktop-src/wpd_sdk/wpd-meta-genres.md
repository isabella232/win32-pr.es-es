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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="5f429-103">\_ \_ Enumeración de metagéneros de WPD</span><span class="sxs-lookup"><span data-stu-id="5f429-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="5f429-104">El tipo de enumeración de **\_ meta \_ géneros de WPD** describe un tipo de género amplio de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="5f429-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f429-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f429-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="5f429-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5f429-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5f429-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_meta Genre de WPD \_ \_ sin usar**</span><span class="sxs-lookup"><span data-stu-id="5f429-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-108">No se ha establecido el género o no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5f429-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_archivo de \_ \_ audio de \_ música \_ genérico de meta de metagénero de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-110">Se trata de un archivo de música genérico (solo audio).</span><span class="sxs-lookup"><span data-stu-id="5f429-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="5f429-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_archivo de \_ \_ \_ \_ audio no musical \_ \_ genérico de metagénero de WPD**</span><span class="sxs-lookup"><span data-stu-id="5f429-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-112">Se trata de un archivo de audio no musical genérico, por ejemplo, un libro de voz o de audio.</span><span class="sxs-lookup"><span data-stu-id="5f429-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_archivos de \_ \_ libro de \_ audio de Word orales \_ de \_ metagénero \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="5f429-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-114">Se trata de un archivo de libro de audio.</span><span class="sxs-lookup"><span data-stu-id="5f429-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**\_meta de \_ metagénero de WPD archivos de \_ \_ Word archivos de palabras \_ no de \_ \_ audio \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-116">Se trata de un archivo de audio hablado que no es un libro de audio, por ejemplo, una entrevista o una voz.</span><span class="sxs-lookup"><span data-stu-id="5f429-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_ \_ \_ \_ palabra \_ News de metagénero de WPD de WPD**</span><span class="sxs-lookup"><span data-stu-id="5f429-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-118">Se trata de un archivo de audio o vídeo de noticias.</span><span class="sxs-lookup"><span data-stu-id="5f429-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**META de metagénero de WPD de la \_ \_ voz de \_ \_ Word \_ Talk \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-120">Se trata de una grabación de audio de un programa de conversación.</span><span class="sxs-lookup"><span data-stu-id="5f429-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_archivo de \_ \_ vídeo genérico \_ de meta de metagénero de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-122">Se trata de un archivo de vídeo genérico.</span><span class="sxs-lookup"><span data-stu-id="5f429-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_archivo de vídeo de noticias de meta de \_ metagénero de \_ \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-124">Este es un archivo de vídeo de noticias.</span><span class="sxs-lookup"><span data-stu-id="5f429-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_archivo de vídeo de música de meta de \_ metagénero de \_ \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-126">Se trata de un archivo de vídeo musical.</span><span class="sxs-lookup"><span data-stu-id="5f429-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_archivo de \_ \_ vídeo principal \_ de meta Genre de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-128">Este es un archivo de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="5f429-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**archivo de vídeo de película de la \_ \_ característica meta Genre \_ \_ \_ \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="5f429-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-130">Se trata de un archivo de vídeo de película de características.</span><span class="sxs-lookup"><span data-stu-id="5f429-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_archivo de vídeo de televisión de meta de \_ metagénero de \_ \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-132">Este es un archivo de vídeo de programa de televisión.</span><span class="sxs-lookup"><span data-stu-id="5f429-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_archivo de \_ \_ \_ vídeo educativo de aprendizaje de \_ metagénero de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="5f429-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-134">Se trata de un archivo de vídeo educativo.</span><span class="sxs-lookup"><span data-stu-id="5f429-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_archivo de \_ \_ vídeo fotográfico \_ \_ meta de metagénero de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-136">Se trata de un archivo de vídeo que incluye un Collage fotográfico.</span><span class="sxs-lookup"><span data-stu-id="5f429-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**\_meta de \_ metagénero de WPD genérico no \_ \_ \_ audio \_ sin \_ vídeo**</span><span class="sxs-lookup"><span data-stu-id="5f429-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-138">Se trata de un archivo sin audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f429-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_podcast de audio de meta Genre de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-140">Se trata de un podcast de audio.</span><span class="sxs-lookup"><span data-stu-id="5f429-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast de vídeo de meta Genre de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-142">Este es un podcast de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f429-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="5f429-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ podcast mezclado de meta Genre de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5f429-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="5f429-144">Se trata de un podcast que contiene audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f429-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f429-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f429-145">Remarks</span></span>

<span data-ttu-id="5f429-146">Esta enumeración la usa la [propiedad \_ \_ meta de \_ metadatos multimedia WPD](media-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5f429-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f429-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f429-147">Requirements</span></span>



| <span data-ttu-id="5f429-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f429-148">Requirement</span></span> | <span data-ttu-id="5f429-149">Value</span><span class="sxs-lookup"><span data-stu-id="5f429-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f429-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f429-150">Header</span></span><br/> | <dl> <span data-ttu-id="5f429-151"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f429-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f429-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f429-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f429-153">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="5f429-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




