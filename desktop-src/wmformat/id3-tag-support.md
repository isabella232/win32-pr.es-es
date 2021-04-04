---
title: Compatibilidad con etiquetas ID3
description: Compatibilidad con etiquetas ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, etiquetas ID3
- Etiquetas ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3dd91119aedf2983e654b4925231b8fd9e4b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076143"
---
# <a name="id3-tag-support"></a>Compatibilidad con etiquetas ID3

En la tabla siguiente se enumeran todos los atributos que corresponden a las etiquetas ID3. Si desea utilizar las etiquetas ID3 como atributos en lugar de usar los nombres de atributo estándar, agregue el prefijo "ID3/" al nombre de la etiqueta. Por ejemplo, "ID3/TPE2" es equivalente a **Author**.



| Atributo                      | ID3v1. x | ID3v 2.2 | ID3v 2.3/v 2.4 |
|--------------------------------|---------|---------|--------------|
| **Autor**                     | Artistas  | TP1     | TPE1         |
| **Copyright**                  |         | TCR     | TCOP         |
| **CopyrightURL**               |         | WCP     | WCOP         |
| **Descripción**                | Comentario | COM     | COMM         |
| **Duration**                   |         | TLE     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Título**                      | Title   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/álbum**              | Álbum   | HABL     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/binario**                  |         | GEOID     | GEOB         |
| **WM/comentarios**                |         | COM     | COMM         |
| **WM/compositor**                |         | TCM     | TCOM         |
| **WM/conductor**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | 10     | TENC         |
| **WM/EncodingSettings**        |         | TSS     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | TCO     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/lenguaje**                |         | PIEZA     | TLAN         |
| **WM/Letras \_ sincronizadas**    |         | SLT     | SYLT         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/humor**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | TOTAL     | TOAL         |
| **WM/OriginalArtist**          |         | TOA     | PARTE superior         |
| **WM/OriginalFilename**        |         | TOF     | TOFN         |
| **WM/OriginalLyricist**        |         | TOLERANCIA     | TOLY         |
| **WM/OriginalReleaseYear**     |         | TOR     | TORY         |
| **WM/PartOfSet**               |         | TPA     | TPOS         |
| **WM/imagen**                 |         | PIC     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/publicador**               |         | TPB     | TPUB         |
| **WM/RadioStationName**        |         | TRN     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/SetSubTitle**             |         |         | TSST         |
| **WM/subtítulo**                |         | TT3     | TIT3         |
| **WM/texto**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | UFI     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/escritor**                  |         | TXT     | TEXT         |
| **WM/año**                    | Year    | TYE     | TYER         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




