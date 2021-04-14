---
title: Objeto Player
description: El objeto Player es el objeto raíz para el control Media Player de Windows. Admite las propiedades, los métodos y los eventos que se muestran en las tablas siguientes.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Media Player de objetos de reproductor de Windows
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104532781"
---
# <a name="player-object"></a>Objeto Player

El objeto Player es el objeto raíz para el control Media Player de Windows. Admite las propiedades, los métodos y los eventos que se muestran en las tablas siguientes.

El objeto Player admite las siguientes propiedades. No se puede acceder a las propiedades marcadas con un asterisco ( \* ) a las máscaras.



| Propiedad                                             | Descripción                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | Recupera el objeto [CdromCollection](cdromcollection-object.md) .                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera el objeto [ClosedCaption](closedcaption-object.md) .                                                                              |
| [permite](player-controls.md)                      | Recupera el objeto de [controles](controls-object.md) .                                                                                        |
| [currentMedia](player-currentmedia.md)              | Especifica o recupera el objeto [multimedia](media-object.md) actual.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Especifica o recupera el objeto de [lista de reproducción](playlist-object.md) actual.                                                                   |
| [discos](player-dvd.md)                                | Recupera el objeto de [DVD](dvd-object.md) .                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Especifica o recupera un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.          |
| [habilitado](player-enabled.md)\*                     | Especifica o recupera un valor que indica si el control Media Player de Windows está habilitado.                                               |
| [error](player-error.md)                            | Recupera el objeto de [error](error-object.md) .                                                                                              |
| [pantalla completa](player-fullscreen.md)\*               | Especifica o recupera un valor que indica si el contenido de vídeo se reproduce en el modo de pantalla completa.                                          |
| [isOnline](player-isonline.md)                      | Recupera un valor que indica si el usuario está conectado a una red.                                                                     |
| [isRemote](player-isremote.md)\*                   | Recupera un valor que indica si el control de Media Player de Windows se está ejecutando en modo remoto.                                             |
| [mediaCollection](player-mediacollection.md)        | Recupera el objeto [MediaCollection](mediacollection-object.md) .                                                                          |
| [network](player-network.md)                        | Recupera el objeto de [red](network-object.md) .                                                                                          |
| [openState](player-openstate.md)                    | Recupera un valor que indica el estado del origen de contenido.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera el objeto [PlayerApplication](playerapplication-object.md) cuando se está ejecutando un control remoto de Windows Media Player.               |
| [playlistCollection](player-playlistcollection.md)  | Recupera el objeto [PlaylistCollection](playlistcollection-object.md) .                                                                    |
| [playState](player-playstate.md)                    | Recupera un valor que indica el estado de la operación de Media Player de Windows.                                                                |
| [settings](player-settings.md)                      | Recupera el objeto de [configuración](settings-object.md) .                                                                                        |
| [status](player-status.md)                          | Recupera un valor que indica el estado actual de Windows Media Player.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Especifica o recupera un valor que indica si el vídeo se ajustará para ajustarse al tamaño de la pantalla de vídeo del control de Windows Media Player.          |
| [uiMode](player-uimode.md)\*                       | Especifica o recupera un valor que indica qué controles se muestran en la interfaz de usuario cuando Windows Media Player se incrusta en una página web. |
| [URL](player-url.md)                                | Especifica o recupera el nombre del clip que se va a reproducir.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Recupera un valor de cadena que especifica la versión de Windows Media Player.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Especifica o recupera un valor que indica si el control Media Player de Windows representa el vídeo en el modo sin ventanas.                         |



 

\* No se puede tener acceso a las máscaras.

El objeto Player admite los métodos siguientes.



| Método                                | Descripción                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Libera los recursos de Media Player de Windows.                  |
| [launchURL](player-launchurl.md)     | Envía una dirección URL al explorador predeterminado del usuario que se va a representar. |
| [newMedia](player-newmedia.md)       | Crea un nuevo objeto [multimedia](media-object.md) .           |
| [Reproducción](player-newplaylist.md) | Crea un nuevo objeto de [lista de reproducción](playlist-object.md) .     |
| [openPlayer](player-openplayer.md)   | Abre Windows Media Player mediante la dirección URL especificada.       |



 

El objeto Player admite los siguientes eventos. No se puede acceder a los eventos marcados con un asterisco ( \* ) a las máscaras. Para obtener información sobre cómo controlar los eventos del mouse y del teclado en las máscaras, vea [eventos externos](external-events.md).



| Evento                                                                                            | Descripción                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Se produce cuando cambia el idioma actual del audio.                                  |
| [de respuesta](player-player-buffering.md)                                                         | Se produce cuando el control de Media Player de Windows comienza o finaliza el almacenamiento en búfer.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Se produce cuando se inserta o se expulsa un CD o DVD en una unidad de CD o DVD.      |
| [Haga clic en](player-player-click.md)\*                                                              | Se produce cuando el usuario hace clic en un botón del mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Se produce cuando *controla*. **CurrentItem** cambia.                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Se produce cuando hay algún cambio en la lista de reproducción actual.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Se produce cuando el elemento de lista de reproducción actual está disponible.                         |
| **Desconexión**                                                                                   | Reservado para uso futuro.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Se produce cuando cambia el dominio del DVD.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Se produce cuando el usuario hace doble clic en un botón del mouse.                               |
| **DurationUnitChange**                                                                           | Reservado para uso futuro.                                                         |
| **EndOfStream**                                                                                  | Reservado para uso futuro.                                                         |
| [Error](player-player-error.md)                                                                 | Se produce cuando el control de Media Player de Windows tiene una condición de error.             |
| [KeyDown](player-player-keydown.md)\*                                                          | Se produce cuando se presiona una tecla.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Se produce cuando se presiona una tecla y se suelta.                                  |
| [KeyUp](player-player-keyup.md)\*                                                              | Se produce cuando se suelta una tecla.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Se produce cuando se alcanza un marcador.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Se produce cuando cambia un elemento multimedia.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Se produce cuando se agrega un valor de atributo a la biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Se produce cuando se cambia un valor de atributo de la biblioteca.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Se produce cuando se quita un valor de atributo de la biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Se produce cuando cambia la colección de medios.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Se produce cuando se agrega un elemento multimedia a la biblioteca local.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Se produce cuando se quita un elemento multimedia de la biblioteca local.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Se produce cuando el objeto **multimedia** tiene una condición de error.                         |
| [ModeChange](player-player-modechange.md)                                                       | Se produce cuando se cambia un modo de Media Player de Windows.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Se produce cuando se presiona un botón del mouse.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Se produce cuando se mueve el puntero del mouse.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Se produce cuando se suelta un botón del mouse.                                          |
| **NewStream**                                                                                    | Reservado para uso futuro.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Se produce cuando comienza a reproducirse un título en un DVD.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Se produce cuando cambia el estado del control de Media Player de Windows.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Se produce cuando cambia una lista de reproducción.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Se produce cuando hay algún cambio en la colección de listas de reproducción.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Reservado para uso futuro.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Se produce cuando cambia el estado de reproducción del control de Media Player de Windows.          |
| [PositionChange](player-player-positionchange.md)                                               | Se produce cuando se ha cambiado la posición actual del elemento multimedia.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Se produce cuando se recibe un comando o una dirección URL sincronizados.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Se produce cuando cambia el valor de la propiedad **status** .                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Se produce cuando cambia una colección de cadenas.                                         |
| **Warning (ADVERTENCIA)**                                                                                      | Reservado para uso futuro.                                                         |



 

\* No se puede tener acceso a las máscaras. Para obtener información sobre cómo controlar los eventos del mouse y del teclado en las máscaras, vea [controladores de eventos de ambiente](ambient-event-handlers.md).

Cuando se inserta en una página web, se puede tener acceso al objeto de **reproducción** mediante el valor de identificador especificado en la etiqueta de objeto. Dentro de un archivo de definición de máscara, se obtiene acceso a él mediante el atributo global del **reproductor** . A efectos de Ilustración, el **reproductor** se usará como el identificador de objeto en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




