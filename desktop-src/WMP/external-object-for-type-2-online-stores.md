---
title: Objeto externo para las tiendas en línea de tipo 2
description: Objeto externo para las tiendas en línea de tipo 2
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Windows Media Player tiendas en línea, objetos externos
- tiendas en línea, objetos externos
- tipo 2 tiendas en línea, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c412cac301d61aeb791131e85bb8bc60f390201d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532254"
---
# <a name="external-object-for-type-2-online-stores"></a>Objeto externo para las tiendas en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El objeto **externo** puede proporcionar funcionalidad a las páginas web proporcionadas por una tienda en línea de tipo 2 y hospedadas en Windows Media Player.

El objeto **externo** expone las siguientes propiedades.



| Propiedad                                                        | Descripción                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | Recupera el color de resaltado del botón actual para la interfaz de usuario de Windows Media Player. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | Recupera el color de desplazamiento del botón actual para la interfaz de usuario de Windows Media Player.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | Recupera el color de la sombra del botón actual para la interfaz de usuario de Windows Media Player.    |
| [appColorDark](external-appcolordark.md)                       | Recupera el color sombreado oscuro actual de la interfaz de usuario de Windows Media Player.       |
| [appColorLight](external-appcolorlight.md)                     | Recupera el color sombreado de la luz actual de la interfaz de usuario de Windows Media Player.      |
| [appColorMedium](external-appcolormedium.md)                   | Recupera el color medio sombreado actual de la interfaz de usuario de Windows Media Player.     |
| [DownloadManager](external-downloadmanager.md)                 | Recupera el objeto **Downloadmanager** .                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Especifica o recupera el panel de tareas seleccionado actualmente.                                  |
| [version](external-version.md)                                 | Recupera la versión actual de Windows Media Player.                                    |



 

El objeto **externo** expone los métodos siguientes.



| Método                                                  | Descripción                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Abre una página web en el panel de tareas especificado y cambia el foco al panel especificado. |
| [playMedia (desusado)](external-playmedia.md)        | Especifica la dirección URL de un elemento multimedia digital que se va a reproducir.                                   |



 

El objeto **externo** expone el evento siguiente.



| Evento                                             | Descripción                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | Se produce cuando cambia el color de la interfaz de usuario de Media Player de Windows. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




