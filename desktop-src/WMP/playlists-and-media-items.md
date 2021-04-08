---
title: Listas de reproducción y elementos multimedia
description: Listas de reproducción y elementos multimedia
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, elementos multimedia
- listas de reproducción de metarchivos, elementos multimedia
- Listas de reproducción de metarchivos de Windows Media, elementos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994083"
---
# <a name="playlists-and-media-items"></a>Listas de reproducción y elementos multimedia

Una lista de reproducción es un conjunto de elementos multimedia. Un objeto de **lista de reproducción** puede manipular los objetos **multimedia** que representan dichos elementos.

## <a name="retrieving-media-items"></a>Recuperar elementos multimedia

En el caso de una lista de reproducción existente, puede leer la *lista de reproducción*. propiedad **Count** para determinar el número de elementos multimedia que hay en la lista de reproducción y puede obtener una referencia al objeto **multimedia** correspondiente a un elemento específico mediante la *lista de reproducción*. propiedad del **elemento** .

En el siguiente ejemplo de C# se recupera una referencia de objeto a un elemento multimedia específico. (A lo largo de este tema, la variable *plist* es una referencia a un objeto de **lista de reproducción** ).


```C++
currMedia = pList.Item(0);

```



En el siguiente ejemplo de C# se recuperan los nombres de todos los elementos multimedia de una lista de reproducción y se colocan en un control ListBox denominado lstOutput.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Agregar elementos a una lista de reproducción

Puede Agregar un elemento multimedia al final de una lista de reproducción o a una posición específica de una lista de reproducción, mediante la *lista de reproducción*. **appendItem** y *lista de reproducción*. métodos **insertItem** .

A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se muestran ambas técnicas agregando el elemento multimedia actual a una lista de reproducción denominada "BluesTest", primero al final y, a continuación, al principio de la lista de reproducción.


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



Al crear una nueva lista de reproducción vacía mediante *PlaylistCollection*. método **reproducción** , puede agregar elementos multimedia a él mediante una llamada repetida a la *lista de reproducción*. método **appendItem** .

## <a name="manipulating-media-items-in-a-playlist"></a>Manipular elementos multimedia en una lista de reproducción

Puede cambiar la posición de un elemento multimedia en la lista de reproducción mediante la *lista de reproducción*. método **moveItem** . Especifique el elemento por su índice actual y, a continuación, especifique el nuevo índice. En el siguiente ejemplo de C# se mueve un elemento del índice 5 al índice 0 dentro de una lista de reproducción.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



Puede quitar un elemento multimedia de la lista de reproducción mediante la **lista de reproducción**. método **RemoveItem** . Tenga en cuenta que si el elemento quitado no era el elemento final de la lista de reproducción, cambian los valores de índice de los elementos subsiguientes. En el siguiente ejemplo de C# se quita el elemento especificado.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Los usuarios pueden cambiar el contenido de una lista de reproducción fuera de la aplicación. Siempre que manipule los elementos de una lista de reproducción, debe supervisar y controlar los eventos relacionados con la lista de reproducción del control de Windows Media Player para asegurarse de que el código funciona correctamente. Estos eventos son *Player*. **CurrentPlaylistChange** y *Player*. **PlaylistChange**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> </dl>

 

 




