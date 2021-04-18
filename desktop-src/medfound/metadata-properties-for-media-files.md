---
description: En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Propiedades de metadatos para archivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707528"
---
# <a name="metadata-properties-for-media-files"></a>Propiedades de metadatos para archivos multimedia

En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.

-   [Propiedades de medios comunes](#common-media-properties)
-   [Propiedades de uso compartido de multimedia](#media-sharing-properties)
-   [Asignaciones del SDK de Windows Media Format](#windows-media-format-sdk-mappings)
-   [Temas relacionados](#related-topics)

## <a name="common-media-properties"></a>Propiedades de medios comunes

El sistema de propiedades de Shell define un conjunto de propiedades de metadatos comunes para todos los tipos de objetos de Shell. Un subconjunto de estos elementos se aplican a los archivos multimedia. En la tabla siguiente se enumeran las propiedades de Shell más comunes para los medios. Los archivos multimedia pueden admitir propiedades adicionales que no se muestran aquí. Además, no todos los formatos de archivo admiten todas las propiedades enumeradas. Para obtener una lista completa de las propiedades del shell, consulte [propiedades de Shell](/previous-versions//ff521730(v=vs.85)).



| PROPERTYKEY                                                              | Nombre de Shell                                                                                    | Descripción                                                                                                                                                                                               | Tipo de datos    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [\_Identificador de \_ Perfil de DLNA de contenido de MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md) | None                                                                                          | Identificador de Perfil de Digital Living Network Alliance (DLNA).                                                                                                                                                | VT \_ LPWStr   |
| **\_ChannelCount de audio PKEY \_**                                            | [System. audio. ChannelCount](../properties/props-system-audio-channelcount.md)                       | Número de canales de audio.                                                                                                                                                                                 | VT \_ UI4      |
| **\_EncodingBitrate de audio PKEY \_**                                         | [System. audio. EncodingBitrate](../properties/props-system-audio-encodingbitrate.md)                 | Velocidad media de bits de audio, en bits por segundo.                                                                                                                                                               | VT \_ UI4      |
| **\_Formato de audio PKEY \_**                                                  | [System. audio. Format](../properties/props-system-audio-format.md)                                   | Subtipo de audio [**( \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)) expresado como una cadena.                                                                                                                 | VT \_ LPWStr   |
| **\_IsVariableBitRate de audio PKEY \_**                                       | [System. audio. IsVariableBitRate](../properties/props-system-audio-isvariablebitrate.md)             | Indica si la secuencia de audio utiliza codificación de velocidad de bits variable.                                                                                                                                       | VT \_ bool     |
| **\_PeakValue de audio PKEY \_**                                               | [System. audio. PeakValue](../properties/props-system-audio-peakvalue.md)                             | Nivel máximo de volumen de contenido de audio.                                                                                                                                                                       | VT \_ UI4      |
| **\_SampleRate de audio PKEY \_**                                              | [System. audio. SampleRate](../properties/props-system-audio-samplerate.md)                           | Velocidad de muestra de audio en muestras por segundo. Equivalente al atributo [**MF \_ MT \_ audio \_ Samples \_ per \_ Second**](mf-mt-audio-samples-per-second-attribute.md) en el tipo de medio.                           | VT \_ UI4      |
| **\_Muestreador de audio PKEY \_**                                              | [System. audio. Sampler](../properties/props-system-audio-samplesize.md)                           | Número de bits por muestra de audio. Equivalente al atributo [**MF \_ MT \_ audio \_ \_ por \_ ejemplo**](mf-mt-audio-bits-per-sample-attribute.md) en el tipo de medio.                                         | VT \_ UI4      |
| **\_StreamNumber de audio PKEY \_**                                            | [System. audio. StreamNumber](../properties/props-system-audio-streamnumber.md)                       | Identificador de la secuencia de audio.                                                                                                                                                                           | VT \_ UI4      |
| **Autor de PKEY \_**                                                         | [System.Author](../properties/props-system-author.md)                                               | Frente.                                                                                                                                                                                                   | VT \_ LPWStr   |
| **\_Comentario PKEY**                                                        | [System. Comment](../properties/props-system-comment.md)                                             | Comentario adjuntado a un archivo, normalmente agregado por un usuario.                                                                                                                                                  | VT \_ LPWStr   |
| **Copyright de PKEY \_**                                                      | [System. Copyright](../properties/props-system-copyright.md)                                         | Información de copyright.                                                                                                                                                                                    | VT \_ LPWStr   |
| **PKEY \_ DRM \_ IsProtected**                                               | [System. DRM. IsProtected](../properties/props-system-drm-isprotected.md)                             | Indica si el contenido está protegido mediante administración de derechos digitales (DRM).                                                                                                                         | VT \_ bool     |
| **\_Palabras clave de PKEY**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Palabra.                                                                                                                                                                                                 | VT \_ LPWStr   |
| **\_Lenguaje PKEY**                                                       | [System. Language](../properties/props-system-language.md)                                           | Idioma.                                                                                                                                                                                                 | VT \_ LPWStr   |
| **PKEY \_ media \_ AuthorUrl**                                               | [System. Media. AuthorUrl](../properties/props-system-media-authorurl.md)                             | Dirección URL del sitio web del autor.                                                                                                                                                                              | VT \_ LPWStr   |
| **PKEY \_ media \_ AverageLevel**                                            | [System. Media. AverageLevel](../properties/props-system-media-averagelevel.md)                       | Nivel de volumen medio de contenido de audio.                                                                                                                                                                    | VT \_ UI4      |
| **PKEY \_ media \_ ClassPrimaryID**                                          | [System. Media. ClassPrimaryID](../properties/props-system-media-classprimaryid.md)                   | Representación de cadena de un GUID que identifica la clase principal de los elementos multimedia. Para obtener información sobre los valores válidos, consulte la documentación del atributo [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md) .       | VT \_ LPWStr   |
| **PKEY \_ media \_ ClassSecondaryID**                                        | [System. Media. ClassSecondaryID](../properties/props-system-media-classsecondaryid.md)               | Representación de cadena de un GUID que identifica la clase secundaria de los elementos multimedia. Para obtener información sobre los valores válidos, consulte la documentación del atributo [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md) . | VT \_ LPWStr   |
| **PKEY \_ media \_ CollectionGroupID**                                       | [System. Media. CollectionGroupID](../properties/props-system-media-collectiongroupid.md)             | Representación de cadena de un GUID que identifica el grupo de recopilación.                                                                                                                                 | VT \_ LPWStr   |
| **PKEY \_ media \_ CollectionID**                                            | [System. Media. CollectionID](../properties/props-system-media-collectionid.md)                       | Representación de cadena de un GUID que identifica la colección.                                                                                                                                       | VT \_ LPWStr   |
| **PKEY \_ media \_ ContentDistributor**                                      | [System. Media. ContentDistributor](../properties/props-system-media-contentdistributor.md)           | Distribuidor del contenido.                                                                                                                                                                               | VT \_ LPWStr   |
| **PKEY \_ media \_ contentid**                                               | [System. Media. ContentID](../properties/props-system-media-contentid.md)                             | Representación de cadena de un GUID que identifica la colección.                                                                                                                                       | VT \_ LPWStr   |
| **PKEY \_ media \_ DateEncoded**                                             | [System. Media. DateEncoded](../properties/props-system-media-dateencoded.md)                         | Hora en la que se ha codificado el contenido.                                                                                                                                                                        | VT \_ FILETIME |
| **PKEY \_ media \_ DateReleased**                                            | [System. Media. DateReleased](../properties/props-system-media-datereleased.md)                       | Fecha de lanzamiento original.                                                                                                                                                                                    | VT \_ LPWStr   |
| **\_Duración del medio de PKEY \_**                                                | [System. Media. Duration](../properties/props-system-media-duration.md)                               | Duración, en unidades de 100-nanosegundos. Equivalente al atributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) en el descriptor de presentación.                                                       | VT \_ UI8      |
| **PKEY \_ media \_ DVDID**                                                   | [System. Media. DVDID](../properties/props-system-media-dvdid.md)                                     | Identificador del disco de vídeo digital (DVDID).                                                                                                                                                                    | VT \_ LPWStr   |
| **PKEY \_ media \_ EncodedBy**                                               | [System. Media. EncodedBy](../properties/props-system-media-encodedby.md)                             | Nombre de la persona o grupo que ha codificado el contenido.                                                                                                                                                     | VT \_ LPWStr   |
| **PKEY \_ media \_ EncodingSettings**                                        | [System. Media. EncodingSettings](../properties/props-system-media-encodingsettings.md)               | Descripción de la configuración utilizada para codificar el contenido.                                                                                                                                                   | VT \_ LPWStr   |
| **PKEY \_ media \_ MCDI**                                                    | [System. Media. MCDI](../properties/props-system-media-mcdi.md)                                       | Identificador del CD de música. Este valor se usa para identificar un CD.                                                                                                                                                 | VT \_ LPWStr   |
| **PKEY \_ media \_ MetadataContentProvider**                                 | [System. Media. MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | Nombre del proveedor de contenido de metadatos. (Por ejemplo, un servicio comercial podría proporcionar los metadatos).                                                                                                 | VT \_ LPWStr   |
| **\_Productor multimedia \_ PKEY**                                                | [System. Media. Producer](../properties/props-system-media-producer.md)                               | Nombre del productor del contenido.                                                                                                                                                                      | VT \_ LPWStr   |
| **PKEY \_ media \_ PromotionUrl**                                            | [System. Media. PromotionUrl](../properties/props-system-media-promotionurl.md)                       | Dirección URL de un sitio web que ofrece una promoción relacionada con el contenido.                                                                                                                                             | VT \_ LPWStr   |
| **PKEY \_ media \_ ProviderRating**                                          | [System. Media. ProviderRating](../properties/props-system-media-providerrating.md)                   | Clasificación del contenido asignado por el proveedor de contenido de metadatos.                                                                                                                                       | VT \_ LPWStr   |
| **PKEY \_ media \_ ProviderStyle**                                           | [System. Media. ProviderStyle](../properties/props-system-media-providerstyle.md)                     | Estilo o género del contenido asignado por el proveedor de contenido de metadatos.                                                                                                                               | VT \_ LPWStr   |
| **PKEY \_ media \_ Publisher**                                               | [System. Media. Publisher](../properties/props-system-media-publisher.md)                             | Editor.                                                                                                                                                                                                | VT \_ LPWStr   |
| **\_Subtítulo multimedia PKEY \_**                                                | [System. Media. subtítulo](../properties/props-system-media-subtitle.md)                               | Subtítulo.                                                                                                                                                                                                 | VT \_ LPWStr   |
| **PKEY \_ media \_ UniqueFileIdentifier**                                    | [System. Media. UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | Cadena genérica que puede ser para identificar el archivo.                                                                                                                                                        | VT \_ LPWStr   |
| **PKEY \_ media \_ Writer**                                                  | [System. Media. Writer](../properties/props-system-media-writer.md)                                   | Escritor.                                                                                                                                                                                                   | VT \_ LPWStr   |
| **PKEY \_ \_ año multimedia**                                                    | [System. Media. Year](../properties/props-system-media-year.md)                                       | Año en que se publicó el contenido.                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ Music \_ AlbumArtist**                                             | [System. Music. AlbumArtist](../properties/props-system-music-albumartist.md)                         | Intérprete principal del álbum. Este atributo se puede usar para distinguir el intérprete principal de un álbum de un artista que colaboró en una determinada pista.                                            | VT \_ LPWStr   |
| **PKEY \_ Music \_ álbum**                                              | [System. Music. álbum](../properties/props-system-music-albumtitle.md)                           | Título del álbum.                                                                                                                                                                                              | VT \_ LPWStr   |
| **PKEY \_ Music \_ artista**                                                  | [System. Music. artista](../properties/props-system-music-artist.md)                                   | Artistas.                                                                                                                                                                                                   | VT \_ LPWStr   |
| **PKEY \_ Music \_ BeatsPerMinute**                                          | [System. Music. BeatsPerMinute](../properties/props-system-music-beatsperminute.md)                   | Pulsaciones por minuto.                                                                                                                                                                                         | VT \_ LPWStr   |
| **PKEY \_ Music \_ Composer**                                                | [System. Music. Composer](../properties/props-system-music-composer.md)                               | Compositor.                                                                                                                                                                                                 | VT \_ LPWStr   |
| **\_Conductor de música PKEY \_**                                               | [System. Music. conductores](../properties/props-system-music-conductor.md)                             | Conductor.                                                                                                                                                                                                | VT \_ LPWStr   |
| **PKEY \_ Music \_ ContentGroupDescription**                                 | [System. Music. ContentGroupDescription](../properties/props-system-music-contentgroupdescription.md) | Descripción del grupo de contenido (por ejemplo, conjunto o serie con conversión boxing).                                                                                                                                      | VT \_ LPWStr   |
| **\_Género de música PKEY \_**                                                   | [System. Music. Genre](../properties/props-system-music-genre.md)                                     | Vídeos.                                                                                                                                                                                                    | VT \_ LPWStr   |
| **PKEY \_ Music \_ InitialKey**                                              | [System.Music.InitialKey](../properties/props-system-music-initialkey.md)                           | La clave inicial de la música.                                                                                                                                                                             | VT \_ LPWStr   |
| **PKEY \_ Music \_ IsCompilation**                                           | [System. Music. IsCompilation](../properties/props-system-music-iscompilation.md)                     | Indica si el archivo de música forma parte de una compilación.                                                                                                                                                | VT \_ bool     |
| **PKEY \_ \_ canciones**                                                  | [System. Music. letra](../properties/props-system-music-lyrics.md)                                   | Letra.                                                                                                                                                                                                   | VT \_ LPWStr   |
| **PKEY \_ música \_ ambiente**                                                    | [System. Music. ambiente](../properties/props-system-music-mood.md)                                       | Ánimo.                                                                                                                                                                                                     | VT \_ LPWStr   |
| **PKEY \_ Music \_ PartOfSet**                                               | [System. Music. PartOfSet](../properties/props-system-music-partofset.md)                             | El número de pieza y el número total de elementos del conjunto al que pertenece el archivo, separados por una barra diagonal.                                                                                                 | VT \_ LPWStr   |
| **PKEY de \_ música \_**                                                  | [System. Music. period](../properties/props-system-music-period.md)                                   | Cierto.                                                                                                                                                                                                   | VT \_ LPWStr   |
| **PKEY \_ Music \_ TrackNumber**                                             | [System. Music. TrackNumber](../properties/props-system-music-tracknumber.md)                         | Número de pista.                                                                                                                                                                                             | VT \_ UI4      |
| **PKEY \_ ParentalRating**                                                 | [System. ParentalRating](../properties/props-system-parentalrating.md)                               | Clasificación parental.                                                                                                                                                                                          | VT \_ LPWStr   |
| **PKEY \_ ParentalRatingReason**                                           | [System. ParentalRatingReason](../properties/props-system-parentalratingreason.md)                   | Motivos de la clasificación parental asignada.                                                                                                                                                                 | VT \_ LPWStr   |
| **\_Clasificación PKEY**                                                         | [System. Rating](../properties/props-system-rating.md)                                               | Clasificación de usuario.                                                                                                                                                                                              | VT \_ UI4      |
| **PKEY \_ ThumbnailStream**                                                | [System. ThumbnailStream](../properties/props-system-thumbnailstream.md)                             | Imagen en miniatura.                                                                                                                                                                                          | secuencia de VT \_   |
| **Título de PKEY \_**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Título.                                                                                                                                                                                                    | VT \_ LPWStr   |
| **\_Compresión de vídeo PKEY \_**                                             | [System. video. Compression](../properties/props-system-video-compression.md)                         | Subtipo de vídeo [**( \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)) expresado como una cadena.                                                                                                                 | VT \_ LPWStr   |
| **\_Director de vídeo de PKEY \_**                                                | [System. video. Director](../properties/props-system-video-director.md)                               | DataDirectory.                                                                                                                                                                                                 | VT \_ LPWStr   |
| **PKEY \_ vídeo \_ EncodingBitrate**                                         | [System. video. EncodingBitrate](../properties/props-system-video-encodingbitrate.md)                 | Promedio de velocidad de bits de vídeo, en bits por segundo.                                                                                                                                                               | VT \_ UI4      |
| **PKEY \_ vídeo \_ FourCC**                                                  | [System. video. FourCC](../properties/props-system-video-fourcc.md)                                   | **FourCC** del formato de codificación de vídeo. Solo se aplica si el subtipo de vídeo se puede expresar como un valor de **FourCC** .                                                                                    | VT \_ UI4      |
| **PKEY \_ vídeo \_ FrameHeight**                                             | [System. video. FrameHeight](../properties/props-system-video-frameheight.md)                         | Alto de fotogramas de vídeo.                                                                                                                                                                                       | VT \_ UI4      |
| **\_Fotogramas de vídeo PKEY \_**                                               | [System. video. velocidad de fotogramas](../properties/props-system-video-framerate.md)                             | Velocidad de fotogramas de vídeo, expresada como fotogramas por segundo × 1000.                                                                                                                                                  | VT \_ UI4      |
| **PKEY \_ vídeo \_ FrameWidth**                                              | [System. video. FrameWidth](../properties/props-system-video-framewidth.md)                           | Ancho del fotograma de vídeo.                                                                                                                                                                                        | VT \_ UI4      |
| **PKEY \_ vídeo \_ HorizontalAspectRatio**                                   | [System. video. HorizontalAspectRatio](../properties/props-system-video-horizontalaspectratio.md)     | Componente horizontal de la relación de aspecto de píxeles. (Equivalente al numerador del atributo [**de \_ \_ relación de \_ aspecto \_ de los píxeles MF MT**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio).          | VT \_ UI4      |
| **PKEY \_ vídeo \_ IsStereo**                                                | [System. video. IsStereo](/previous-versions//mt744507(v=vs.85))                                     | Indica si la secuencia de vídeo contiene contenido de vídeo estéreo.                                                                                                                                         | VT \_ bool     |
| **PKEY \_ vídeo \_ StreamNumber**                                            | [System. video. StreamNumber](../properties/props-system-video-streamnumber.md)                       | Identificador de la secuencia de vídeo.                                                                                                                                                                           | VT \_ UI4      |
| **PKEY \_ vídeo \_ TotalBitrate**                                            | [System. video. TotalBitrate](../properties/props-system-video-totalbitrate.md)                       | Velocidad de datos total para todas las secuencias de audio y vídeo, en bits por segundo. (Se aplica solo a los archivos con al menos una secuencia de vídeo).                                                                              | VT \_ UI4      |
| **PKEY \_ vídeo \_ VerticalAspectRatio**                                     | [System. video. VerticalAspectRatio](../properties/props-system-video-verticalaspectratio.md)         | Componente vertical de la relación de aspecto de píxeles. (Equivalente al denominador del atributo de relación de aspecto de los [**\_ \_ píxeles \_ \_ MF MT**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio).          | VT \_ UI4      |



 

## <a name="media-sharing-properties"></a>Propiedades de uso compartido de multimedia

Para que un archivo multimedia sea compatible con la característica de uso compartido de multimedia, el controlador de propiedad debe exponer las siguientes propiedades de metadatos. Estas propiedades permiten al servicio de uso compartido de multimedia ofrecer las opciones adecuadas para transcodificar el contenido en diferentes formatos o velocidades de bits.

-   [\_Identificador de \_ Perfil de DLNA de contenido de MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md)
-   **\_ChannelCount de audio PKEY \_**
-   **\_EncodingBitrate de audio PKEY \_**
-   **\_Formato de audio PKEY \_**
-   **PKEY \_ Audio \_ SampleRate** (opcional)
-   **PKEY \_ \_Muestreador de audio** (opcional)
-   **PKEY \_ DRM \_ IsProtected** (necesario para el contenido DRM)
-   **\_Duración del medio de PKEY \_**
-   **\_Compresión de vídeo PKEY \_**
-   **PKEY \_ vídeo \_ EncodingBitrate**
-   **PKEY \_ vídeo \_ FourCC**
-   **PKEY \_ vídeo \_ FrameHeight**
-   **PKEY \_ \_Fotogramas de vídeo** (opcional)
-   **PKEY \_ vídeo \_ FrameWidth**
-   **PKEY \_ vídeo \_ TotalBitrate**

La propiedad **PKEY de \_ DRM de \_ IsProtected** es necesaria si el contenido está protegido mediante DRM. De lo contrario, esta propiedad es opcional.

Las propiedades **PKEY \_ audio \_ SampleRate**, **PKEY \_ audio \_ muestreator** y **PKEY \_ video \_ fotogramas de vídeo** son opcionales. El servicio de uso compartido de multimedia lo expondrá si están disponibles.

Las propiedades del **\_ Grupo PKEY audio \_ \* *_ _ se aplican solo a los archivos con una secuencia de audio y las propiedades* del grupo de \_ vídeo \_ \* _ PKEY** solo se aplican a los archivos con una secuencia de vídeo.

## <a name="windows-media-format-sdk-mappings"></a>Asignaciones del SDK de Windows Media Format

El origen de medios ASF asigna las siguientes claves de propiedades a los atributos de encabezado ASF. En algunos casos, los tipos de datos difieren entre la propiedad de Shell y el atributo de formato SDK.



| PROPERTYKEY                              | Format (atributo de SDK)                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **\_IsVariableBitRate de audio PKEY \_**       | [**IsVBR**](../wmformat/isvbr.md)                                           |
| **\_PeakValue de audio PKEY \_**               | [**PeakValue**](../wmformat/peakvalue.md)                                   |
| **Autor de PKEY \_**                         | [**Autor**](../wmformat/author.md)                                         |
| **\_Comentario PKEY**                        | [**Descripción**](../wmformat/description.md)                               |
| **Copyright de PKEY \_**                      | [**SSoftware**](../wmformat/copyright.md)                                   |
| **PKEY \_ DRM \_ IsProtected**               | [**Está \_ protegido**](../wmformat/is-protected.md)                            |
| **\_Palabras clave de PKEY**                       | [**WM/categoría**](../wmformat/wm-category.md)                               |
| **\_Lenguaje PKEY**                       | [**WM/lenguaje**](../wmformat/wm-language.md)                               |
| **PKEY \_ media \_ AuthorUrl**               | [**WM/AuthorURL**](../wmformat/wm-authorurl.md)                             |
| **PKEY \_ media \_ AverageLevel**            | [**AverageLevel**](../wmformat/averagelevel.md)                             |
| **PKEY \_ media \_ ClassPrimaryID**          | [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md)              |
| **PKEY \_ media \_ ClassSecondaryID**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **PKEY \_ media \_ CollectionGroupID**       | [**WM/WMCollectionGroupID**](../wmformat/wm-wmcollectiongroupid.md)         |
| **PKEY \_ media \_ CollectionID**            | [**WM/WMCollectionID**](../wmformat/wm-wmcollectionid.md)                   |
| **PKEY \_ media \_ ContentDistributor**      | [**WM/ContentDistributor**](../wmformat/wm-contentdistributor.md)           |
| **PKEY \_ media \_ contentid**               | [**WM/WMContentID**](../wmformat/wm-wmcontentid.md)                         |
| **PKEY \_ media \_ DateEncoded**             | [**WM/EncodingTime**](../wmformat/wm-encodingtime.md)                       |
| **PKEY \_ media \_ DateReleased**            | [**WM/OriginalReleaseTime**](../wmformat/wm-originalreleasetime.md)         |
| **PKEY \_ media \_ DVDID**                   | [**WM/DVDID**](../wmformat/wm-dvdid.md)                                     |
| **PKEY \_ media \_ EncodedBy**               | [**WM/EncodedBy**](../wmformat/wm-encodedby.md)                             |
| **PKEY \_ media \_ EncodingSettings**        | [**WM/EncodingSettings**](../wmformat/wm-encodingsettings.md)               |
| **PKEY \_ media \_ MCDI**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **PKEY \_ media \_ MetadataContentProvider** | [**WM/proveedor**](../wmformat/wm-provider.md)                               |
| **\_Productor multimedia \_ PKEY**                | [**WM/productor**](../wmformat/wm-producer.md)                               |
| **PKEY \_ media \_ PromotionUrl**            | [**WM/PromotionURL**](../wmformat/wm-promotionurl.md)                       |
| **PKEY \_ media \_ ProviderRating**          | [**WM/ProviderRating**](../wmformat/wm-providerrating.md)                   |
| **PKEY \_ media \_ ProviderStyle**           | [**WM/ProviderStyle**](../wmformat/wm-providerstyle.md)                     |
| **PKEY \_ media \_ Publisher**               | [**WM/publicador**](../wmformat/wm-publisher.md)                             |
| **\_Subtítulo multimedia PKEY \_**                | [**WM/SubTitleDescription**](../wmformat/wm-subtitledescription.md)         |
| **PKEY \_ media \_ UniqueFileIdentifier**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **PKEY \_ media \_ Writer**                  | [**WM/escritor**](../wmformat/wm-writer.md)                                   |
| **PKEY \_ \_ año multimedia**                    | [**WM/año**](../wmformat/wm-year.md)                                       |
| **PKEY \_ Music \_ AlbumArtist**             | [**WM/AlbumArtist**](../wmformat/wm-albumartist.md)                         |
| **PKEY \_ Music \_ álbum**              | [**WM/álbum**](../wmformat/wm-albumtitle.md)                           |
| **PKEY \_ Music \_ artista**                  | [**Autor**](../wmformat/author.md)                                         |
| **PKEY \_ Music \_ BeatsPerMinute**          | [**WM/BeatsPerMinute**](../wmformat/wm-beatsperminute.md)                   |
| **PKEY \_ Music \_ Composer**                | [**WM/compositor**](../wmformat/wm-composer.md)                               |
| **\_Conductor de música PKEY \_**               | [**WM/conductor**](../wmformat/wm-conductor.md)                             |
| **PKEY \_ Music \_ ContentGroupDescription** | [**WM/ContentGroupDescription**](../wmformat/wm-contentgroupdescription.md) |
| **\_Género de música PKEY \_**                   | [**WM/género**](../wmformat/wm-genre.md)                                     |
| **PKEY \_ Music \_ InitialKey**              | [**WM/InitialKey**](../wmformat/wm-initialkey.md)                           |
| **PKEY \_ Music \_ IsCompilation**           | **WM/IsCompilation**                                                  |
| **PKEY \_ \_ canciones**                  | [**WM/Letras**](../wmformat/wm-lyrics.md)                                   |
| **PKEY \_ música \_ ambiente**                    | [**WM/humor**](../wmformat/wm-mood.md)                                       |
| **PKEY \_ Music \_ PartOfSet**               | [**WM/PartOfSet**](../wmformat/wm-partofset.md)                             |
| **PKEY de \_ música \_**                  | [**WM/período**](../wmformat/wm-period.md)                                   |
| **PKEY \_ Music \_ TrackNumber**             | [**WM/TrackNumber**](../wmformat/wm-tracknumber.md)                         |
| **PKEY \_ ParentalRating**                 | [**WM/ParentalRating**](../wmformat/wm-parentalrating.md)                   |
| **PKEY \_ ParentalRatingReason**           | [**WM/ParentalRatingReason**](../wmformat/wm-parentalratingreason.md)       |
| **\_Clasificación PKEY**                         | [**WM/SharedUserRating**](../wmformat/wm-shareduserrating.md)               |
| **PKEY \_ ThumbnailStream**                | [**WM/imagen**](../wmformat/wmpicture.md)                       |
| **Título de PKEY \_**                          | [**Title**](../wmformat/title.md)                                           |
| **\_Director de vídeo de PKEY \_**                | [**WM/Director**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos de medios](media-metadata.md)
</dt> <dt>

[Proveedores de metadatos de Shell](shell-metadata-providers.md)
</dt> </dl>

 

 
