---
title: Atributos de lista de reproducción
description: Atributos de lista de reproducción
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, atributos
- metarchivos, listas de reproducción, atributos
- Listas de reproducción de metarchivos de Windows Media, atributos
- atributos, listas de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994098"
---
# <a name="playlist-attributes"></a>Atributos de lista de reproducción

Las listas de reproducción tienen información de metadatos denominada atributos, del mismo modo que los elementos multimedia tienen atributos. Puede recuperar los nombres y valores de los atributos de la lista de reproducción y mostrarlos en la interfaz de usuario, o bien el código puede realizar acciones basadas en el valor de un atributo.

Las listas de reproducción se definen en archivos organizados en formato XML y los elementos concretos del archivo definen los atributos de la lista de reproducción. Algunos elementos de atributo son conocidos; el autor del metarchivo también puede definir atributos arbitrarios. Para obtener más información sobre los elementos de atributo en los archivos de lista de reproducción, vea [recuperar metadatos](retrieving-metadata.md).

La biblioteca puede proporcionar atributos adicionales de la lista de reproducción, como **SourceURL** o **UserLastPlayedTime**. Para obtener más información acerca de los atributos de la lista de reproducción de la biblioteca, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

*Lista de reproducción*. la propiedad **attributeCount** recupera el número de atributos asociados a la lista de reproducción. *Lista de reproducción*. la propiedad **attributeName** recupera el nombre de un atributo basándose en su índice y en la *lista de reproducción*. el método **getItemInfo** recupera el valor de un atributo basándose en su nombre.

Puede modificar el valor de un atributo de la lista de reproducción actual con la *lista de reproducción*. método **setItemInfo** .

Un uso especial del método **setItemInfo** es ordenar los elementos de la lista de reproducción mediante el atributo **SortAttribute** . En el siguiente ejemplo de C# se ordena una lista de reproducción por los valores del atributo **UserLastPlayedTime** . La *lista de reproducción* de variables es una referencia a un objeto de **lista de reproducción** .


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente código de ejemplo de C# se muestra cómo recuperar los atributos de la lista de reproducción. La primera función, ShowPlaylists, rellena un control ListBox con los nombres de las listas de reproducción disponibles. La segunda parte es el controlador de eventos del cuadro de lista. Cuando el usuario hace clic en un nombre de lista de reproducción, este código recupera los atributos de la lista de reproducción y muestra esos atributos en un segundo cuadro de lista.


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



Se llama al evento SelectedIndexChanged para el control ListBox cada vez que el usuario selecciona un nombre de lista de reproducción. El siguiente controlador de eventos rellena un segundo cuadro de lista con los nombres de atributo y los valores correspondientes a la selección del usuario.


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Atributos de elemento multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> </dl>

 

 




