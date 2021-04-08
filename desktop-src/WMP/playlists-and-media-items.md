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
# <a name="playlists-and-media-items"></a><span data-ttu-id="491ff-113">Listas de reproducción y elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="491ff-113">Playlists and Media Items</span></span>

<span data-ttu-id="491ff-114">Una lista de reproducción es un conjunto de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="491ff-114">A playlist is a set of media items.</span></span> <span data-ttu-id="491ff-115">Un objeto de **lista de reproducción** puede manipular los objetos **multimedia** que representan dichos elementos.</span><span class="sxs-lookup"><span data-stu-id="491ff-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="491ff-116">Recuperar elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="491ff-116">Retrieving Media Items</span></span>

<span data-ttu-id="491ff-117">En el caso de una lista de reproducción existente, puede leer la *lista de reproducción*. propiedad **Count** para determinar el número de elementos multimedia que hay en la lista de reproducción y puede obtener una referencia al objeto **multimedia** correspondiente a un elemento específico mediante la *lista de reproducción*. propiedad del **elemento** .</span><span class="sxs-lookup"><span data-stu-id="491ff-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="491ff-118">En el siguiente ejemplo de C# se recupera una referencia de objeto a un elemento multimedia específico.</span><span class="sxs-lookup"><span data-stu-id="491ff-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="491ff-119">(A lo largo de este tema, la variable *plist* es una referencia a un objeto de **lista de reproducción** ).</span><span class="sxs-lookup"><span data-stu-id="491ff-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="491ff-120">En el siguiente ejemplo de C# se recuperan los nombres de todos los elementos multimedia de una lista de reproducción y se colocan en un control ListBox denominado lstOutput.</span><span class="sxs-lookup"><span data-stu-id="491ff-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="491ff-121">Agregar elementos a una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="491ff-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="491ff-122">Puede Agregar un elemento multimedia al final de una lista de reproducción o a una posición específica de una lista de reproducción, mediante la *lista de reproducción*. **appendItem** y *lista de reproducción*. métodos **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="491ff-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="491ff-123">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="491ff-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="491ff-124">En el siguiente ejemplo de C# se muestran ambas técnicas agregando el elemento multimedia actual a una lista de reproducción denominada "BluesTest", primero al final y, a continuación, al principio de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="491ff-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


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



<span data-ttu-id="491ff-125">Al crear una nueva lista de reproducción vacía mediante *PlaylistCollection*. método **reproducción** , puede agregar elementos multimedia a él mediante una llamada repetida a la *lista de reproducción*. método **appendItem** .</span><span class="sxs-lookup"><span data-stu-id="491ff-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="491ff-126">Manipular elementos multimedia en una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="491ff-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="491ff-127">Puede cambiar la posición de un elemento multimedia en la lista de reproducción mediante la *lista de reproducción*. método **moveItem** .</span><span class="sxs-lookup"><span data-stu-id="491ff-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="491ff-128">Especifique el elemento por su índice actual y, a continuación, especifique el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="491ff-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="491ff-129">En el siguiente ejemplo de C# se mueve un elemento del índice 5 al índice 0 dentro de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="491ff-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="491ff-130">Puede quitar un elemento multimedia de la lista de reproducción mediante la **lista de reproducción**. método **RemoveItem** .</span><span class="sxs-lookup"><span data-stu-id="491ff-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="491ff-131">Tenga en cuenta que si el elemento quitado no era el elemento final de la lista de reproducción, cambian los valores de índice de los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="491ff-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="491ff-132">En el siguiente ejemplo de C# se quita el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="491ff-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="491ff-133">Los usuarios pueden cambiar el contenido de una lista de reproducción fuera de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491ff-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="491ff-134">Siempre que manipule los elementos de una lista de reproducción, debe supervisar y controlar los eventos relacionados con la lista de reproducción del control de Windows Media Player para asegurarse de que el código funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="491ff-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="491ff-135">Estos eventos son *Player*. **CurrentPlaylistChange** y *Player*. **PlaylistChange**.</span><span class="sxs-lookup"><span data-stu-id="491ff-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="491ff-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="491ff-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491ff-137">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="491ff-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="491ff-138">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="491ff-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="491ff-139">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="491ff-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




