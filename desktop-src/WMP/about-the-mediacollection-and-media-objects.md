---
title: Acerca de los objetos MediaCollection y multimedia
description: Acerca de los objetos MediaCollection y multimedia
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Media Player de Windows, objeto MediaCollection
- Modelo de objetos de Media Player de Windows, objeto MediaCollection
- modelo de objetos, MediaCollection (objeto)
- Control ActiveX de Windows Media Player, objeto MediaCollection
- Control ActiveX, objeto MediaCollection
- Control ActiveX de Windows Media Player Mobile, objeto MediaCollection
- Windows Media Player Mobile, objeto MediaCollection
- Objeto MediaCollection
- Windows Media Player, objeto multimedia
- Modelo de objetos de Windows Media Player, objeto multimedia
- modelo de objetos, objeto multimedia
- Control ActiveX de Windows Media Player, objeto multimedia
- Control ActiveX, objeto multimedia
- Control ActiveX móvil de Windows Media Player, objeto multimedia
- Windows Media Player Mobile, objeto multimedia
- Objeto multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695411"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Acerca de los objetos MediaCollection y multimedia

Los objetos **MediaCollection** y **multimedia** rigen la colección de medios, que define las ubicaciones de los archivos multimedia digitales a los que puede tener acceso Windows Media Player. Obtiene el objeto **MediaCollection** de la propiedad **MediaCollection** del objeto **Player** . La propiedad **mediaCollection** devuelve el objeto **mediaCollection** . Solo puede acceder a las propiedades del objeto **MediaCollection** una vez creado. Por ejemplo, para agregar un objeto **multimedia** (una canción), use el código siguiente:


```C++
player.mediacollection.add('laure.wma');

```



Ha agregado el archivo Laure. WMA a la colección de medios.

Puede obtener el objeto **multimedia** actual mediante la propiedad **currentMedia** del **reproductor**. Por ejemplo, este código obtiene la propiedad **Duration** del objeto **multimedia** actual:


```C++
myduration = player.currentmedia.duration;

```



Hay muchas maneras de obtener un objeto **multimedia** para poder tener acceso a sus propiedades. Por ejemplo, si desea tener acceso a la propiedad **Duration** del medio actual, se podría usar cada una de las siguientes líneas de código.

Para obtener la duración del contenido multimedia que se está reproduciendo actualmente:


```C++
player.currentMedia.duration;

```



Para obtener la duración del medio actual en una lista de reproducción:


```C++
player.controls.currentItem.duration;

```



Para obtener la duración del tercer elemento multimedia de una lista de reproducción:


```C++
player.currentPlaylist.item(2).duration;

```



Para obtener la duración del tercer elemento multimedia en un género "Jazz":


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Para obtener la duración del tercer elemento multimedia en la segunda lista de reproducción:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




