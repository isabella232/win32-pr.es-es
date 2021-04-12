---
title: Usar el modelo de objetos de Windows Media Player 7 o posterior
description: Usar el modelo de objetos de Windows Media Player 7 o posterior
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, versión 7 o posterior
- modelo de objetos, versión 7 o posterior
- Windows Media Player control ActiveX, versión 7 o posterior
- Control ActiveX, versión 7 o posterior
- Windows Media Player Mobile ActiveX Control, versión 7 o posterior
- Windows Media Player Mobile, modelo de objetos
- Guía de migración, versión 7 o posterior
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357280"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Usar el modelo de objetos de Windows Media Player 7 o posterior

La mayoría de las tareas que se pueden haber realizado con el modelo de objetos de control ActiveX de Windows Media Player 6,4 requerirán un enfoque nuevo. En muchos casos, los nombres de las propiedades, métodos y eventos han cambiado en el modelo de objetos de Windows Media Player 7 o posterior. Por ejemplo, para especificar la ruta de acceso del archivo en el modelo de objetos de la versión 6,4, establezca la propiedad **Player6. FileName** :


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Al usar el modelo de objetos de Windows Media Player 7 o posterior, debe establecer la propiedad **Player. URL** :


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



También puede usar el modelo de objetos 10 para obtener un objeto **multimedia** de la biblioteca y, a continuación, establecer la propiedad **Player. currentMedia** :


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Gran parte de la funcionalidad del modelo de objetos de Windows Media Player 7 o posterior se obtiene acceso a través de la jerarquía de objetos. Como se mostró en el ejemplo anterior, puede obtener un objeto de **lista de reproducción** con el método **GetAll** del objeto **mediaCollection** , al que se tiene acceso a través del objeto **reproductor** raíz. A continuación, puede obtener un objeto **multimedia** determinado del objeto de **lista de reproducción** mediante el método **Item** del objeto **playlist** . Hay cinco métodos adicionales accesibles a través del objeto **mediaCollection** que devuelven un objeto de **lista de reproducción** : cada método permite recuperar el objeto basándose en criterios específicos, como el género o el álbum.

La estructura jerárquica del modelo de objetos de control ActiveX de Windows Media Player 7 o posterior proporciona un enfoque más lógico para organizar las propiedades, los métodos y los eventos disponibles para su uso. Toda la funcionalidad de los controles del reproductor está contenida en el objeto **Controls** , toda la funcionalidad de la conexión de red del reproductor está contenida en el objeto de **red** , etc. Por ejemplo, para iniciar la reproducción de contenido con el modelo de objetos de la versión 6,4, se usa el método **Player6. Play** :


```C++
WMP64.Play();

```



Al usar el modelo de objetos de Windows Media Player 7 o posterior, debe tener acceso al método **Play** mediante el objeto **Controls** :


```C++
WMP9.controls.play();

```



La profundidad del modelo de objetos, sin embargo, puede dar lugar a instrucciones de script muy largas:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Las instrucciones como la anterior se pueden hacer mucho más sencillas y legibles si se trabaja con objetos con nombre individuales. En el ejemplo siguiente se reemplaza la instrucción de código anterior con la sintaxis mediante variables de objeto independientes:


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



Este estilo de codificación requiere más líneas de script, pero es mucho más fácil de seguir, especialmente con los comentarios agregados. Existe otra ventaja: el objeto **currentPlaylist** es fácil de volver a usar porque se almacena en la variable pl.

Muchas de las propiedades, métodos y eventos del modelo de objetos de Windows Media Player 7 o posterior establecen o recuperan valores diferentes, o devuelven valores de un tipo o número diferente, en comparación con la funcionalidad correspondiente en el modelo de objetos de la versión 6,4. Por ejemplo, cuando **Player6. openState** recupera 2, ese valor corresponde a la constante Visual Basic **nsLoadingNSC**, lo que significa que el reproductor está cargando un archivo de estación con la extensión de nombre de archivo. NSC. Pero cuando el modelo de objetos de Windows Media Player 7 o posterior **Player. openState** recupera 2, ese valor corresponde al estado PlaylistLocating, lo que significa que Windows Media Player está intentando buscar una lista de reproducción. Además, la propiedad **Player6. openState** puede recuperar siete valores diferentes, mientras que la propiedad **Player. openState** de Windows Media Player 7 o posterior puede recuperar 22 valores distintos. Asegúrese de consultar la sección referencia del modelo de objetos para scripting del SDK de Windows Media Player al revisar el código para usar una versión de modelo de objetos diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del modelo de objetos de Player**](about-the-player-object-model.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guía de migración del modelo de objetos**](object-model-migration-guide.md)
</dt> </dl>

 

 




