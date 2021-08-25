---
title: Objeto AxWindowsMediaPlayer (VB y C)
description: Objeto AxWindowsMediaPlayer (VB y C\)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Reproductor de Windows Media objeto AxWindowsMediaPlayer
- Reproductor de Windows Media Objeto Mobile,AxWindowsMediaPlayer
- Reproductor de Windows Media objeto object model,AxWindowsMediaPlayer
- object model,AxWindowsMediaPlayer object
- ActiveX control, objeto AxWindowsMediaPlayer
- Reproductor de Windows Media ActiveX control, objeto AxWindowsMediaPlayer
- Reproductor de Windows Media Control ActiveX móvil,objeto AxWindowsMediaPlayer
- referencia para el objeto object model,AxWindowsMediaPlayer
- Objeto AxWindowsMediaPlayer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d0c66360e80ea293795442472ce163292c38152baa859889086a5687f03764f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765285"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>Objeto AxWindowsMediaPlayer (VB y C#)

El objeto AxWindowsMediaPlayer es el objeto raíz del control Reproductor de Windows Media control . Admite las propiedades, métodos y eventos enumerados en las tablas siguientes.

El objeto AxWindowsMediaPlayer admite las siguientes propiedades.



| Propiedad                                                                             | Descripción                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Obtiene una **interfaz IWMPCdromCollection.**                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Obtiene una interfaz IWMPClosedCaption.                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Obtiene una interfaz IWMPControls.                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Obtiene o establece un valor que indica si el control Reproductor de Windows Media está habilitado.                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Obtiene o establece la interfaz IWMPMedia que corresponde al elemento multimedia actual.                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Obtiene o establece la interfaz **IWMPPlaylist** actual.                                                                               |
| [Dvd](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Obtiene una interfaz IWMPDVD.                                                                                                         |
| [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic con el botón derecho del mouse.          |
| [Error](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Obtiene una interfaz IWMPError.                                                                                                       |
| [Fullscreen](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Obtiene o establece un valor que indica si el contenido del vídeo se reproduce en modo de pantalla completa.                                          |
| [isOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Obtiene un valor que indica si el usuario está conectado a una red.                                                                |
| isRemote                                                                             | No se admite para la programación de .NET.                                                                                                |
| [mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Obtiene una interfaz IWMPMediaCollection.                                                                                             |
| [network](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Obtiene una interfaz IWMPNetwork.                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Obtiene un valor que indica el estado del origen de contenido.                                                                           |
| playerApplication                                                                    | No se admite para la programación de .NET.                                                                                                |
| [playlistCollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Obtiene una interfaz IWMPPlaylistCollection.                                                                                          |
| [playState](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Obtiene un valor que indica el estado de la Reproductor de Windows Media operación.                                                           |
| [settings](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Obtiene una interfaz IWMPSettings.                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Obtiene un valor que indica el estado actual de Reproductor de Windows Media.                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Obtiene o establece un valor que indica si el vídeo se ajustará para ajustarse al tamaño de la pantalla Reproductor de Windows Media vídeo de control.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Obtiene o establece un valor que indica qué controles se muestran en la interfaz de usuario cuando Reproductor de Windows Media se inserta en una página web. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Obtiene o establece el nombre del clip que se va a reproducir.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Obtiene un valor que especifica la versión del Reproductor de Windows Media.                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Obtiene o establece un valor que indica si el control Reproductor de Windows Media representa el vídeo en modo sin ventanas.                         |



 

El objeto AxWindowsMediaPlayer admite los métodos siguientes.



| Método                                                       | Descripción                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Versiones Reproductor de Windows Media recursos.                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | Envía una dirección URL al explorador predeterminado del usuario que se va a representar. |
| [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.      |
| [newPlaylist](axwmplib-axwindowsmediaplayer-newplaylist.md) | devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | Abre Reproductor de Windows Media con la dirección URL especificada.       |



 

El objeto AxWindowsMediaPlayer admite los siguientes eventos.



| Evento                                                                                                              | Descripción                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Se produce cuando cambia el idioma de audio actual.                                                            |
| [de respuesta](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Se produce cuando el control Reproductor de Windows Media inicia o finaliza el almacenamiento en búfer.                                     |
| [CdromError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Se produce cuando se produce un error genérico durante una operación de grabación de CD.                                         |
| [CdromErrorMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Se produce cuando se produce un error al grabar un elemento multimedia individual en un CD.                               |
| [CdromChangeStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Se produce cuando una operación de grabación de CD cambia de estado.                                                          |
| [CdromMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Se produce cuando se inserta o expulsa un CD o DVD en una unidad de CD o DVD.                                |
| [CdromRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Se produce cuando se produce un error mientras se realiza una pista individual desde un CD.                                  |
| [CdromRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Se produce cuando cambia el estado de una operación de arrasado de CD.                                                          |
| [Hacer clic](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Se produce cuando el usuario hace clic en un botón del mouse.                                                                |
| CreatePartnershipComplete                                                                                          | No se admite para la programación de .NET.                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Se produce cuando [cambia IWMPControls.currentItem.](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible.                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Se produce cuando algo cambia dentro de la lista de reproducción actual.                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Se produce cuando el elemento de lista de reproducción actual está disponible.                                                   |
| DeviceConnect.                                                                                                      | No se admite para la programación de .NET.                                                                        |
| DeviceDisconnect                                                                                                   | No se admite para la programación de .NET.                                                                        |
| DeviceStatusChange                                                                                                 | No se admite para la programación de .NET.                                                                        |
| DeviceSyncError                                                                                                    | No se admite para la programación de .NET.                                                                        |
| DeviceSyncStateChange                                                                                              | No se admite para la programación de .NET.                                                                        |
| [Desconexión](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | Reservado para uso futuro.                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Se produce cuando cambia el dominio de DVD.                                                                        |
| [Doubleclick](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Se produce cuando el usuario hace doble clic en un botón del mouse.                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Reservado para uso futuro.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Reservado para uso futuro.                                                                                   |
| [Error](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Se produce cuando el control Reproductor de Windows Media tiene una condición de error.                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Se produce cuando una operación de supervisión de carpetas cambia de estado.                                                   |
| [Keydown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Se produce cuando se presiona una tecla.                                                                              |
| [Keypress](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Se produce cuando se presiona una tecla y, a continuación, se libera.                                                            |
| [Keyup](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Se produce cuando se suelta una tecla.                                                                             |
| [LibraryConnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Se produce cuando una biblioteca está disponible.                                                                   |
| [LibraryDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Se produce cuando una biblioteca ya no está disponible.                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Se produce cuando se alcanza un marcador.                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Se produce cuando cambia un elemento multimedia.                                                                          |
| [MediaCollectionAttributeString agregado](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Se produce cuando se agrega un valor de atributo a la biblioteca.                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Se produce cuando se cambia un valor de atributo en la biblioteca.                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Se produce cuando se quita un valor de atributo de la biblioteca.                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Se produce cuando cambia la colección de medios.                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Se produce cuando se agrega un elemento multimedia a la biblioteca local.                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Se produce cuando se quita un elemento multimedia de la biblioteca local.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Se produce cuando el **objeto Media** tiene una condición de error.                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Se produce cuando se cambia un Reproductor de Windows Media de datos.                                                     |
| [Mousedown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Se produce cuando se presiona un botón del mouse.                                                                     |
| [Mousemove](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Se produce cuando se mueve el puntero del mouse.                                                                    |
| [MouseUp](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Se produce cuando se libera un botón del mouse.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Reservado para uso futuro.                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Se produce cuando comienza a reproducirse un título de un DVD.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Se produce cuando el control Reproductor de Windows Media cambia de estado.                                                |
| PlayerDockedStateChange                                                                                            | No se admite para la programación de .NET.                                                                        |
| PlayerReconnect                                                                                                    | No se admite para la programación de .NET.                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Se produce cuando cambia una lista de reproducción.                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Se produce cuando algo cambia en la colección de listas de reproducción.                                                  |
| [Se ha agregado PlaylistCollectionPlaylist](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Se produce cuando se agrega una lista de reproducción a la colección de listas de reproducción.                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Reservado para uso futuro.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Se produce cuando cambia el estado de reproducción Reproductor de Windows Media control.                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Se produce cuando se ha cambiado la posición actual del elemento multimedia.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Se produce cuando se recibe un comando sincronizado o una dirección URL.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Se produce cuando cambia **el valor de** la propiedad status.                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Se produce cuando cambia una colección de cadenas.                                                                   |
| SwitchedToControl                                                                                                  | No se admite para la programación de .NET.                                                                        |
| SwitchedToPlayerApplication                                                                                        | No se admite para la programación de .NET.                                                                        |
| [Advertencia](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Reservado para uso futuro.                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Referencia del modelo de objetos Visual Basic .NET y C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 




