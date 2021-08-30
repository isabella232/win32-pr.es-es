---
title: Listas de reproducción y elementos multimedia
description: Listas de reproducción y elementos multimedia
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media modelo de objetos, listas de reproducción
- modelo de objetos, listas de reproducción
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- listas de reproducción, elementos multimedia
- listas de reproducción de metarchivo, elementos multimedia
- Windows Listas de reproducción de metarchivo multimedia, elementos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef42f4c79c8239af9278532c8bd09e320725a9d3bb36b361995e25fa905257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862085"
---
# <a name="playlists-and-media-items"></a>Listas de reproducción y elementos multimedia

Una lista de reproducción es un conjunto de elementos multimedia. Un **objeto Lista** de reproducción puede manipular los objetos **Multimedia** que representan esos elementos.

## <a name="retrieving-media-items"></a>Recuperar elementos multimedia

Para una lista de reproducción existente, puede leer la lista de *reproducción*. **count** para determinar cuántos elementos multimedia hay en la lista de reproducción y puede obtener una referencia al objeto **Multimedia** correspondiente a un elemento específico mediante la lista de *reproducción*. **propiedad item.**

En el siguiente ejemplo de C# se recupera una referencia de objeto a un elemento multimedia específico. (En este tema, la variable *pList* es una referencia a un objeto **Playlist).**


```C++
currMedia = pList.Item(0);

```



En el siguiente ejemplo de C# se recuperan los nombres de todos los elementos multimedia de una lista de reproducción y se coloca en un listBox denominado lstOutput.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Agregar elementos a una lista de reproducción

Puede agregar un elemento multimedia al final de una lista de reproducción o en una posición específica de una lista de reproducción, mediante la lista de *reproducción*. **appendItem y** *Playlist*. **Métodos insertItem.**

A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se muestran ambas técnicas agregando el elemento multimedia actual a una lista de reproducción denominada "BluesTest", primero al final y luego al principio de la lista de reproducción.


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



Al crear una nueva lista de reproducción vacía mediante *PlaylistCollection*. **Método newPlaylist,** puede agregarle elementos multimedia llamando repetidamente a la lista de *reproducción*. **Método appendItem.**

## <a name="manipulating-media-items-in-a-playlist"></a>Manipulación de elementos multimedia en una lista de reproducción

Puede cambiar la posición de un elemento multimedia en la lista de reproducción mediante la lista de *reproducción*. **Método moveItem.** Especifique el elemento por su índice actual y, a continuación, especifique el nuevo índice. En el siguiente ejemplo de C# se mueve un elemento del índice 5 al índice 0 dentro de una lista de reproducción.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



Puede quitar un elemento multimedia de la lista de reproducción mediante la lista **de reproducción**. **Método removeItem.** Tenga en cuenta que si el elemento quitado no era el último elemento de la lista de reproducción, los valores de índice de los elementos posteriores cambian. En el siguiente ejemplo de C# se quita el elemento especificado.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Los usuarios pueden cambiar el contenido de una lista de reproducción fuera de la aplicación. Cada vez que manipula los elementos de una lista de reproducción, debe supervisar y controlar los eventos relacionados con la lista de reproducción del control Reproductor de Windows Media para asegurarse de que el código funciona correctamente. Estos eventos son *player.* **CurrentPlaylistChange** y *Player*. **Lista de reproducciónCambiar**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 




