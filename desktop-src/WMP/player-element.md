---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Aspectos de Windows Media Player, elemento PLAYER
- máscaras, elemento PLAYER
- Elemento PLAYER
- referencia de las máscaras, elemento PLAYER
- elementos, reproductor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148831"
---
# <a name="player-element"></a>Elemento PLAYER

El elemento **Player** permite definir controladores de eventos y especificar la propiedad **URL** del objeto **Player** en tiempo de diseño dentro de un archivo de definición de máscara. En el código de script, se tiene acceso al objeto **Player** a través del atributo global **Player** en lugar de un nombre especificado por un atributo **ID** , que no es compatible con el elemento **Player** .

El elemento **Player** admite el siguiente atributo.



| Atributo             | Descripción                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Especifica o recupera el nombre del archivo que se va a reproducir. |



 

El elemento **Player** puede implementar controladores de eventos para los siguientes eventos desencadenados desde el objeto **Player** .



| Evento                                                                                            | Descripción                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produce cuando cambia el idioma actual del audio.                                  |
| [de respuesta](player-player-buffering.md)                                                         | Se produce cuando Windows Media Player inicia o finaliza el almacenamiento en búfer.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produce cuando cambia el medio del CD.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produce cuando cambia el elemento actual.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produce cuando el elemento multimedia actual está disponible.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produce cuando cambia la lista de reproducción actual.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produce cuando el elemento de lista de reproducción actual está disponible.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produce cuando cambia el dominio del DVD.                                              |
| [Error](player-player-error.md)                                                                 | Se produce cuando el control de Media Player de Windows tiene una condición de error.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produce cuando Windows Media Player encuentra un marcador en el clip.                |
| [MediaChange](player-player-mediachange.md)                                                     | Se produce cuando cambia un elemento multimedia.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Se produce cuando se agrega un valor de atributo a la biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produce cuando se cambia un valor de atributo de la biblioteca.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produce cuando se quita un valor de atributo de la biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produce cuando cambia el objeto **MediaCollection** .                              |
| [MediaError](player-player-mediaerror.md)                                                       | Se produce cuando el objeto **multimedia** tiene una condición de error.                         |
| [ModeChange](player-player-modechange.md)                                                       | Tiene lugar cuando se cambia entre el modo de orden aleatorio y normal.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produce cuando comienza a reproducirse un título en un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produce cuando el *reproductor*. **openState** cambios.                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produce cuando cambia una lista de reproducción.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produce cuando hay algún cambio en la colección de listas de reproducción.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produce cuando el *reproductor*. **playState** cambios.                                      |
| [PositionChange](player-player-positionchange.md)                                               | Se produce cuando el *reproductor*. *controles*. **currentPosition** cambios.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produce cuando Windows Media Player encuentra un comando de script incrustado en un archivo. |
| [StatusChange](player-player-statuschange.md)                                                   | Se produce cuando cambia el valor de la propiedad **status** .                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




