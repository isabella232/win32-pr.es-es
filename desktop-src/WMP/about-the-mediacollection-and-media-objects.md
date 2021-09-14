---
title: Acerca de los objetos MediaCollection y Media
description: Acerca de los objetos MediaCollection y Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Reproductor de Windows Media,objeto MediaCollection
- Reproductor de Windows Media modelo de objetos,objeto MediaCollection
- object model,MediaCollection object
- Reproductor de Windows Media ActiveX control,objeto MediaCollection
- ActiveX control,objeto MediaCollection
- Reproductor de Windows Media Control ActiveX móvil, objeto MediaCollection
- Reproductor de Windows Media Mobile,MediaCollection , objeto
- Objeto MediaCollection
- Reproductor de Windows Media,objeto Media
- Reproductor de Windows Media modelo de objetos, objeto Multimedia
- object model,Media object
- Reproductor de Windows Media ActiveX control, objeto Media
- ActiveX control, objeto Media
- Reproductor de Windows Media Control de ActiveX móvil,objeto Multimedia
- Reproductor de Windows Media Mobile,Media (objeto)
- Objeto multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264764"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Acerca de los objetos MediaCollection y Media

Los **objetos MediaCollection** y **Media** rigen la colección multimedia, que define las ubicaciones de los archivos multimedia digitales a los Reproductor de Windows Media pueden acceder. Obtiene el objeto **MediaCollection** de la **propiedad mediaCollection** del **objeto Player.** La **propiedad mediaCollection** devuelve el **objeto MediaCollection.** Solo puede acceder a las propiedades del **objeto MediaCollection** después de crearlo. Por ejemplo, para agregar un **objeto Media** (una canción), use el código siguiente:


```C++
player.mediacollection.add('laure.wma');

```



Ha agregado el archivo laure.wma a la colección de medios.

Puede obtener el objeto **Multimedia** actual mediante la **propiedad currentMedia** del **reproductor**. Por ejemplo, este código obtiene la **propiedad duration** del objeto **Media** actual:


```C++
myduration = player.currentmedia.duration;

```



Hay muchas maneras de obtener un **objeto Multimedia** para que pueda acceder a sus propiedades. Por ejemplo, si desea tener acceso a la **propiedad duration** del medio actual, se podría usar cada una de las siguientes líneas de código.

Para obtener la duración de los medios que se reproducen actualmente:


```C++
player.currentMedia.duration;

```



Para obtener la duración del medio actual en una lista de reproducción:


```C++
player.controls.currentItem.duration;

```



Para obtener la duración del tercer elemento multimedia en una lista de reproducción:


```C++
player.currentPlaylist.item(2).duration;

```



Para obtener la duración del tercer elemento multimedia de un género "Jazz":


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



Para obtener la duración del tercer elemento multimedia de la segunda lista de reproducción:


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

 

 




