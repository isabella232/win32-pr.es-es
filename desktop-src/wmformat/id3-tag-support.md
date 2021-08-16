---
title: Compatibilidad con etiquetas ID3
description: Compatibilidad con etiquetas ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows SDK de formato multimedia, atributos
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,ID3 tags
- Etiquetas ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fd65ffadb952e9370af609e336c08fc07c9b96f50d09d95c78492bef2163db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703030"
---
# <a name="id3-tag-support"></a>Compatibilidad con etiquetas ID3

En la tabla siguiente se enumeran todos los atributos que corresponden a las etiquetas ID3. Si quiere usar las etiquetas ID3 como atributos en lugar de usar los nombres de atributo estándar, agregue el prefijo "ID3/" al nombre de etiqueta. Por ejemplo, "ID3/TPE2" equivale a **Author**.



| Atributo                      | ID3v1.x | ID3v2.2 | ID3v2.3/v2.4 |
|--------------------------------|---------|---------|--------------|
| **Author**                     | Artista  | TP1     | TPE1         |
| **Copyright**                  |         | Tcr     | TCOP         |
| **CopyrightURL**               |         | Wcp     | WCOP         |
| **Descripción**                | Comentario | COM     | COMM         |
| **Duración**                   |         | TLE     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Título**                      | Título   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Álbum   | TAL     | TALB         |
| **WM/ArtistSortOrder**         |         |         | Tsop         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/Binary**                  |         | Geo     | GEOB         |
| **WM/Comments**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/Conductor**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | Diez     | TENC         |
| **WM/EncodingSettings**        |         | Tss     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | TCO     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/Language**                |         | Tla     | Tlan         |
| **\_WM/Sincronizado**    |         | Slt     | Sylt         |
| **WM/MCDI**                    |         |         | Mcdi         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/Estados de ánimo**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | Tot     | TOAL         |
| **WM/OriginalArtist**          |         | Toa     | TOPE         |
| **WM/OriginalFilename**        |         | Tof     | TOFN         |
| **WM/OriginalLyricist**        |         | Tol     | TOLY         |
| **WM/OriginalReleaseYear**     |         | Tor     | Tory         |
| **WM/PartOfSet**               |         | Tpa     | TPOS         |
| **WM/Picture**                 |         | PIC     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | Tpb     | TPUB         |
| **WM/RadioStationName**        |         | Trn     | TRSN         |
| **WM/RadioStationOwner**       |         | Tro     | TRSO         |
| **WM/SetSubTitle**             |         |         | Tsst         |
| **WM/SubTitle**                |         | TT3     | TIT3         |
| **WM/Text**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | Ufi     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/Writer**                  |         | TXT     | TEXT         |
| **WM/Year**                    | Year    | Tye     | TYER         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




