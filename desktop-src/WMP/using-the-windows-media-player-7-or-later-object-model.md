---
title: Usar el modelo de Reproductor de Windows Media 7 o posterior
description: Usar el modelo de Reproductor de Windows Media 7 o posterior
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Reproductor de Windows Media,modelo de objetos
- Reproductor de Windows Media modelo de objetos, versión 7 o posterior
- modelo de objetos, versión 7 o posterior
- Reproductor de Windows Media ActiveX control, versión 7 o posterior
- ActiveX control, versión 7 o posterior
- Reproductor de Windows Media Control de ActiveX móvil, versión 7 o posterior
- Reproductor de Windows Media Móvil, modelo de objetos
- guía de migración, versión 7 o posterior
- versiones de Reproductor de Windows Media,object model
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359129"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Usar el modelo de Reproductor de Windows Media 7 o posterior

La mayoría de las tareas que puede haber realizado con el modelo de objetos de control Reproductor de Windows Media 6.4 ActiveX 6.4 requerirá un nuevo enfoque. En muchos casos, los nombres de las propiedades, métodos y eventos han cambiado en el modelo de objetos Reproductor de Windows Media 7 o posterior. Por ejemplo, para especificar la ruta de acceso del archivo en el modelo de objetos de la versión 6.4, establezca la **propiedad Player6.FileName:**


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Cuando se usa Reproductor de Windows Media modelo de objetos 7 o posterior, debe establecer la **propiedad Player.URL:**


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



Se accede a gran parte de la funcionalidad Reproductor de Windows Media modelo de objetos 7 o posterior a través de la jerarquía de objetos. Como se mostró en el ejemplo anterior, puede obtener un objeto **Playlist** mediante el método **getAll** del objeto **mediaCollection,** al que se accede a través del objeto **Player** raíz. A continuación, puede obtener un objeto **Multimedia** determinado del objeto **Lista de** reproducción mediante el método **item** del objeto **Lista de** reproducción. Hay cinco métodos adicionales accesibles a través del **objeto mediaCollection** que devuelven un objeto **Playlist;** Cada método permite recuperar el objeto en función de criterios específicos, como género o álbum.

La estructura jerárquica del modelo de objetos de control Reproductor de Windows Media 7 o posterior de ActiveX proporciona un enfoque más lógico para organizar las propiedades, los métodos y los eventos disponibles para su uso. Toda la funcionalidad de los controles Player está contenida en el objeto **Controls,** toda la funcionalidad de la conexión de red player está contenida en el objeto **Network,** etc. Por ejemplo, para iniciar la reproducción de contenido con el modelo de objetos de la versión 6.4, use el **método Player6.Play:**


```C++
WMP64.Play();

```



Cuando se usa Reproductor de Windows Media modelo de objetos 7 o posterior, debe tener acceso al método **Play** mediante el **objeto Controls:**


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

Muchas de las propiedades, métodos y eventos del modelo de objetos de Reproductor de Windows Media 7 o posterior establecen o recuperan valores diferentes, o valores devueltos de un tipo o número diferente, en comparación con la funcionalidad correspondiente en el modelo de objetos de la versión 6.4. Por ejemplo, cuando **Player6.openState** recupera 2, ese valor corresponde Visual Basic la constante de Visual Basic **nsLoadingNSC**, lo que significa que el reproductor carga un archivo de estación con una extensión de nombre de archivo .nsc. Pero cuando la propiedad **player.openState** del modelo de objetos Reproductor de Windows Media 7 o posterior recupera 2, ese valor corresponde al estado PlaylistLocating, lo que significa que Reproductor de Windows Media está intentando encontrar una lista de reproducción. Además, la propiedad **Player6.openState** puede recuperar siete valores diferentes, mientras que la propiedad **player.openState** de Reproductor de Windows Media 7 o posterior puede recuperar 22 valores diferentes. Asegúrese de consultar la sección Referencia del modelo de objetos para scripting del SDK de Reproductor de Windows Media al revisar el código para usar otra versión del modelo de objetos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos del reproductor**](about-the-player-object-model.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




