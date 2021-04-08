---
title: Objeto externo para las tiendas en línea de tipo 1
description: Objeto externo para las tiendas en línea de tipo 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player tiendas en línea, objetos externos
- tiendas en línea, objetos externos
- tipo 1 almacenes en línea, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f50e5e6bfc98ea3669996b06fa4a4defb52452fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994540"
---
# <a name="external-object-for-type-1-online-stores"></a>Objeto externo para las tiendas en línea de tipo 1

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El objeto **externo** proporciona funcionalidad a las páginas web, proporcionadas por una tienda en línea, hospedadas en Windows Media Player.

El objeto **externo** expone las siguientes propiedades para las tiendas en línea de tipo 1.



| Propiedad                                                                                  | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Recupera el tipo de cuenta del usuario actual.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera el color de resaltado del botón actual para la interfaz de usuario de Windows Media Player.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera el color de desplazamiento del botón actual para la interfaz de usuario de Windows Media Player.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera el color de la sombra del botón actual para la interfaz de usuario de Windows Media Player.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera el color sombreado oscuro actual de la interfaz de usuario de Windows Media Player.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera el color sombreado de la luz actual de la interfaz de usuario de Windows Media Player.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera el color medio sombreado actual de la interfaz de usuario de Windows Media Player.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera el título del botón en el panel lista (también denominado cesta) en Windows Media Player.                                     |
| [filter](external-filter.md)                                                             | Recupera el filtro de búsqueda actualmente en uso por Media Player de Windows.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Especifica si Windows Media Player debe omitir el historial de Internet Explorer.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera el identificador de un elemento multimedia específico que se muestra actualmente en la vista del reproductor.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera una [constante de ubicación de biblioteca](library-location-constants.md) que indica el tipo de la vista actual en Windows Media Player. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera un valor que indica si se está ejecutando el complemento de la tienda en línea.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Recupera el identificador del elemento multimedia seleccionado actualmente en Windows Media Player.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Recupera el tipo del elemento multimedia seleccionado actualmente en Windows Media Player.                                                 |
| [Task](external-task.md)                                                                 | Recupera el nombre del panel de tareas actual.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Recupera un valor que indica si el usuario ha iniciado sesión en la tienda en línea.                                                          |
| [version](external-version.md)                                                           | Recupera la versión actual de Windows Media Player.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Recupera los parámetros asociados a la vista actual en Windows Media Player.                                                           |



 

El objeto **externo** expone los siguientes métodos para las tiendas en línea de tipo 1.



| Método                                                            | Descripción                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Agrega elementos multimedia al panel lista (también denominado cesta) en Windows Media Player.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.                                                 |
| [autenticar](external-authenticate.md)                         | Inicia un intento de autenticar al usuario.                                                                               |
| [comprar](external-buy.md)                                           | Inicia la compra de un conjunto de elementos multimedia.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa a Windows Media Player de que no debe mostrar una nueva página de detección aunque la vista haya cambiado en el reproductor. |
| [changeView](external-changeview.md)                             | Cambia la vista en Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Cambia la vista de Windows Media Player para mostrar una lista generada dinámicamente por la tienda en línea.                        |
| [download](external-download.md)                                 | Inicia la descarga de un conjunto de elementos multimedia.                                                                              |
| [reproducción](external-play.md)                                         | Indica a Windows Media Player que reproduzca un conjunto de elementos multimedia.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.                     |
| [sendMessage](external-sendmessage.md)                           | Envía un mensaje al complemento de la tienda en línea.                                                                               |
| [showPopup](external-showpopup.md)                               | Indica a Windows Media Player que muestre una página web emergente; es decir, una página web que aparece en una ventana independiente.            |



 

El objeto **externo** expone los siguientes eventos para las tiendas en línea de tipo 1.



| Evento                                                                         | Descripción                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Se produce cuando una llamada al método **external. ChangeView** produce un error.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Se produce cuando una llamada al método **external. ChangeViewOnlineList** produce un error. |
| [OnColorChange](external-oncolorchange-event.md)                             | Se produce cuando cambia el color de la interfaz de usuario de Media Player de Windows.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Se produce cuando cambia el estado del inicio de sesión del usuario o cuando se produce un error al intentar iniciar sesión.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Se produce cuando la tienda en línea ha finalizado el procesamiento de un mensaje.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Se produce cuando la vista cambia en Media Player de Windows.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




