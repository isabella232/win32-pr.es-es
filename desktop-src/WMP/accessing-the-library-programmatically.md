---
title: Obtener acceso a la biblioteca mediante programación
description: Obtener acceso a la biblioteca mediante programación
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, obtener acceso mediante programación
- Biblioteca, acceso
- obtener acceso a la biblioteca de Windows Media Player mediante programación
- Biblioteca de Media Player de Windows, agregar elementos multimedia
- Biblioteca, agregar elementos multimedia
- Biblioteca de Media Player de Windows, recuperar elementos multimedia
- Biblioteca, recuperar elementos multimedia
- Biblioteca de Media Player de Windows, quitar elementos multimedia
- Biblioteca, quitar elementos multimedia
- agregar elementos multimedia a la biblioteca de Windows Media Player
- recuperar elementos multimedia de la biblioteca de Media Player de Windows
- quitar elementos multimedia de la biblioteca de Media Player de Windows
- recuperar metadatos
- Biblioteca de Media Player de Windows, recuperar metadatos de elementos multimedia
- Biblioteca, recuperar metadatos de elementos multimedia
- metadatos, recuperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418906"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="9678c-126">Obtener acceso a la biblioteca mediante programación</span><span class="sxs-lookup"><span data-stu-id="9678c-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="9678c-127">En el código, la biblioteca se representa mediante el objeto **MediaCollection** (o la interfaz **IWMPMediaCollection** ).</span><span class="sxs-lookup"><span data-stu-id="9678c-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="9678c-128">Los elementos multimedia se representan como objetos **multimedia** (o mediante la interfaz **IWMPMedia** ).</span><span class="sxs-lookup"><span data-stu-id="9678c-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="9678c-129">Los elementos de la lista de reproducción se representan como objetos de **lista de reproducción** (o por la interfaz **IWMPPlaylist** ).</span><span class="sxs-lookup"><span data-stu-id="9678c-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="9678c-130">Para simplificar, esta sección simplemente hará referencia a los nombres de objeto, siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="9678c-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="9678c-131">Con el objeto **MediaCollection** , puede trabajar con elementos multimedia y listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9678c-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="9678c-132">La biblioteca también expone el objeto **PlaylistCollection** (o la interfaz **IWMPPlaylistCollection** ), que proporciona cierta funcionalidad específica para trabajar con listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9678c-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="9678c-133">La mayoría de las veces, el objeto **MediaCollection** le proporcionará la funcionalidad que necesita, incluso al trabajar con listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9678c-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="9678c-134">Para obtener más información sobre cómo trabajar con elementos multimedia, vea [administrar elementos multimedia](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="9678c-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="9678c-135">Para obtener más información sobre cómo trabajar con listas de reproducción, consulte [Administración de listas de reproducción](managing-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="9678c-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="9678c-136">Agregar elementos multimedia a la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9678c-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="9678c-137">Agregar contenido multimedia digital a la biblioteca es sencillo.</span><span class="sxs-lookup"><span data-stu-id="9678c-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="9678c-138">Simplemente llame al método [MediaCollection. Add](mediacollection-add.md) y proporcione la ruta de acceso al archivo multimedia como un argumento.</span><span class="sxs-lookup"><span data-stu-id="9678c-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="9678c-139">Recuperar elementos multimedia de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9678c-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="9678c-140">Al recuperar elementos multimedia de la biblioteca, lo que realmente recupera es una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9678c-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="9678c-141">Incluso si espera recuperar solo un elemento multimedia, obtendrá un objeto de lista de **reproducción** que contiene un solo elemento, que se asociará con el índice cero.</span><span class="sxs-lookup"><span data-stu-id="9678c-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="9678c-142">Por ejemplo, si desea recuperar un objeto **multimedia** que representa la canción denominada "Jeanne", puede usar el siguiente código JScript:</span><span class="sxs-lookup"><span data-stu-id="9678c-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="9678c-143">En el código anterior se recupera una lista de reproducción que contiene todos los elementos multimedia que tienen el nombre "Jeanne" como título.</span><span class="sxs-lookup"><span data-stu-id="9678c-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="9678c-144">En este ejemplo, suponga que sabe que solo hay una canción con ese nombre en la biblioteca (tenga en cuenta que la biblioteca admite varias canciones con el mismo nombre).</span><span class="sxs-lookup"><span data-stu-id="9678c-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="9678c-145">Esto significa que puede esperar que el número de elementos de la lista de reproducción que recupere sea igual a uno y que el elemento multimedia se represente mediante el índice cero.</span><span class="sxs-lookup"><span data-stu-id="9678c-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="9678c-146">El código de ejemplo siguiente continúa el ejemplo anterior para mostrar cómo se recuperaría el elemento multimedia de la lista de reproducción mediante el método [playlist. Item](playlist-item.md) .</span><span class="sxs-lookup"><span data-stu-id="9678c-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="9678c-147">Para obtener más información acerca de cómo recuperar elementos multimedia de listas de reproducción, vea [listas de reproducción y elementos multimedia](playlists-and-media-items.md) en la [Guía de control del reproductor](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="9678c-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="9678c-148">Recuperar metadatos de un elemento multimedia</span><span class="sxs-lookup"><span data-stu-id="9678c-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="9678c-149">Después de recuperar un objeto **multimedia** , puede leer los valores de atributo asociados con el contenido.</span><span class="sxs-lookup"><span data-stu-id="9678c-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="9678c-150">En el caso más simple, es posible que solo desee conocer un valor único, como el nombre del artista que realizó una pista de música. En el ejemplo de JScript siguiente se muestra cómo utilizar el método [media. getItemInfo](media-getiteminfo.md) para recuperar el nombre del artista del medio recuperado en el ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="9678c-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="9678c-151">Un elemento multimedia puede tener muchos atributos diferentes y trabajar con metadatos no siempre es tan sencillo como el caso simple que se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="9678c-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="9678c-152">Por ejemplo, algunos atributos pueden contener varios valores o tener valores en más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="9678c-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="9678c-153">Para obtener más información sobre cómo trabajar con metadatos, vea [atributos de elemento multimedia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9678c-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="9678c-154">Para obtener más información sobre los distintos atributos, su significado y la compatibilidad con tipos de archivo, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9678c-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="9678c-155">Quitar elementos multimedia de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="9678c-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="9678c-156">Quitar el contenido multimedia digital de la biblioteca también es sencillo.</span><span class="sxs-lookup"><span data-stu-id="9678c-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="9678c-157">Simplemente llame a **MediaCollection. Remove**, proporcionando el objeto **multimedia** que representa el elemento como primer argumento y el valor **true** como segundo.</span><span class="sxs-lookup"><span data-stu-id="9678c-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="9678c-158">En el siguiente ejemplo de JScript se quita el archivo denominado Jeanne (recuperado en el ejemplo anterior) de la biblioteca:</span><span class="sxs-lookup"><span data-stu-id="9678c-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="9678c-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9678c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9678c-160">**Acerca de la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="9678c-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="9678c-161">**Acerca de los objetos MediaCollection y multimedia**</span><span class="sxs-lookup"><span data-stu-id="9678c-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="9678c-162">**Acerca de los objetos playlist, PlaylistCollection y PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="9678c-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="9678c-163">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="9678c-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




