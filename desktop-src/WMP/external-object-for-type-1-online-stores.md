---
title: Objeto externo para almacenes en línea de tipo 1
description: Objeto externo para almacenes en línea de tipo 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Reproductor de Windows Media en línea, objetos externos
- tiendas en línea, objetos externos
- tiendas en línea de tipo 1, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649005"
---
# <a name="external-object-for-type-1-online-stores"></a>Objeto externo para almacenes en línea de tipo 1

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **objeto Externo** proporciona funcionalidad a las páginas web, proporcionadas por una tienda en línea, hospedadas en Reproductor de Windows Media.

El **objeto External** expone las siguientes propiedades para almacenes en línea de tipo 1.



| Propiedad                                                                                  | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Recupera el tipo de cuenta del usuario actual.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Recupera el color de resaltado del botón actual para la interfaz Reproductor de Windows Media usuario.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Recupera el color actual del mouse del botón para la Reproductor de Windows Media usuario.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Recupera el color de sombra del botón actual para la interfaz Reproductor de Windows Media usuario.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Recupera el color sombreado oscuro actual de la interfaz Reproductor de Windows Media usuario.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Recupera el color sombreado claro actual de la interfaz Reproductor de Windows Media usuario.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Recupera el color sombreado medio actual de la interfaz Reproductor de Windows Media usuario.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Recupera el título del botón en el panel de lista (también denominado cesta) en Reproductor de Windows Media.                                     |
| [filter](external-filter.md)                                                             | Recupera el filtro de búsqueda actualmente en uso por Reproductor de Windows Media.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Especifica si Reproductor de Windows Media debe omitir Internet Explorer historial.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Recupera el identificador de un elemento multimedia específico que se muestra actualmente en la vista del reproductor.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Recupera una constante [de ubicación de biblioteca](library-location-constants.md) que indica el tipo de la vista actual en Reproductor de Windows Media. |
| [pluginRunning](external-pluginrunning.md)                                               | Recupera un valor que indica si el complemento de la tienda en línea se está ejecutando.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Recupera el identificador del elemento multimedia que está seleccionado actualmente en Reproductor de Windows Media.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Recupera el tipo del elemento multimedia que está seleccionado actualmente en Reproductor de Windows Media.                                                 |
| [Tarea](external-task.md)                                                                 | Recupera el nombre del panel de tareas actual.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indica si la fuente representada por la página de detección actual se muestra en el control de vista de árbol de la biblioteca local.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Recupera un valor que indica si el usuario ha iniciado sesión en la tienda en línea.                                                          |
| [version](external-version.md)                                                           | Recupera la versión actual de Reproductor de Windows Media.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Recupera los parámetros asociados a la vista actual en Reproductor de Windows Media.                                                           |



 

El **objeto External** expone los métodos siguientes para almacenes en línea de tipo 1.



| Método                                                            | Descripción                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Agrega elementos multimedia al panel de lista (también denominado cesta) en Reproductor de Windows Media.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.                                                 |
| [authenticate](external-authenticate.md)                         | Inicia un intento de autenticar al usuario.                                                                               |
| [comprar](external-buy.md)                                           | Inicia la compra de un conjunto de elementos multimedia.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informa Reproductor de Windows Media que no debe mostrar una nueva página de detección aunque la vista haya cambiado en el reproductor. |
| [changeView](external-changeview.md)                             | Cambia la vista en Reproductor de Windows Media.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Cambia la vista de Reproductor de Windows Media para mostrar una lista generada dinámicamente por la tienda en línea.                        |
| [download](external-download.md)                                 | Inicia la descarga de un conjunto de elementos multimedia.                                                                              |
| [Jugar](external-play.md)                                         | Indica Reproductor de Windows Media reproducir un conjunto de elementos multimedia.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crea una lista de reproducción a partir de los elementos multimedia de la vista actual y guarda la lista de reproducción en la biblioteca local.                     |
| [sendMessage](external-sendmessage.md)                           | Envía un mensaje al complemento de la tienda en línea.                                                                               |
| [showPopup](external-showpopup.md)                               | Indica a Reproductor de Windows Media que muestre una página web emergente; es decir, una página web que aparece en una ventana independiente.            |



 

El **objeto External** expone los siguientes eventos para almacenes en línea de tipo 1.



| Evento                                                                         | Descripción                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Se produce cuando una llamada al **método External.ChangeView** produce un error.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Se produce cuando una llamada al **método External.ChangeViewOnlineList** produce un error. |
| [OnColorChange](external-oncolorchange-event.md)                             | Se produce cuando cambia el color del Reproductor de Windows Media interfaz de usuario.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Se produce cuando cambia el estado de inicio de sesión del usuario o cuando se produce un error al intentar iniciar sesión.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Se produce cuando la tienda en línea ha terminado de procesar un mensaje.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Se produce cuando la vista cambia en Reproductor de Windows Media.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




