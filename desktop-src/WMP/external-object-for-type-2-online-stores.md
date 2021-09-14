---
title: Objeto externo para almacenes en línea de tipo 2
description: Objeto externo para almacenes en línea de tipo 2
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Reproductor de Windows Media en línea, objetos externos
- tiendas en línea, objetos externos
- tiendas en línea de tipo 2, objetos externos
- objetos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c412cac301d61aeb791131e85bb8bc60f390201d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241905"
---
# <a name="external-object-for-type-2-online-stores"></a>Objeto externo para almacenes en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **objeto** Externo puede proporcionar funcionalidad a las páginas web proporcionadas por una tienda en línea de tipo 2 y hospedadas en Reproductor de Windows Media.

El **objeto External** expone las siguientes propiedades.



| Propiedad                                                        | Descripción                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | Recupera el color de resaltado del botón actual para la Reproductor de Windows Media interfaz de usuario. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | Recupera el color actual del mouse del botón para la Reproductor de Windows Media interfaz de usuario.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | Recupera el color de sombra del botón actual para la interfaz Reproductor de Windows Media usuario.    |
| [appColorDark](external-appcolordark.md)                       | Recupera el color sombreado oscuro actual de la interfaz Reproductor de Windows Media usuario.       |
| [appColorLight](external-appcolorlight.md)                     | Recupera el color sombreado claro actual de la interfaz Reproductor de Windows Media usuario.      |
| [appColorMedium](external-appcolormedium.md)                   | Recupera el color sombreado medio actual de la interfaz Reproductor de Windows Media usuario.     |
| [DownloadManager](external-downloadmanager.md)                 | Recupera el **objeto DownloadManager.**                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Especifica o recupera el panel de tareas seleccionado actualmente.                                  |
| [version](external-version.md)                                 | Recupera la versión actual de Reproductor de Windows Media.                                    |



 

El **objeto External** expone los métodos siguientes.



| Método                                                  | Descripción                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Abre una página web en el panel de tareas especificado y cambia el foco al panel especificado. |
| [playMedia (en desuso)](external-playmedia.md)        | Especifica la dirección URL de un elemento multimedia digital que se reproducirá.                                   |



 

El **objeto External** expone el evento siguiente.



| Evento                                             | Descripción                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | Se produce cuando cambia el color del Reproductor de Windows Media interfaz de usuario. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




