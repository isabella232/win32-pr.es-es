---
title: ELEMENTO PLAYER
description: ELEMENTO PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Reproductor de Windows Media máscaras, elemento PLAYER
- máscaras, elemento PLAYER
- ELEMENTO PLAYER
- referencia de máscaras,elemento PLAYER
- elements,PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bef2e7758a0146ae6197d17dc3790011a758f9d2fa4e3d54af9461a8b870c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338130"
---
# <a name="player-element"></a>ELEMENTO PLAYER

El **elemento PLAYER** permite definir controladores de eventos y especificar la propiedad **URL** del objeto **Player** en tiempo de diseño dentro de un archivo de definición de máscara. Dentro del código de script, se accede al objeto **Player** a través del atributo **global** player en lugar de a través de un nombre especificado por un atributo **id,** que no es compatible con el **elemento PLAYER.**

El **elemento PLAYER** admite el atributo siguiente.



| Atributo             | Descripción                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Especifica o recupera el nombre del archivo que se reproducirá. |



 

El **elemento PLAYER** puede implementar controladores de eventos para los siguientes eventos desencadenados desde el objeto **Player.**



| Evento                                                                                            | Descripción                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produce cuando cambia el idioma de audio actual.                                  |
| [de respuesta](player-player-buffering.md)                                                         | Se produce cuando Reproductor de Windows Media o finaliza el almacenamiento en búfer.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produce cuando cambia el medio de CD.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produce cuando cambia el elemento actual.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produce cuando el elemento multimedia actual está disponible.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produce cuando cambia la lista de reproducción actual.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produce cuando el elemento de lista de reproducción actual está disponible.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produce cuando cambia el dominio de DVD.                                              |
| [Error](player-player-error.md)                                                                 | Se produce cuando el control Reproductor de Windows Media tiene una condición de error.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produce cuando Reproductor de Windows Media encuentra un marcador en el clip.                |
| [MediaChange](player-player-mediachange.md)                                                     | Se produce cuando cambia un elemento multimedia.                                                |
| [MediaCollectionAttributeString agregado](player-player-mediacollectionattributestringadded.md)     | Se produce cuando se agrega un valor de atributo a la biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produce cuando se cambia un valor de atributo en la biblioteca.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produce cuando se quita un valor de atributo de la biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produce cuando cambia **el objeto MediaCollection.**                              |
| [MediaError](player-player-mediaerror.md)                                                       | Se produce cuando el **objeto Media** tiene una condición de error.                         |
| [ModeChange](player-player-modechange.md)                                                       | Se produce al cambiar entre el modo aleatorio y el modo normal.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produce cuando comienza a reproducirse un título de un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produce cuando el *reproductor*. **openState** cambia.                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produce cuando cambia una lista de reproducción.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produce cuando algo cambia en la colección de listas de reproducción.                        |
| [Se ha agregado PlaylistCollectionPlaylist](player-player-playlistcollectionplaylistadded.md)             | Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produce cuando el *reproductor*. **cambios de playState.**                                      |
| [PositionChange](player-player-positionchange.md)                                               | Se produce cuando el *reproductor*. *controla*. **currentPosition** cambia.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produce cuando Reproductor de Windows Media un comando de script insertado en un archivo. |
| [StatusChange](player-player-statuschange.md)                                                   | Se produce cuando cambia **el valor de** la propiedad status.                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




