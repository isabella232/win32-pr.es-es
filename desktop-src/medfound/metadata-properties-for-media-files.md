---
description: En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Propiedades de metadatos para archivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466905"
---
# <a name="metadata-properties-for-media-files"></a>Propiedades de metadatos para archivos multimedia

En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.

-   [Propiedades de medios comunes](#common-media-properties)
-   [Propiedades de uso compartido de medios](#media-sharing-properties)
-   [Windows Asignaciones del SDK de formato multimedia](#windows-media-format-sdk-mappings)
-   [Temas relacionados](#related-topics)

## <a name="common-media-properties"></a>Propiedades de medios comunes

El sistema de propiedades de Shell define un conjunto de propiedades de metadatos comunes para todos los tipos de objetos de shell. Un subconjunto de ellos es aplicable a los archivos multimedia. En la tabla siguiente se enumeran las propiedades de Shell más comunes para medios. Los archivos multimedia pueden admitir propiedades adicionales que no aparecen aquí. Además, no todos los formatos de archivo admiten todas las propiedades enumeradas. Para obtener una lista completa de las propiedades de Shell, vea [Propiedades del shell.](/previous-versions//ff521730(v=vs.85))



| PROPERTYKEY                                                              | Nombre del shell                                                                                    | Descripción                                                                                                                                                                                               | Tipo de datos    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [Id. de perfil \_ \_ DLNA de contenido MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md) | None                                                                                          | Identificador de perfil de Digital Living Network Alliance (DLNA).                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ Audio \_ ChannelCount**                                            | [System.Audio.ChannelCount](../properties/props-system-audio-channelcount.md)                       | Número de canales de audio.                                                                                                                                                                                 | VT \_ UI4      |
| **PKEY \_ Audio \_ EncodingBitrate**                                         | [System.Audio.EncodingBitrate](../properties/props-system-audio-encodingbitrate.md)                 | Velocidad de bits de audio media, en bits por segundo.                                                                                                                                                               | VT \_ UI4      |
| **Formato de audio PKEY \_ \_**                                                  | [System.Audio.Format](../properties/props-system-audio-format.md)                                   | Subtipo de audio [**(MF \_ MT \_ SUBTYPE)**](mf-mt-subtype-attribute.md)expresado como una cadena.                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Audio \_ IsVariableBitRate**                                       | [System.Audio.IsVariableBitRate](../properties/props-system-audio-isvariablebitrate.md)             | Indica si la secuencia de audio usa codificación de velocidad de bits variable.                                                                                                                                       | VT \_ BOOL     |
| **PKEY \_ Audio \_ PeakValue**                                               | [System.Audio.PeakValue](../properties/props-system-audio-peakvalue.md)                             | Nivel máximo de volumen de contenido de audio.                                                                                                                                                                       | VT \_ UI4      |
| **PKEY \_ Audio \_ SampleRate**                                              | [System.Audio.SampleRate](../properties/props-system-audio-samplerate.md)                           | Velocidad de muestreo de audio en muestras por segundo. Equivalente al atributo [**MF MT AUDIO SAMPLES PER \_ \_ \_ \_ \_ SECOND**](mf-mt-audio-samples-per-second-attribute.md) en el tipo de medio.                           | VT \_ UI4      |
| **PKEY \_ Audio \_ SampleSize**                                              | [System.Audio.SampleSize](../properties/props-system-audio-samplesize.md)                           | Número de bits por muestra de audio. Equivalente al atributo [**MF MT AUDIO BITS PER \_ \_ \_ \_ \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) en el tipo de medio.                                         | VT \_ UI4      |
| **PKEY \_ Audio \_ StreamNumber**                                            | [System.Audio.StreamNumber](../properties/props-system-audio-streamnumber.md)                       | Identificador de la secuencia de audio.                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ Author**                                                         | [System.Author](../properties/props-system-author.md)                                               | Autor.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **Comentario \_ PKEY**                                                        | [System.Comment](../properties/props-system-comment.md)                                             | Comentario adjunto a un archivo, que normalmente agrega un usuario.                                                                                                                                                  | VT \_ LPWSTR   |
| **PKEY \_ Copyright**                                                      | [System.Copyright](../properties/props-system-copyright.md)                                         | Información de copyright.                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ DRM \_ IsProtected**                                               | [System.DRM.IsProtected](../properties/props-system-drm-isprotected.md)                             | Indica si el contenido está protegido mediante administración de derechos digitales (DRM).                                                                                                                         | VT \_ BOOL     |
| **Palabras \_ clave PKEY**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Palabras clave.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **Lenguaje \_ PKEY**                                                       | [System.Language](../properties/props-system-language.md)                                           | Idioma.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Media \_ AuthorUrl**                                               | [System.Media.AuthorUrl](../properties/props-system-media-authorurl.md)                             | Dirección URL del sitio web del autor.                                                                                                                                                                              | VT \_ LPWSTR   |
| **PKEY \_ Media \_ AverageLevel**                                            | [System.Media.AverageLevel](../properties/props-system-media-averagelevel.md)                       | Nivel medio de volumen de contenido de audio.                                                                                                                                                                    | VT \_ UI4      |
| **PKEY \_ Media \_ ClassPrimaryID**                                          | [System.Media.ClassPrimaryID](../properties/props-system-media-classprimaryid.md)                   | Representación de cadena de un GUID que identifica la clase principal de medios. Para obtener valores válidos, consulte la documentación del [**atributo WM/MediaClassPrimaryID.**](../wmformat/wm-mediaprimaryid.md)       | VT \_ LPWSTR   |
| **PKEY \_ Media \_ ClassSecondaryID**                                        | [System.Media.ClassSecondaryID](../properties/props-system-media-classsecondaryid.md)               | Representación de cadena de un GUID que identifica la clase secundaria de medios. Para obtener valores válidos, vea la documentación del [**atributo WM/MediaClassSecondaryID.**](../wmformat/wm-mediasecondaryid.md) | VT \_ LPWSTR   |
| **PKEY \_ Media \_ CollectionGroupID**                                       | [System.Media.CollectionGroupID](../properties/props-system-media-collectiongroupid.md)             | Representación de cadena de un GUID que identifica el grupo de recopilación.                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Media \_ CollectionID**                                            | [System.Media.CollectionID](../properties/props-system-media-collectionid.md)                       | Representación de cadena de un GUID que identifica la colección.                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ Media \_ ContentDistributor**                                      | [System.Media.ContentDistributor](../properties/props-system-media-contentdistributor.md)           | Distribuidor del contenido.                                                                                                                                                                               | VT \_ LPWSTR   |
| **PKEY \_ Media \_ ContentID**                                               | [System.Media.ContentID](../properties/props-system-media-contentid.md)                             | Representación de cadena de un GUID que identifica la colección.                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ Media \_ DateEncoded**                                             | [System.Media.DateEncoded](../properties/props-system-media-dateencoded.md)                         | Hora a la que se ha codificado el contenido.                                                                                                                                                                        | VT \_ FILETIME |
| **PKEY \_ Media \_ DateReleased**                                            | [System.Media.DateReleased](../properties/props-system-media-datereleased.md)                       | Fecha de lanzamiento original.                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ Media \_ Duration**                                                | [System.Media.Duration](../properties/props-system-media-duration.md)                               | Duración, en unidades de 100 nanosegundos. Equivalente al atributo [**MF \_ PD \_ DURATION**](mf-pd-duration-attribute.md) en el descriptor de presentación.                                                       | VT \_ UI8      |
| **PKEY \_ Media \_ DVDID**                                                   | [System.Media.DVDID](../properties/props-system-media-dvdid.md)                                     | Identificador de disco de vídeo digital (DVDID).                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ Media \_ EncodedBy**                                               | [System.Media.EncodedBy](../properties/props-system-media-encodedby.md)                             | Nombre de la persona o grupo que codifica el contenido.                                                                                                                                                     | VT \_ LPWSTR   |
| **PKEY \_ Media \_ EncodingSettings**                                        | [System.Media.EncodingSettings](../properties/props-system-media-encodingsettings.md)               | Descripción de la configuración utilizada para codificar el contenido.                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Media \_ MCDI**                                                    | [System.Media.MCDI](../properties/props-system-media-mcdi.md)                                       | Música Identificador de CD. Este valor se usa para identificar un CD.                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Media \_ MetadataContentProvider**                                 | [System.Media.MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | Nombre del proveedor de contenido de metadatos. (Por ejemplo, un servicio comercial podría proporcionar metadatos).                                                                                                 | VT \_ LPWSTR   |
| **Productor \_ multimedia PKEY \_**                                                | [System.Media.Producer](../properties/props-system-media-producer.md)                               | Nombre del productor del contenido.                                                                                                                                                                      | VT \_ LPWSTR   |
| **PKEY \_ Media \_ PromotionUrl**                                            | [System.Media.PromotionUrl](../properties/props-system-media-promotionurl.md)                       | Dirección URL de un sitio web que ofrece una promoción relacionada con el contenido.                                                                                                                                             | VT \_ LPWSTR   |
| **Proveedor de \_ medios PKEYRating \_**                                          | [System.Media.ProviderRating](../properties/props-system-media-providerrating.md)                   | Clasificación del contenido según lo asignado por el proveedor de contenido de metadatos.                                                                                                                                       | VT \_ LPWSTR   |
| **PKEY \_ Media \_ ProviderStyle**                                           | [System.Media.ProviderStyle](../properties/props-system-media-providerstyle.md)                     | Estilo o género del contenido según lo asignado por el proveedor de contenido de metadatos.                                                                                                                               | VT \_ LPWSTR   |
| **PKEY \_ Media \_ Publisher**                                               | [System.Media. Publisher](../properties/props-system-media-publisher.md)                             | Editor.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ Media \_ SubTitle**                                                | [System.Media.SubTitle](../properties/props-system-media-subtitle.md)                               | Subtítulo.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Media \_ UniqueFileIdentifier**                                    | [System.Media.UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | Cadena genérica que puede ser para identificar el archivo.                                                                                                                                                        | VT \_ LPWSTR   |
| **PKEY \_ Media \_ Writer**                                                  | [System.Media.Writer](../properties/props-system-media-writer.md)                                   | Escritor.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Media \_ Year**                                                    | [System.Media.Year](../properties/props-system-media-year.md)                                       | Año en que se publicó el contenido.                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ Música \_ AlbumArtist**                                             | [Sistema. Música. AlbumArtist](../properties/props-system-music-albumartist.md)                         | Intérprete principal del álbum. Este atributo se puede usar para distinguir el intérprete principal de un álbum de un intérprete que colaboró en un tema determinado.                                            | VT \_ LPWSTR   |
| **PKEY \_ Música \_ AlbumTitle**                                              | [Sistema. Música. AlbumTitle](../properties/props-system-music-albumtitle.md)                           | Título del álbum.                                                                                                                                                                                              | VT \_ LPWSTR   |
| **PKEY \_ Música \_ Artist**                                                  | [Sistema. Música. Artista](../properties/props-system-music-artist.md)                                   | Artista.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Música \_ BeatsPerMinute**                                          | [Sistema. Música. BeatsPerMinute](../properties/props-system-music-beatsperminute.md)                   | Latidos por minuto.                                                                                                                                                                                         | VT \_ LPWSTR   |
| **PKEY \_ Música \_ Composer**                                                | [Sistema. Música. Composer](../properties/props-system-music-composer.md)                               | Composer.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Música \_ Conductor**                                               | [Sistema. Música. Director de orquesta](../properties/props-system-music-conductor.md)                             | Director.                                                                                                                                                                                                | VT \_ LPWSTR   |
| **PKEY \_ Música \_ ContentGroupDescription**                                 | [Sistema. Música. ContentGroupDescription](../properties/props-system-music-contentgroupdescription.md) | Descripción del grupo de contenido (por ejemplo, conjunto o serie con formato boxed).                                                                                                                                      | VT \_ LPWSTR   |
| **PKEY \_ Música \_ genre**                                                   | [Sistema. Música. Género](../properties/props-system-music-genre.md)                                     | Género.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **PKEY \_ Música \_ InitialKey**                                              | [Sistema. Música. InitialKey](../properties/props-system-music-initialkey.md)                           | Clave inicial de la música.                                                                                                                                                                             | VT \_ LPWSTR   |
| **PKEY \_ Música \_ IsCompilation**                                           | [Sistema. Música. IsCompilation](../properties/props-system-music-iscompilation.md)                     | Indica si el archivo de música forma parte de una compilación.                                                                                                                                                | VT \_ BOOL     |
| **PKEY \_ Música \_ de texto**                                                  | [Sistema. Música. Letras](../properties/props-system-music-lyrics.md)                                   | Letras.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Música \_ Desánimo**                                                    | [Sistema. Música. Humor](../properties/props-system-music-mood.md)                                       | Humor.                                                                                                                                                                                                     | VT \_ LPWSTR   |
| **PKEY \_ Música \_ PartOfSet**                                               | [Sistema. Música. PartOfSet](../properties/props-system-music-partofset.md)                             | Número de elemento y número total de partes del conjunto al que pertenece el archivo, separados por una barra diagonal.                                                                                                 | VT \_ LPWSTR   |
| **Período de \_ Música \_ PKEY**                                                  | [Sistema. Música. Período](../properties/props-system-music-period.md)                                   | Período.                                                                                                                                                                                                   | VT \_ LPWSTR   |
| **PKEY \_ Música \_ TrackNumber**                                             | [Sistema. Música. TrackNumber](../properties/props-system-music-tracknumber.md)                         | Número de seguimiento.                                                                                                                                                                                             | VT \_ UI4      |
| **PKEY \_ ParentalRating**                                                 | [System.ParentalRating](../properties/props-system-parentalrating.md)                               | Clasificación parental.                                                                                                                                                                                          | VT \_ LPWSTR   |
| **PKEY \_ ParentalRatingReason**                                           | [System.ParentalRatingReason](../properties/props-system-parentalratingreason.md)                   | Motivos de la clasificación parental asignada.                                                                                                                                                                 | VT \_ LPWSTR   |
| **Clasificación \_ PKEY**                                                         | [System.Rating](../properties/props-system-rating.md)                                               | Clasificación de usuarios.                                                                                                                                                                                              | VT \_ UI4      |
| **PKEY \_ ThumbnailStream**                                                | [System.ThumbnailStream](../properties/props-system-thumbnailstream.md)                             | Imagen en miniatura.                                                                                                                                                                                          | VT \_ STREAM   |
| **PKEY \_ Title**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Título.                                                                                                                                                                                                    | VT \_ LPWSTR   |
| **Compresión de vídeo PKEY \_ \_**                                             | [System.Video.Compression](../properties/props-system-video-compression.md)                         | Subtipo de vídeo [**(MF \_ MT \_ SUBTYPE)**](mf-mt-subtype-attribute.md)expresado como una cadena.                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Video \_ Director**                                                | [System.Video.Director](../properties/props-system-video-director.md)                               | Director.                                                                                                                                                                                                 | VT \_ LPWSTR   |
| **PKEY \_ Video \_ EncodingBitrate**                                         | [System.Video.EncodingBitrate](../properties/props-system-video-encodingbitrate.md)                 | Velocidad de bits de vídeo media, en bits por segundo.                                                                                                                                                               | VT \_ UI4      |
| **PKEY \_ Video \_ FourCC**                                                  | [System.Video.FourCC](../properties/props-system-video-fourcc.md)                                   | **FOURCC del** formato de codificación de vídeo. Solo se aplica si el subtipo de vídeo se puede expresar como **un valor FOURCC.**                                                                                    | VT \_ UI4      |
| **Fotograma de \_ vídeo PKEYHeight \_**                                             | [System.Video.FrameHeight](../properties/props-system-video-frameheight.md)                         | Alto del fotograma de vídeo.                                                                                                                                                                                       | VT \_ UI4      |
| **PKEY \_ Video \_ FrameRate**                                               | [System.Video.FrameRate](../properties/props-system-video-framerate.md)                             | Velocidad de fotogramas de vídeo, expresada como fotogramas por × 1000.                                                                                                                                                  | VT \_ UI4      |
| **Fotograma de \_ vídeo \_ PKEYWidth**                                              | [System.Video.FrameWidth](../properties/props-system-video-framewidth.md)                           | Ancho del fotograma de vídeo.                                                                                                                                                                                        | VT \_ UI4      |
| **Vídeo PKEY \_ \_ HorizontalAspectRatio**                                   | [System.Video.HorizontalAspectRatio](../properties/props-system-video-horizontalaspectratio.md)     | Componente horizontal de la relación de aspecto de píxeles. (Equivalente al numerador del atributo [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio).          | VT \_ UI4      |
| **PKEY \_ Video \_ IsStereo**                                                | [System.Video.IsStereo](/previous-versions//mt744507(v=vs.85))                                     | Indica si la secuencia de vídeo contiene contenido de vídeo estéreo.                                                                                                                                         | VT \_ BOOL     |
| **PKEY \_ Video \_ StreamNumber**                                            | [System.Video.StreamNumber](../properties/props-system-video-streamnumber.md)                       | Identificador de la secuencia de vídeo.                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ Video \_ TotalBitrate**                                            | [System.Video.TotalBitrate](../properties/props-system-video-totalbitrate.md)                       | Velocidad total de datos de todas las secuencias de vídeo y audio, en bits por segundo. (Solo se aplica a archivos con al menos una secuencia de vídeo).                                                                              | VT \_ UI4      |
| **Vídeo PKEY \_ \_ VerticalAspectRatio**                                     | [System.Video.VerticalAspectRatio](../properties/props-system-video-verticalaspectratio.md)         | Componente vertical de la relación de aspecto de píxeles. (Equivalente al denominador del atributo [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio).          | VT \_ UI4      |



 

## <a name="media-sharing-properties"></a>Propiedades de uso compartido de medios

Para que un archivo multimedia sea compatible con la característica Uso compartido de medios, el controlador de propiedades debe exponer las siguientes propiedades de metadatos. Estas propiedades permiten al servicio Uso compartido de medios ofrecer las opciones adecuadas para transcodificar el contenido en diferentes formatos o velocidades de bits.

-   [Id. de perfil \_ \_ DLNA de contenido MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md)
-   **PKEY \_ Audio \_ ChannelCount**
-   **PKEY \_ Audio \_ EncodingBitrate**
-   **Formato de audio PKEY \_ \_**
-   **PKEY \_ Audio \_ SampleRate** (opcional)
-   **PKEY \_ Audio \_ SampleSize** (opcional)
-   **PKEY \_ DRM \_ IsProtected (necesario** para el contenido DRM)
-   **PKEY \_ Media \_ Duration**
-   **Compresión de vídeo PKEY \_ \_**
-   **PKEY \_ Video \_ EncodingBitrate**
-   **PKEY \_ Video \_ FOURCC**
-   **Fotograma de \_ vídeo PKEYHeight \_**
-   **PKEY \_ Velocidad \_ de fotogramas de** vídeo (opcional)
-   **Fotograma de \_ vídeo PKEYWidth \_**
-   **PKEY \_ Video \_ TotalBitrate**

La **propiedad \_ \_ IsProtected de DRM** de PKEY es necesaria si el contenido está protegido mediante DRM. De lo contrario, esta propiedad es opcional.

Las **propiedades PKEY \_ Audio \_ SampleRate**, **PKEY Audio \_ \_ SampleSize** y **PKEY Video \_ \_ FrameRate** son opcionales. El servicio Uso compartido de medios los expondrá si están disponibles.

Las propiedades del grupo PKEY Audio _ solo se aplican a los archivos con una secuencia de audio, y las propiedades del grupo **\_ \_ \* *_* PKEY \_ Video \_ \*** solo se aplican a los archivos con una secuencia de vídeo.

## <a name="windows-media-format-sdk-mappings"></a>Windows Asignaciones del SDK de formato multimedia

El origen de medios de ASF asigna las siguientes claves de propiedad a los atributos de encabezado de ASF. En algunos casos, los tipos de datos difieren entre la propiedad Shell y el atributo format SDK.



| PROPERTYKEY                              | Atributo del SDK de formato                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **PKEY \_ Audio \_ IsVariableBitRate**       | [**IsVBR**](../wmformat/isvbr.md)                                           |
| **PKEY \_ Audio \_ PeakValue**               | [**PeakValue**](../wmformat/peakvalue.md)                                   |
| **PKEY \_ Author**                         | [**Autor**](../wmformat/author.md)                                         |
| **Comentario \_ PKEY**                        | [**Descripción**](../wmformat/description.md)                               |
| **PKEY \_ Copyright**                      | [**Copyright**](../wmformat/copyright.md)                                   |
| **PKEY \_ DRM \_ IsProtected**               | [**Está \_ protegido**](../wmformat/is-protected.md)                            |
| **Palabras \_ clave PKEY**                       | [**WM/Category**](../wmformat/wm-category.md)                               |
| **Lenguaje \_ PKEY**                       | [**WM/Language**](../wmformat/wm-language.md)                               |
| **PKEY \_ Media \_ AuthorUrl**               | [**WM/AuthorURL**](../wmformat/wm-authorurl.md)                             |
| **PKEY \_ Media \_ AverageLevel**            | [**AverageLevel**](../wmformat/averagelevel.md)                             |
| **PKEY \_ Media \_ ClassPrimaryID**          | [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md)              |
| **PKEY \_ Media \_ ClassSecondaryID**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **PKEY \_ Media \_ CollectionGroupID**       | [**WM/WMCollectionGroupID**](../wmformat/wm-wmcollectiongroupid.md)         |
| **PKEY \_ Media \_ CollectionID**            | [**WM/WMCollectionID**](../wmformat/wm-wmcollectionid.md)                   |
| **PKEY \_ Media \_ ContentDistributor**      | [**WM/ContentDistributor**](../wmformat/wm-contentdistributor.md)           |
| **PKEY \_ Media \_ ContentID**               | [**WM/WMContentID**](../wmformat/wm-wmcontentid.md)                         |
| **PKEY \_ Media \_ DateEncoded**             | [**WM/EncodingTime**](../wmformat/wm-encodingtime.md)                       |
| **PKEY \_ Media \_ DateReleased**            | [**WM/OriginalReleaseTime**](../wmformat/wm-originalreleasetime.md)         |
| **PKEY \_ Media \_ DVDID**                   | [**WM/DVDID**](../wmformat/wm-dvdid.md)                                     |
| **PKEY \_ Media \_ EncodedBy**               | [**WM/EncodedBy**](../wmformat/wm-encodedby.md)                             |
| **PKEY \_ Media \_ EncodingSettings**        | [**WM/EncodingSettings**](../wmformat/wm-encodingsettings.md)               |
| **PKEY \_ Media \_ MCDI**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **PKEY \_ Media \_ MetadataContentProvider** | [**WM/Proveedor**](../wmformat/wm-provider.md)                               |
| **Productor \_ multimedia PKEY \_**                | [**WM/Producer**](../wmformat/wm-producer.md)                               |
| **PKEY \_ Media \_ PromotionUrl**            | [**WM/PromotionURL**](../wmformat/wm-promotionurl.md)                       |
| **Proveedor de \_ medios PKEYRating \_**          | [**WM/ProviderRating**](../wmformat/wm-providerrating.md)                   |
| **PKEY \_ Media \_ ProviderStyle**           | [**WM/ProviderStyle**](../wmformat/wm-providerstyle.md)                     |
| **PKEY \_ Media \_ Publisher**               | [**WM/Publisher**](../wmformat/wm-publisher.md)                             |
| **PKEY \_ Media \_ SubTitle**                | [**WM/SubTitleDescription**](../wmformat/wm-subtitledescription.md)         |
| **PKEY \_ Media \_ UniqueFileIdentifier**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **Escritor \_ multimedia PKEY \_**                  | [**WM/Writer**](../wmformat/wm-writer.md)                                   |
| **Año \_ multimedia PKEY \_**                    | [**WM/Year**](../wmformat/wm-year.md)                                       |
| **PKEY \_ Música \_ AlbumArtist**             | [**WM/AlbumArtist**](../wmformat/wm-albumartist.md)                         |
| **PKEY \_ Música \_ AlbumTitle**              | [**WM/AlbumTitle**](../wmformat/wm-albumtitle.md)                           |
| **PKEY \_ Música \_ Artist**                  | [**Autor**](../wmformat/author.md)                                         |
| **PKEY \_ Música \_ BeatsPerMinute**          | [**WM/BeatsPerMinute**](../wmformat/wm-beatsperminute.md)                   |
| **PKEY \_ Música \_ Composer**                | [**WM/Composer**](../wmformat/wm-composer.md)                               |
| **PKEY \_ Música \_ Conductor**               | [**WM/Conductor**](../wmformat/wm-conductor.md)                             |
| **PKEY \_ Música \_ ContentGroupDescription** | [**WM/ContentGroupDescription**](../wmformat/wm-contentgroupdescription.md) |
| **PKEY \_ Música \_ genre**                   | [**WM/Genre**](../wmformat/wm-genre.md)                                     |
| **PKEY \_ Música \_ InitialKey**              | [**WM/InitialKey**](../wmformat/wm-initialkey.md)                           |
| **PKEY \_ Música \_ IsCompilation**           | **WM/IsCompilation**                                                  |
| **PKEY \_ Música \_ de texto**                  | [**WM/Desa,**](../wmformat/wm-lyrics.md)                                   |
| **PKEY \_ Música \_ Desánimo**                    | [**WM/Estados de ánimo**](../wmformat/wm-mood.md)                                       |
| **PKEY \_ Música \_ PartOfSet**               | [**WM/PartOfSet**](../wmformat/wm-partofset.md)                             |
| **Período de Música PKEY \_ \_**                  | [**WM/Period**](../wmformat/wm-period.md)                                   |
| **PKEY \_ Música \_ TrackNumber**             | [**WM/TrackNumber**](../wmformat/wm-tracknumber.md)                         |
| **PKEY \_ ParentalRating**                 | [**WM/ParentalRating**](../wmformat/wm-parentalrating.md)                   |
| **PKEY \_ ParentalRatingReason**           | [**WM/ParentalRatingReason**](../wmformat/wm-parentalratingreason.md)       |
| **Clasificación \_ PKEY**                         | [**WM/SharedUserRating**](../wmformat/wm-shareduserrating.md)               |
| **PKEY \_ ThumbnailStream**                | [**WM/Picture**](../wmformat/wmpicture.md)                       |
| **PKEY \_ Title**                          | [**Título**](../wmformat/title.md)                                           |
| **PKEY \_ Video \_ Director**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos multimedia](media-metadata.md)
</dt> <dt>

[Proveedores de metadatos de shell](shell-metadata-providers.md)
</dt> </dl>

 

 
