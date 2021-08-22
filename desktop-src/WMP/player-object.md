---
title: Objeto Player
description: El objeto Player es el objeto raíz del Reproductor de Windows Media control. Admite las propiedades, métodos y eventos enumerados en las tablas siguientes.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Player Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ee314862aad1237036d5a7fa6a5627f42a6185d1ab6914f1e11ec19a831b755
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616705"
---
# <a name="player-object"></a>Objeto Player

El objeto Player es el objeto raíz del Reproductor de Windows Media control. Admite las propiedades, métodos y eventos enumerados en las tablas siguientes.

El objeto Player admite las siguientes propiedades. Las propiedades marcadas con un asterisco ( \* ) no son accesibles para las máscaras.



| Propiedad                                             | Descripción                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | Recupera el [objeto CdromCollection.](cdromcollection-object.md)                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera el [objeto ClosedCaption.](closedcaption-object.md)                                                                              |
| [controls](player-controls.md)                      | Recupera el [objeto Controls.](controls-object.md)                                                                                        |
| [currentMedia](player-currentmedia.md)              | Especifica o recupera el objeto [Multimedia](media-object.md) actual.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Especifica o recupera el objeto Playlist [actual.](playlist-object.md)                                                                   |
| [Dvd](player-dvd.md)                                | Recupera el [objeto DVD.](dvd-object.md)                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic con el botón derecho del mouse.          |
| [habilitado](player-enabled.md)\*                     | Especifica o recupera un valor que indica si el control Reproductor de Windows Media está habilitado.                                               |
| [error](player-error.md)                            | Recupera el [objeto Error.](error-object.md)                                                                                              |
| [fullScreen](player-fullscreen.md)\*               | Especifica o recupera un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.                                          |
| [isOnline](player-isonline.md)                      | Recupera un valor que indica si el usuario está conectado a una red.                                                                     |
| [isRemote](player-isremote.md)\*                   | Recupera un valor que indica si el control Reproductor de Windows Media se ejecuta en modo remoto.                                             |
| [mediaCollection](player-mediacollection.md)        | Recupera el [objeto MediaCollection.](mediacollection-object.md)                                                                          |
| [network](player-network.md)                        | Recupera el [objeto Network.](network-object.md)                                                                                          |
| [openState](player-openstate.md)                    | Recupera un valor que indica el estado del origen de contenido.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera el objeto [PlayerApplication](playerapplication-object.md) cuando se ejecuta un control Reproductor de Windows Media remoto.               |
| [playlistCollection](player-playlistcollection.md)  | Recupera el objeto [PlaylistCollection.](playlistcollection-object.md)                                                                    |
| [playState](player-playstate.md)                    | Recupera un valor que indica el estado de la Reproductor de Windows Media operación.                                                                |
| [settings](player-settings.md)                      | Recupera el [Configuración](settings-object.md) objeto .                                                                                        |
| [status](player-status.md)                          | Recupera un valor que indica el estado actual de Reproductor de Windows Media.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Especifica o recupera un valor que indica si el vídeo se ajustará para ajustarse al tamaño de la pantalla Reproductor de Windows Media vídeo de control.          |
| [uiMode](player-uimode.md)\*                       | Especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario cuando Reproductor de Windows Media está insertado en una página web. |
| [URL](player-url.md)                                | Especifica o recupera el nombre del clip que se reproducirá.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Recupera un valor String que especifica la versión del Reproductor de Windows Media.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Especifica o recupera un valor que indica si el control Reproductor de Windows Media representa el vídeo en modo sin ventanas.                         |



 

\* No es accesible para las máscaras.

El objeto Player admite los métodos siguientes.



| Método                                | Descripción                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Versiones Reproductor de Windows Media recursos.                  |
| [launchURL](player-launchurl.md)     | Envía una dirección URL al explorador predeterminado del usuario que se va a representar. |
| [newMedia](player-newmedia.md)       | Crea un nuevo [objeto](media-object.md) Multimedia.           |
| [newPlaylist](player-newplaylist.md) | Crea un nuevo objeto [Playlist.](playlist-object.md)     |
| [openPlayer](player-openplayer.md)   | Abre Reproductor de Windows Media con la dirección URL especificada.       |



 

El objeto Player admite los siguientes eventos. Los eventos marcados con un asterisco ( \* ) no son accesibles para las máscaras. Para obtener información sobre cómo controlar eventos de mouse y teclado en máscaras, vea [External Events](external-events.md).



| Evento                                                                                            | Descripción                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produce cuando cambia el idioma de audio actual.                                  |
| [de respuesta](player-player-buffering.md)                                                         | Se produce cuando el control Reproductor de Windows Media inicia o finaliza el almacenamiento en búfer.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produce cuando se inserta o expulsa un CD o DVD desde una unidad de CD o DVD.      |
| [Hacer clic](player-player-click.md) \*                                                              | Se produce cuando el usuario hace clic en un botón del mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produce cuando *controla*. **currentItem** cambia.                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produce cuando algo cambia dentro de la lista de reproducción actual.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produce cuando el elemento de lista de reproducción actual está disponible.                         |
| **Desconexión**                                                                                   | Reservado para uso futuro.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produce cuando cambia el dominio de DVD.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Se produce cuando el usuario hace doble clic en un botón del mouse.                               |
| **DurationUnitChange**                                                                           | Reservado para uso futuro.                                                         |
| **EndOfStream**                                                                                  | Reservado para uso futuro.                                                         |
| [Error](player-player-error.md)                                                                 | Se produce cuando el Reproductor de Windows Media control tiene una condición de error.             |
| [KeyDown](player-player-keydown.md)\*                                                          | Se produce cuando se presiona una tecla.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Se produce cuando se presiona una tecla y, a continuación, se libera.                                  |
| [KeyUp](player-player-keyup.md)\*                                                              | Se produce cuando se suelta una tecla.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produce cuando se alcanza un marcador.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Se produce cuando cambia un elemento multimedia.                                                |
| [MediaCollectionAttributeString agregado](player-player-mediacollectionattributestringadded.md)     | Se produce cuando se agrega un valor de atributo a la biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produce cuando se cambia un valor de atributo en la biblioteca.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produce cuando se quita un valor de atributo de la biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produce cuando cambia la colección de medios.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Se produce cuando se agrega un elemento multimedia a la biblioteca local.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Se produce cuando se quita un elemento multimedia de la biblioteca local.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Se produce cuando el **objeto Media** tiene una condición de error.                         |
| [ModeChange](player-player-modechange.md)                                                       | Se produce cuando se cambia un Reproductor de Windows Media de datos.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Se produce cuando se presiona un botón del mouse.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Se produce cuando se mueve el puntero del mouse.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Se produce cuando se libera un botón del mouse.                                          |
| **NewStream**                                                                                    | Reservado para uso futuro.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produce cuando comienza a reproducirse un título de un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produce cuando el control Reproductor de Windows Media cambia de estado.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produce cuando cambia una lista de reproducción.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produce cuando algo cambia en la colección de listas de reproducción.                        |
| [Se ha agregado PlaylistCollectionPlaylist](player-player-playlistcollectionplaylistadded.md)             | Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Reservado para uso futuro.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produce cuando cambia el estado de reproducción Reproductor de Windows Media control.          |
| [PositionChange](player-player-positionchange.md)                                               | Se produce cuando se ha cambiado la posición actual del elemento multimedia.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produce cuando se recibe un comando sincronizado o una dirección URL.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Se produce cuando cambia **el valor de** la propiedad status.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Se produce cuando cambia una colección de cadenas.                                         |
| **Advertencia**                                                                                      | Reservado para uso futuro.                                                         |



 

\* No es accesible para las máscaras. Para obtener información sobre cómo controlar eventos de mouse y teclado en máscaras, vea [Controladores de eventos ambiente](ambient-event-handlers.md).

Cuando se inserta en una página web, se puede acceder al objeto **Player** mediante el valor de identificador especificado en la etiqueta OBJECT. Dentro de un archivo de definición de máscara, se accede a él mediante el atributo global **player.** Con fines ilustrativos, **el reproductor** se usará como identificador de objeto en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




