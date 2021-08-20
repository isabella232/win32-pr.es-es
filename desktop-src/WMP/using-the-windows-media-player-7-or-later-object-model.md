---
title: Usar el Reproductor de Windows Media de objetos 7 o posterior
description: Usar el Reproductor de Windows Media de objetos 7 o posterior
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Reproductor de Windows Media,modelo de objetos
- Reproductor de Windows Media modelo de objetos, versión 7 o posterior
- modelo de objetos, versión 7 o posterior
- Reproductor de Windows Media ActiveX control, versión 7 o posterior
- ActiveX control, versión 7 o posterior
- Reproductor de Windows Media Control ActiveX móvil, versión 7 o posterior
- Reproductor de Windows Media Móvil, modelo de objetos
- guía de migración, versión 7 o posterior
- versiones de Reproductor de Windows Media,modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa40dea2718c602bfae305703913b418d0f8a48b90278683aba099dfe0d703bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117033"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Usar el Reproductor de Windows Media de objetos 7 o posterior

La mayoría de las tareas que puede haber realizado con Reproductor de Windows Media 6.4 ActiveX modelo de objetos de control requerirán un nuevo enfoque. En muchos casos, los nombres de las propiedades, métodos y eventos han cambiado en Reproductor de Windows Media modelo de objetos 7 o posterior. Por ejemplo, para especificar la ruta de acceso del archivo en el modelo de objetos de la versión 6.4, establezca la **propiedad Player6.FileName:**


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Al usar el Reproductor de Windows Media de objetos 7 o posterior, debe establecer la **propiedad Player.URL:**


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



Como alternativa, con el modelo de objetos 10, puede obtener un objeto **Media** de la biblioteca y, a continuación, establecer la **propiedad Player.currentMedia:**


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Se accede a gran parte de la funcionalidad Reproductor de Windows Media modelo de objetos 7 o posterior a través de la jerarquía de objetos. Como se mostró en el ejemplo anterior, puede obtener un objeto **Playlist** mediante el método **getAll** del objeto **mediaCollection,** al que se accede a través del objeto **Player** raíz. A continuación, puede obtener un objeto **Multimedia** determinado del objeto **Lista de** reproducción mediante el método **de** elemento del objeto **Lista de** reproducción. Hay cinco métodos adicionales accesibles a través del **objeto mediaCollection** que devuelven un objeto **Playlist;** cada método permite recuperar el objeto en función de criterios específicos, como género o álbum.

La estructura jerárquica del modelo de objetos de control Reproductor de Windows Media 7 o posterior de ActiveX proporciona un enfoque más lógico para organizar las propiedades, métodos y eventos disponibles para su uso. Toda la funcionalidad de los controles Player está contenida en el objeto **Controls,** toda la funcionalidad de la conexión de red player está contenida en el objeto **Network,** etc. Por ejemplo, para iniciar la reproducción de contenido con el modelo de objetos de la versión 6.4, use el **método Player6.Play:**


```C++
WMP64.Play();

```



Al usar el Reproductor de Windows Media de objetos 7 o posterior, debe tener acceso al método **Play** mediante el **objeto Controls:**


```C++
WMP9.controls.play();

```



Sin embargo, la profundidad del modelo de objetos puede dar lugar a instrucciones de script muy largas:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Las instrucciones como la anterior se pueden hacer mucho más sencillas y legibles si se trabaja con objetos con nombre individuales. En el ejemplo siguiente se reemplaza la instrucción de código anterior por la sintaxis mediante variables de objeto independientes:


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



Este estilo de codificación requiere más líneas de script, pero es mucho más fácil de seguir, especialmente con los comentarios agregados. Hay otra ventaja: el **objeto currentPlaylist** es fácil de reutilizar porque se almacena en la variable pl.

Muchas de las propiedades, métodos y eventos del modelo de objetos de Reproductor de Windows Media 7 o posterior establecen o recuperan valores diferentes, o devuelven valores de un tipo o número diferentes, en comparación con la funcionalidad correspondiente del modelo de objetos de la versión 6.4. Por ejemplo, cuando **Player6.openState** recupera 2, ese valor corresponde a la constante **nsLoadingNSC** de Visual Basic , lo que significa que el reproductor carga un archivo de estación con una extensión de nombre de archivo .nsc. Pero cuando la propiedad del modelo de objetos Reproductor de Windows Media 7 o posterior **Player.openState** recupera 2, ese valor corresponde al estado PlaylistLocating, lo que significa que Reproductor de Windows Media está intentando buscar una lista de reproducción. Además, la propiedad **Player6.openState** puede recuperar siete valores diferentes, mientras que la propiedad Reproductor de Windows Media 7 o posterior **Player.openState** puede recuperar 22 valores diferentes. Asegúrese de consultar la sección Referencia del modelo de objetos para scripting del SDK de Reproductor de Windows Media al revisar el código para usar una versión de modelo de objetos diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guía de migración de modelos de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




