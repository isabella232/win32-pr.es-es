---
title: Listas de reproducción y el objeto PlaylistCollection
description: Listas de reproducción y el objeto PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, objeto PlaylistCollection
- listas de reproducción de metarchivos, objeto PlaylistCollection
- Listas de reproducción de metarchivo de Windows Media, objeto PlaylistCollection
- Objeto PlaylistCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704615"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="777e6-114">Listas de reproducción y el objeto PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="777e6-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="777e6-115">El objeto **PlaylistCollection** proporciona acceso a las listas de reproducción de la biblioteca y tiene métodos para crear listas de reproducción nuevas y vacías, así como nuevas listas de reproducción de los metaarchivos.</span><span class="sxs-lookup"><span data-stu-id="777e6-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="777e6-116">Trabajar con listas de reproducción existentes</span><span class="sxs-lookup"><span data-stu-id="777e6-116">Working with Existing Playlists</span></span>

<span data-ttu-id="777e6-117">*PlaylistCollection*. **getAll** y *PlaylistCollection*. cada método de **getByName** devuelve un objeto **PlaylistArray** , que puede contener varias listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="777e6-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="777e6-118">*PlaylistCollection*. **getAll** (método) devuelve todas las listas de reproducción existentes que se encuentran en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="777e6-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="777e6-119">Por ejemplo, puede llamar a este método y, a continuación, recuperar las listas de reproducción en el objeto **PlaylistArray** para determinar si ya se ha utilizado un nombre de lista de reproducción determinado, o para mostrar todas las listas de reproducción al usuario.</span><span class="sxs-lookup"><span data-stu-id="777e6-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="777e6-120">El código de ejemplo de [los atributos](playlist-attributes.md) de la lista de reproducción utiliza el método **getAll** .</span><span class="sxs-lookup"><span data-stu-id="777e6-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="777e6-121">*PlaylistCollection*. el método **getByName** devuelve todas las listas de reproducción con un nombre determinado.</span><span class="sxs-lookup"><span data-stu-id="777e6-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="777e6-122">Puede usar este método para controlar cada una de esas listas de reproducción por separado.</span><span class="sxs-lookup"><span data-stu-id="777e6-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="777e6-123">También puede usar el método **getByName** para recuperar una lista de reproducción única por nombre.</span><span class="sxs-lookup"><span data-stu-id="777e6-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="777e6-124">En ese caso, el objeto **PlaylistArray** tiene solo un elemento.</span><span class="sxs-lookup"><span data-stu-id="777e6-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="777e6-125">En el siguiente ejemplo de C# se muestra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="777e6-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="777e6-126">Trabajar con nuevas listas de reproducción</span><span class="sxs-lookup"><span data-stu-id="777e6-126">Working with New Playlists</span></span>

<span data-ttu-id="777e6-127">Puede usar *PlaylistCollection*. método **reproducción** para crear una nueva lista de reproducción vacía.</span><span class="sxs-lookup"><span data-stu-id="777e6-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="777e6-128">El método devuelve una referencia al nuevo objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="777e6-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="777e6-129">Después, puede llamar a la *lista de reproducción*. método **appendItem** para agregar elementos multimedia a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="777e6-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="777e6-130">También puede crear una nueva lista de reproducción basada en un metarchivo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="777e6-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="777e6-131">En primer lugar, pase el nombre de la lista de reproducción y la ruta de acceso al metarchivo al *reproductor*. método **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="777e6-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="777e6-132">Ese método devuelve una referencia al nuevo objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="777e6-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="777e6-133">A continuación, pase el nuevo objeto de **lista de reproducción** a *PlaylistCollection*. método **importPlaylist** para agregarlo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="777e6-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="777e6-134">Observe la diferencia entre *PlaylistCollection*. método **reproducción** y el *reproductor*. método **reproducción** .</span><span class="sxs-lookup"><span data-stu-id="777e6-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="777e6-135">El método **PlaylistCollection** crea una lista de reproducción nueva y vacía y la agrega a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="777e6-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="777e6-136">El método **Player** crea un nuevo objeto de **lista de reproducción** rellenado, pero no lo agrega a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="777e6-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="777e6-137">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="777e6-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="777e6-138">En el siguiente ejemplo de C# se muestra cómo importar una lista de reproducción de un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="777e6-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="777e6-139">El argumento *strPListName* especifica el nombre de la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="777e6-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="777e6-140">*StrMetaFileName* especifica el nombre del metarchivo del que se importa la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="777e6-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="777e6-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="777e6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="777e6-142">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="777e6-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="777e6-143">**Player. reproducción**</span><span class="sxs-lookup"><span data-stu-id="777e6-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="777e6-144">**Lista de reproducción. appendItem**</span><span class="sxs-lookup"><span data-stu-id="777e6-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="777e6-145">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="777e6-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="777e6-146">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="777e6-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="777e6-147">**Listas de reproducción y elementos multimedia**</span><span class="sxs-lookup"><span data-stu-id="777e6-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




