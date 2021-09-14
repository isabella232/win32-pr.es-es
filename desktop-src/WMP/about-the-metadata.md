---
title: Acerca de los metadatos
description: Acerca de los metadatos
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Reproductor de Windows Media,metadata
- metadata,about
- metadata,attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073291"
---
# <a name="about-the-metadata"></a>Acerca de los metadatos

Reproductor de Windows Media 10 o posterior intenta sincronizar los siguientes atributos de metadatos.



| Atributo player | Constante global de WMDM  | Descripción                                                                                                 | Versión requerida                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | Cadena terminada en **NULL** que contiene el nombre del intérprete principal del álbum.                         | Reproductor de Windows Media 11 o posterior. |
| Álbum            | g \_ wszWMDMAlbumTitle  | Cadena terminada en **NULL** que contiene el título del álbum en el que se publicó originalmente el contenido.  | Reproductor de Windows Media 11 o posterior. |
| Autor           | g \_ wszWMDMAuthor      | Cadena terminada en **NULL** que contiene el nombre del actor o intérprete multimedia asociado al contenido.    | Reproductor de Windows Media 11 o posterior. |
| BuyNow           | g \_ wszWMDMBuyNow      | **Valor** booleano que indica si el usuario ha elegido comprar el contenido.                                 | Reproductor de Windows Media 10 o posterior. |
| WM/Genre         | g \_ wszWMDMGenre       | Cadena terminada en **NULL** que contiene el género del contenido.                                             | Reproductor de Windows Media 11 o posterior. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD que** contiene el número de veces que el usuario ha reproducdo el archivo multimedia digital.                        | Reproductor de Windows Media 10 o posterior. |
| ReleaseDate      | g \_ wszWMDMYear        | Fecha de la versión original del elemento.                                                               | Reproductor de Windows Media 11 o posterior. |
| Título            | g \_ wszWMDMTitle       | Cadena terminada en **NULL** que contiene el título.                                                            | Reproductor de Windows Media 11 o posterior. |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** que contiene el número de pista del elemento del álbum en el que se publicó originalmente.         | Reproductor de Windows Media 11 o posterior. |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** que contiene un valor que representa la clasificación de estrella que el usuario especificó para el archivo multimedia digital. | Reproductor de Windows Media 10 o posterior. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de dispositivo para la transferencia acelerada de metadatos**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




