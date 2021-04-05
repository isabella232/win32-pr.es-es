---
title: Lista de atributos
description: Lista de atributos
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, lista de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533184"
---
# <a name="attribute-list"></a>Lista de atributos

Los atributos predefinidos que se incluyen en este SDK se presentan en orden alfabético en la tabla siguiente. Cada atributo tiene un nombre, un identificador global y un tipo de datos, tal y como lo define el miembro adecuado de la enumeración del [**\_ \_ tipo**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) de datos del atributo WMT. Algunos atributos no usan un tipo de datos simple o se les da formato según una estructura. Las entradas de estos atributos muestran un nombre de estructura en la columna de tipo de datos con el tipo de datos usado para establecer el valor entre paréntesis.

> [!Note]  
> Consulte [lista de atributos de DRM](drm-attribute-list.md) para obtener una tabla de todos los atributos relacionados con DRM.

 

Al programar con estos atributos, debe utilizar el identificador global en lugar de usar el nombre como un literal de cadena. Con el identificador global, los errores tipográficos producirán un error en tiempo de compilación.



| Nombre del atributo                                                                       | Identificador global                             | Tipo de datos                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **tipo de WMT \_ \_ binario**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **tipo de WMT \_ \_ DWORD**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **tipo de WMT \_ \_ DWORD**                                 |
| [**Autor**](author.md)                                                             | g \_ wszWMAuthor                                | **\_cadena de tipo WMT \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **tipo de WMT \_ \_ DWORD**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **tipo de WMT \_ \_ binario**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **tipo de WMT \_ \_ DWORD**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **\_cadena de tipo WMT \_**                                |
| [**Bitrate**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **tipo de WMT \_ \_ DWORD**                                 |
| [**Difusión**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **tipo de WMT \_ \_ bool**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **tipo de WMT \_ \_ DWORD**                                 |
| [**Puede \_ omitir \_ hacia atrás**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **tipo de WMT \_ \_ bool**                                  |
| [**Puede \_ saltar \_ adelante**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **tipo de WMT \_ \_ bool**                                  |
| [**SSoftware**](copyright.md)                                                       | g \_ wszWMCopyright                             | **\_cadena de tipo WMT \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **\_cadena de tipo WMT \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **tipo de WMT \_ \_ DWORD**                                 |
| [**Descripción**](description.md)                                                   | g \_ wszWMDescription                           | **\_cadena de tipo WMT \_**                                |
| [**ContentID de DRM \_**](drm-contentid.md)                                              | g \_ wszWMDRM \_ contentid                        | **\_cadena de tipo WMT \_**                                |
| [**\_ContentDistributor DRMHEADER \_ DRM**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **\_cadena de tipo WMT \_**                                |
| [**DRMHeader de de DRM \_ \_**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ contentid             | **\_cadena de tipo WMT \_**                                |
| [**\_IndividualizedVersion DRMHEADER \_ DRM**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **\_cadena de tipo WMT \_**                                |
| [**ID. de DRMHeader de DRM \_ \_**](drm-drmheader-keyid.md)                                 | \_wszWMDRM \_ DRMHeader ID. de cuenta \_                 | **\_cadena de tipo WMT \_**                                |
| [**\_LicenseAcqURL DRMHEADER \_ DRM**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **\_cadena de tipo WMT \_**                                |
| [**\_SubscriptionContentID DRMHEADER \_ DRM**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **\_cadena de tipo WMT \_**                                |
| [**\_DRMHEADER DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **\_cadena de tipo WMT \_**                                |
| [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **\_cadena de tipo WMT \_**                                |
| [**ID. de ID \_ de DRM**](drm-keyid.md)                                                      | ID. de \_ wszWMDRM g \_                            | **\_cadena de tipo WMT \_**                                |
| [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **\_cadena de tipo WMT \_**                                |
| [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **\_cadena de tipo WMT \_**                                |
| [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **\_cadena de tipo WMT \_**                                |
| [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **\_cadena de tipo WMT \_**                                |
| [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **\_cadena de tipo WMT \_**                                |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **\_cadena de tipo WMT \_**                                |
| [**Endrm \_ SourceID**](drm-sourceid.md)                                                | g \_ wszWMDRM \_ SourceID                         | **tipo de WMT \_ \_ DWORD**                                 |
| [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **\_cadena de tipo WMT \_**                                |
| [**Duration**](duration.md)                                                         | g \_ wszWMDuration                              | **tipo de WMT. \_ \_**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszWMFileSize                              | **tipo de WMT. \_ \_**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **tipo de WMT \_ \_ bool**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **tipo de WMT \_ \_ bool**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **tipo de WMT \_ \_ bool**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **tipo de WMT \_ \_ bool**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **tipo de WMT \_ \_ bool**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **tipo de WMT \_ \_ bool**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **tipo de WMT \_ \_ bool**                                  |
| [**Está \_ protegido**](is-protected.md)                                                | g \_ wszWMProtected                             | **tipo de WMT \_ \_ bool**                                  |
| [**Es de \_ confianza**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **tipo de WMT \_ \_ bool**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszISAN                                    | **\_cadena de tipo WMT \_**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **tipo de WMT \_ \_ bool**                                  |
| [**\_Dirección NSC**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **\_cadena de tipo WMT \_**                                |
| [**Descripción de NSC \_**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **\_cadena de tipo WMT \_**                                |
| [**\_Correo electrónico NSC**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **\_cadena de tipo WMT \_**                                |
| [**\_Nombre NSC**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **\_cadena de tipo WMT \_**                                |
| [**\_Teléfono NSC**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **\_cadena de tipo WMT \_**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **tipo de WMT. \_ \_**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **tipo de WMT \_ \_ DWORD**                                 |
| [**PeakValue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **tipo de WMT \_ \_ DWORD**                                 |
| [**Rating**](rating.md)                                                             | g \_ wszWMRating                                | **\_cadena de tipo WMT \_**                                |
| [**En**](seekable.md)                                                         | g \_ wszWMSeekable                              | **tipo de WMT \_ \_ bool**                                  |
| [**Nombre de la firma \_**](signature-name.md)                                            | g \_ wszWMSignature \_ nombre                       | **\_cadena de tipo WMT \_**                                |
| [**Progresable**](stridable.md)                                                       | g \_ wszWMStridable                             | **tipo de WMT \_ \_ bool**                                  |
| [**Title**](title.md)                                                               | g \_ wszWMTitle                                 | **\_cadena de tipo WMT \_**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMAlbumArtist                           | **\_cadena de tipo WMT \_**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMAlbumCoverURL                         | **\_cadena de tipo WMT \_**                                |
| [**WM/álbum**](wm-albumtitle.md)                                               | g \_ wszWMAlbumTitle                            | **\_cadena de tipo WMT \_**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **tipo de WMT. \_ \_**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **tipo de WMT. \_ \_**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **\_cadena de tipo WMT \_**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **\_cadena de tipo WMT \_**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **\_cadena de tipo WMT \_**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **\_cadena de tipo WMT \_**                                |
| [**WM/categoría**](wm-category.md)                                                   | g \_ wszWMCategory                              | **\_cadena de tipo WMT \_**                                |
| [**WM/códec**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **\_cadena de tipo WMT \_**                                |
| [**WM/compositor**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **\_cadena de tipo WMT \_**                                |
| [**WM/conductor**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **\_cadena de tipo WMT \_**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ \_formato de almacenamiento** (**\_ tipo WMT \_ binario**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **\_cadena de tipo WMT \_**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **\_cadena de tipo WMT \_**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszWMDirector                              | **\_cadena de tipo WMT \_**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **\_cadena de tipo WMT \_**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **\_cadena de tipo WMT \_**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **\_cadena de tipo WMT \_**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **\_cadena de tipo WMT \_**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**\_ tipo WMT \_ QWord**)                  |
| [**WM/género**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **\_cadena de tipo WMT \_**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **\_cadena de tipo WMT \_**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **\_cadena de tipo WMT \_**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **\_cadena de tipo WMT \_**                                |
| [**WM/lenguaje**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **\_cadena de tipo WMT \_**                                |
| [**WM/Letras**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **\_cadena de tipo WMT \_**                                |
| [**WM/Letras \_ sincronizadas**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ sincronizado                  | **WM \_ \_Letras sincronizadas** (**\_ \_ binario de tipo WMT**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **tipo de WMT \_ \_ binario**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **\_GUID de tipo WMT \_**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **\_GUID de tipo WMT \_**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **\_cadena de tipo WMT \_**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **tipo de WMT \_ \_ bool**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **\_cadena de tipo WMT \_**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **\_cadena de tipo WMT \_**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **\_cadena de tipo WMT \_**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **\_cadena de tipo WMT \_**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **\_cadena de tipo WMT \_**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **\_cadena de tipo WMT \_**                                |
| [**WM/humor**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalAlbumTitle                    | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **\_cadena de tipo WMT \_**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **\_cadena de tipo WMT \_**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **\_cadena de tipo WMT \_**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **\_cadena de tipo WMT \_**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **\_cadena de tipo WMT \_**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/período**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **\_cadena de tipo WMT \_**                                |
| [**WM/imagen**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_ IMAGEN** (**\_ tipo WMT \_ binario**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **\_cadena de tipo WMT \_**                                |
| [**WM/productor**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **\_cadena de tipo WMT \_**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **\_cadena de tipo WMT \_**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **\_cadena de tipo WMT \_**                                |
| [**WM/proveedor**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **\_cadena de tipo WMT \_**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **\_cadena de tipo WMT \_**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **\_cadena de tipo WMT \_**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **\_cadena de tipo WMT \_**                                |
| [**WM/publicador**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **\_cadena de tipo WMT \_**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | g \_ wszWMRadioStationName                      | **\_cadena de tipo WMT \_**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWMRadioStationOwner                     | **\_cadena de tipo WMT \_**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_ \_ \_ información de tipo de secuencia** (**tipo WMT \_ \_ binario**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **\_cadena de tipo WMT \_**                                |
| [**WM/subtítulo**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **\_cadena de tipo WMT \_**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **\_cadena de tipo WMT \_**                                |
| [**WM/texto**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_ \_texto de usuario** (**\_ tipo WMT \_ binario**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **\_cadena de tipo WMT \_**                                |
| [**WM/ToolVersion**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **\_cadena de tipo WMT \_**                                |
| [**WM/pista**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **\_cadena de tipo WMT \_**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **\_cadena de tipo WMT \_**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **\_cadena de tipo WMT \_**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_ \_ \_ dirección URL Web de usuario** (**\_ tipo WMT \_ binario**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **tipo de WMT \_ \_ bool**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/height**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/ancho de**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **tipo de WMT \_ \_ DWORD**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **\_GUID de tipo WMT \_**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **\_GUID de tipo WMT \_**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **\_GUID de tipo WMT \_**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **\_cadena de tipo WMT \_**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **\_cadena de tipo WMT \_**                                |
| [**WM/escritor**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **\_cadena de tipo WMT \_**                                |
| [**WM/año**](wm-year.md)                                                           | g \_ wszWMYear                                  | **\_cadena de tipo WMT \_**                                |



 

## <a name="remarks"></a>Observaciones

Las siguientes constantes se definen con los atributos. Cada uno de ellos indica el número de un tipo específico de atributo. No es necesario usar estos valores para nada en las aplicaciones.



| Constante                 | Value |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 