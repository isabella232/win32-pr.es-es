---
title: Atributos de lista de reproducción
description: Atributos de lista de reproducción
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media modelo de objetos, listas de reproducción
- modelo de objetos, listas de reproducción
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- playlists,attributes
- listas de reproducción de metarchivo, atributos
- Windows Listas de reproducción de metarchivo multimedia, atributos
- attributes,playlists
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359530"
---
# <a name="playlist-attributes"></a>Atributos de lista de reproducción

Las listas de reproducción tienen información de metadatos denominada atributos, igual que los elementos multimedia tienen atributos. Puede recuperar los nombres y valores de los atributos de lista de reproducción y mostrarlos en la interfaz de usuario, o bien el código puede realizar acciones en función del valor de un atributo.

Las listas de reproducción se definen en archivos organizados en formato XML y determinados elementos del archivo definen atributos de lista de reproducción. Algunos elementos de atributo son conocidos; el autor del metarchivo también puede definir atributos arbitrarios. Para obtener más información sobre los elementos de atributo en los archivos de lista de reproducción, vea [Recuperar metadatos.](retrieving-metadata.md)

La biblioteca puede proporcionar atributos de lista de reproducción adicionales, como **SourceURL** o **UserLastPlayedTime.** Para obtener más información sobre los atributos de lista de reproducción de biblioteca, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

Lista *de reproducción*. **La propiedad attributeCount** recupera el número de atributos asociados a la lista de reproducción. Lista *de reproducción*. **La propiedad attributeName** recupera el nombre de un atributo en función de su índice y la lista de *reproducción*. **El método getItemInfo** recupera el valor de un atributo en función de su nombre.

Puede modificar el valor de un atributo de la lista de reproducción actual con la lista de *reproducción*. **Método setItemInfo.**

Un uso especial del **método setItemInfo** consiste en ordenar los elementos de la lista de reproducción mediante el **atributo SortAttribute.** En el siguiente ejemplo de C# se ordena una lista de reproducción por los valores del **atributo UserLastPlayedTime.** La variable *Lista de reproducción* es una referencia a un objeto **Playlist.**


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



El siguiente código de ejemplo de C# muestra cómo recuperar atributos de lista de reproducción. La primera función, ShowPlaylists, rellena un control ListBox con los nombres de las listas de reproducción disponibles. La segunda parte es el controlador de eventos del cuadro de lista. Cuando el usuario hace clic en un nombre de lista de reproducción, este código recupera los atributos de esa lista de reproducción y muestra esos atributos en un segundo cuadro de lista.


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

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Atributos de elementos multimedia**](media-item-attributes.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 




