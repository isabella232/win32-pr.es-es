---
title: Lista de atributos
description: Lista de atributos
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows SDK de formato multimedia, atributos
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,list of
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251582"
---
# <a name="attribute-list"></a>Lista de atributos

Los atributos predefinidos incluidos con este SDK se presentan alfabéticamente en la tabla siguiente. Cada atributo tiene un nombre, un identificador global y un tipo de datos tal como lo define el miembro adecuado de la enumeración [**\_ \_ DATATYPE DE ATTR de WMT.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) Algunos atributos no usan un tipo de datos simple o tienen formato según una estructura . Entries for these attributes list a structure name in the data-type column with the data type used to set the value in parentheses.

> [!Note]  
> Consulte [Lista de atributos DE DRM](drm-attribute-list.md) para obtener una tabla de todos los atributos relacionados con DRM.

 

Al programar con estos atributos, debe usar el identificador global en lugar de usar el nombre como literal de cadena. Al usar el identificador global, los errores tipográficos producirán un error en tiempo de compilación.



| Nombre del atributo                                                                       | Identificador global                             | Tipo de datos                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **BINARIO DE \_ TIPO \_ WMT**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**Autor**](author.md)                                                             | g \_ wszWMAuthor                                | **CADENA DE TIPO WMT \_ \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **BINARIO DE \_ TIPO \_ WMT**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **CADENA DE TIPO WMT \_ \_**                                |
| [**Bitrate**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**Difusión**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **WMT \_ TYPE \_ BOOL**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**Puede \_ omitir hacia \_ atrás**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **WMT \_ TYPE \_ BOOL**                                  |
| [**Puede \_ omitir \_ el avance**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **WMT \_ TYPE \_ BOOL**                                  |
| [**Copyright**](copyright.md)                                                       | g \_ wszWMCopyright                             | **CADENA DE TIPO WMT \_ \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **CADENA DE TIPO WMT \_ \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**Descripción**](description.md)                                                   | g \_ wszWMDescription                           | **CADENA DE TIPO WMT \_ \_**                                |
| [**ContentID de DRM \_**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentID                        | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ ContentDistributor**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ ContentID**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentID             | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)                                 | g \_ wszWMDRM \_ DRMHeader \_ KeyID                 | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ DRMHeader \_ SubscriptionContentID**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRMHeader \_ de DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ KeyID**](drm-keyid.md)                                                      | g \_ wszWMDRM \_ KeyID                            | **CADENA DE TIPO WMT \_ \_**                                |
| [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **CADENA DE \_ TIPO \_ WMT**                                |
| [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **CADENA DE \_ TIPO \_ WMT**                                |
| [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**DRM \_ LicenseAcqURL**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Id. de licencia de DRM \_**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**ID de origen de DRM \_**](drm-sourceid.md)                                                | g \_ wszWMDRM \_ SourceID                         | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Duration**](duration.md)                                                         | g \_ wszWMDuration                              | **TIPO WMT \_ \_ QWORD**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszWMFileSize                              | **TIPO WMT \_ \_ QWORD**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **TIPO WMT \_ \_ BOOL**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **TIPO WMT \_ \_ BOOL**                                  |
| [**Está \_ protegido**](is-protected.md)                                                | g \_ wszWMProtected                             | **TIPO WMT \_ \_ BOOL**                                  |
| [**Es de \_ confianza**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **TIPO WMT \_ \_ BOOL**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszISAN                                    | **CADENA DE \_ TIPO \_ WMT**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **TIPO WMT \_ \_ BOOL**                                  |
| [**Dirección \_ NSC**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Descripción de \_ NSC**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Correo electrónico de NSC \_**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Nombre de \_ NSC**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **CADENA DE \_ TIPO \_ WMT**                                |
| [**NSC \_ Teléfono**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **TIPO WMT \_ \_ QWORD**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**PeakValue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**Rating**](rating.md)                                                             | g \_ wszWMRating                                | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Buscable**](seekable.md)                                                         | g \_ wszWMSeekable                              | **TIPO WMT \_ \_ BOOL**                                  |
| [**Nombre de \_ la firma**](signature-name.md)                                            | g \_ wszWMSignature \_ Name                       | **CADENA DE \_ TIPO \_ WMT**                                |
| [**Stridable**](stridable.md)                                                       | g \_ wszWMStridable                             | **TIPO WMT \_ \_ BOOL**                                  |
| [**Título**](title.md)                                                               | g \_ wszWMTitle                                 | **CADENA DE \_ TIPO \_ WMT**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMAlbumArtist                           | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMAlbumCoverURL                         | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/AlbumTitle**](wm-albumtitle.md)                                               | g \_ wszWMAlbumTitle                            | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **QWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **QWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Categoría**](wm-category.md)                                                   | g \_ wszWMCategory                              | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Codec**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Composer**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Conductor**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ STORAGE \_ FORMAT** (**WMT TYPE \_ \_ BINARY**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszWMDirector                              | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**WMT \_ TYPE \_ QWORD**)                  |
| [**WM/Genre**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Language**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **CADENA DE TIPO WMT \_ \_**                                |
| [**WM/Desa eso**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **CADENA DE TIPO WMT \_ \_**                                |
| [**\_WM/Sincronización de wm/desastroso**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ Synchronised                  | **WM \_ SYNCHRONISED \_ LATA (BINARIO** **DE \_ TIPO \_ WMT)** |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **BINARIO DE \_ TIPO \_ WMT**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **GUID DE \_ TIPO \_ WMT**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **GUID DE \_ TIPO \_ WMT**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Estados de ánimo**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalAlbumTitle                    | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/Period**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Picture**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_ PICTURE** (**WMT \_ TYPE \_ BINARY**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Producer**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Provider**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Publisher**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | g \_ wszWMRadioStationName                      | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWMRadioStationOwner                     | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_ STREAM \_ TYPE \_ INFO** (**WMT TYPE \_ \_ BINARY**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/SubTitle**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Text**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_ USER \_ TEXT** (**WMT TYPE \_ \_ BINARY**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/ToolVersion**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Track**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_ USER \_ WEB \_ URL** (**WMT TYPE \_ \_ BINARY**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **TIPO WMT \_ \_ BOOL**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **DWORD \_ DE TIPO \_ WMT**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **GUID DE \_ TIPO \_ WMT**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **GUID DE \_ TIPO \_ WMT**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **GUID DE \_ TIPO \_ WMT**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Writer**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **CADENA DE \_ TIPO \_ WMT**                                |
| [**WM/Year**](wm-year.md)                                                           | g \_ wszWMYear                                  | **CADENA DE \_ TIPO \_ WMT**                                |



 

## <a name="remarks"></a>Observaciones

Las siguientes constantes se definen con los atributos . Cada uno indica el número de un tipo específico de atributo. No es necesario usar estos valores para nada en las aplicaciones.



| Constante                 | Value |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 