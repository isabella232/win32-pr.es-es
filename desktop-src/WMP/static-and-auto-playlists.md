---
title: Listas de reproducción estáticas y automáticas
description: Listas de reproducción estáticas y automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, estáticas
- listas de reproducción de metarchivo, estáticas
- Listas de reproducción de metarchivos de Windows Media, estáticas
- listas de reproducción estáticas
- listas de reproducción automáticas
- listas de reproducción, auto
- listas de reproducción de metarchivo, automática
- Listas de reproducción de metarchivos de Windows Media, automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418447"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="ba2ca-118">Listas de reproducción estáticas y automáticas</span><span class="sxs-lookup"><span data-stu-id="ba2ca-118">Static and Auto Playlists</span></span>

<span data-ttu-id="ba2ca-119">Hay dos tipos de listas de reproducción:</span><span class="sxs-lookup"><span data-stu-id="ba2ca-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="ba2ca-120">Listas de reproducción estáticas, que incluyen elementos multimedia específicos</span><span class="sxs-lookup"><span data-stu-id="ba2ca-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="ba2ca-121">Listas de reproducción automáticas, que buscan en la biblioteca cada vez que se abren y pueden contener diferentes elementos multimedia en momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="ba2ca-122">Una lista de reproducción automática es el resultado de una consulta de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="ba2ca-123">Para importar una lista de reproducción estática desde un metarchivo, primero llame a *Player*. **reproducción** para crear un objeto de **lista de reproducción** basado en los datos del metarchivo y, a continuación, pase ese objeto a *PlaylistCollection*. **importPlaylist** para agregar la lista de reproducción a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="ba2ca-124">Para importar una lista de reproducción automática desde un metarchivo, use *MediaCollection*. **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="ba2ca-125">Para obtener más información, vea [listas de reproducción y el objeto MediaCollection](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="ba2ca-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="ba2ca-126">Para importar una lista de reproducción estática de un metarchivo de lista de reproducción automática, use *Player*. **reproducción** y *PlaylistCollection*. **importPlaylist** como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="ba2ca-127">La lista de reproducción automática se ejecutará una vez y se creará una lista de reproducción estática según el resultado de esa ejecución.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="ba2ca-128">No se admite el uso de una lista de reproducción automática para consultar la biblioteca del usuario para las páginas web a las que los usuarios tienen acceso a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="ba2ca-129">El siguiente código de ejemplo de C# muestra cómo importar un metarchivo de lista de reproducción automática como una lista de reproducción estática.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="ba2ca-130">Para ejecutar este ejemplo, cree una lista de reproducción automática mediante la interfaz de usuario de la biblioteca y, a continuación, incluya la ruta de acceso correcta al metarchivo de lista de reproducción automática en este código.</span><span class="sxs-lookup"><span data-stu-id="ba2ca-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="ba2ca-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba2ca-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba2ca-132">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="ba2ca-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




