---
title: Acerca de los objetos playlist, PlaylistCollection y PlaylistArray
description: Acerca de los objetos playlist, PlaylistCollection y PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, objeto Playlist
- Modelo de objetos de Windows Media Player, objeto Playlist
- modelo de objetos, objeto Playlist
- Control ActiveX de Windows Media Player, objeto Playlist
- Control ActiveX, objeto Playlist
- Control ActiveX móvil de Windows Media Player, objeto Playlist
- Windows Media Player Mobile, objeto de lista de reproducción
- Objeto Playlist
- Media Player de Windows, objeto PlaylistCollection
- Modelo de objetos de Media Player de Windows, objeto PlaylistCollection
- modelo de objetos, PlaylistCollection (objeto)
- Control ActiveX de Windows Media Player, objeto PlaylistCollection
- Control ActiveX, objeto PlaylistCollection
- Control ActiveX de Windows Media Player Mobile, objeto PlaylistCollection
- Windows Media Player Mobile, objeto PlaylistCollection
- Objeto PlaylistCollection
- Media Player de Windows, objeto PlaylistArray
- Modelo de objetos de Media Player de Windows, objeto PlaylistArray
- modelo de objetos, PlaylistArray (objeto)
- Control ActiveX de Windows Media Player, objeto PlaylistArray
- Control ActiveX, objeto PlaylistArray
- Control ActiveX de Windows Media Player Mobile, objeto PlaylistArray
- Windows Media Player Mobile, objeto PlaylistArray
- Objeto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695316"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="69c25-127">Acerca de los objetos playlist, PlaylistCollection y PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="69c25-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="69c25-128">Los objetos **playlist**, **PlaylistCollection** y **PlaylistArray** rigen las listas de reproducción que Windows Media Player puede usar para especificar el orden en el que se reproducirá el contenido.</span><span class="sxs-lookup"><span data-stu-id="69c25-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="69c25-129">Obtiene el objeto **PlaylistCollection** de la propiedad **PlaylistCollection** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="69c25-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="69c25-130">La propiedad **playlistCollection** devuelve el objeto **playlistCollection** .</span><span class="sxs-lookup"><span data-stu-id="69c25-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="69c25-131">Solo puede acceder a las propiedades del objeto **PlaylistCollection** una vez creado.</span><span class="sxs-lookup"><span data-stu-id="69c25-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="69c25-132">Por ejemplo, para crear una nueva lista de reproducción, primero debe obtener el objeto **PlaylistCollection** y, a continuación, usar un método en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="69c25-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="69c25-133">Puede obtener la lista de reproducción actual mediante la propiedad **currentPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="69c25-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="69c25-134">Por ejemplo, para obtener el nombre de la lista de reproducción actual, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="69c25-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="69c25-135">Los métodos **getAll** y **GetByName** del objeto **PlaylistCollection** devuelven el objeto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="69c25-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="69c25-136">Para obtener el número de listas de reproducción, por ejemplo, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="69c25-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="69c25-137">Para recuperar una lista de reproducción conocida por nombre, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="69c25-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="69c25-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69c25-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69c25-139">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="69c25-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="69c25-140">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="69c25-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="69c25-141">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="69c25-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="69c25-142">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="69c25-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




