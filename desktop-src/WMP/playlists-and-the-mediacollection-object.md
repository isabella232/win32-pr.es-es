---
title: Listas de reproducción y el objeto MediaCollection
description: Listas de reproducción y el objeto MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, objeto MediaCollection
- listas de reproducción de metarchivos, objeto MediaCollection
- Listas de reproducción de metarchivo de Windows Media, objeto MediaCollection
- Objeto MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418541"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="69b2b-114">Listas de reproducción y el objeto MediaCollection</span><span class="sxs-lookup"><span data-stu-id="69b2b-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="69b2b-115">El objeto **MediaCollection** proporciona acceso a varias listas de reproducción especiales e incluye un método para crear una nueva lista de reproducción a partir de un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="69b2b-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="69b2b-116">Los métodos siguientes recuperan listas de reproducción especiales:</span><span class="sxs-lookup"><span data-stu-id="69b2b-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="69b2b-117">**getAll**</span><span class="sxs-lookup"><span data-stu-id="69b2b-117">**getAll**</span></span>
-   <span data-ttu-id="69b2b-118">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="69b2b-118">**getByAlbum**</span></span>
-   <span data-ttu-id="69b2b-119">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="69b2b-119">**getByAttribute**</span></span>
-   <span data-ttu-id="69b2b-120">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="69b2b-120">**getByAuthor**</span></span>
-   <span data-ttu-id="69b2b-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="69b2b-121">**getByGenre**</span></span>
-   <span data-ttu-id="69b2b-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="69b2b-122">**getByName**</span></span>

<span data-ttu-id="69b2b-123">Como sugieren sus nombres, estos métodos recuperan listas de reproducción que contienen todos los elementos multimedia de la biblioteca que coinciden con determinados criterios.</span><span class="sxs-lookup"><span data-stu-id="69b2b-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="69b2b-124">Tenga cuidado de no confundir el *MediaCollection*. método **getByName** con *PlaylistCollection*. método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="69b2b-125">El método **MediaCollection** devuelve un objeto de **lista de reproducción** que contiene todos los elementos multimedia que tienen el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="69b2b-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="69b2b-126">El método **PlaylistCollection** devuelve un objeto **PlaylistArray** que contiene todas las listas de reproducción que tienen el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="69b2b-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="69b2b-127">Puede usar *MediaCollection*. **agregue** el método para agregar listas de reproducción y elementos multimedia a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="69b2b-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="69b2b-128">Para agregar una lista de reproducción, pase el método a la ruta de acceso al metarchivo que define la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="69b2b-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="69b2b-129">El método siempre devuelve un objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="69b2b-130">No se puede convertir entre objetos **multimedia** y de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="69b2b-131">Para trabajar con la lista de reproducción que ha agregado, recupere el objeto de **lista de reproducción** que tiene el mismo nombre que el objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="69b2b-132">En el siguiente ejemplo de C# se muestra cómo recuperar los elementos multimedia por tipo mediante **MediaCollection**. método **getByAttribute** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="69b2b-133">Este código recupera los nombres de todos los atributos asociados a un tipo determinado, así como el estado de lectura/escritura o de solo lectura de esos atributos.</span><span class="sxs-lookup"><span data-stu-id="69b2b-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="69b2b-134">Genera un único archivo que contiene listas de atributos para los tipos audio, vídeo, radio, lista de reproducción, otros, música y fotografías.</span><span class="sxs-lookup"><span data-stu-id="69b2b-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="69b2b-135">En el siguiente ejemplo de C# se muestra cómo agregar una lista de reproducción de un metarchivo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="69b2b-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="69b2b-136">Las listas de reproducción estáticas incluyen elementos multimedia específicos.</span><span class="sxs-lookup"><span data-stu-id="69b2b-136">Static playlists include specific media items.</span></span> <span data-ttu-id="69b2b-137">Las listas de reproducción automáticas buscan en la biblioteca cada vez que se abren y pueden contener diferentes elementos multimedia en momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="69b2b-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="69b2b-138">Puede Agregar listas de reproducción estáticas y automáticas a la biblioteca mediante *MediaCollection*. **agregue** el método.</span><span class="sxs-lookup"><span data-stu-id="69b2b-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="69b2b-139">También puede Agregar listas de reproducción estáticas mediante *PlaylistCollection*. método **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="69b2b-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69b2b-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69b2b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b2b-141">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="69b2b-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="69b2b-142">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="69b2b-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="69b2b-143">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="69b2b-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="69b2b-144">**Objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="69b2b-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="69b2b-145">**Listas de reproducción y el objeto PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="69b2b-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="69b2b-146">**Listas de reproducción estáticas y automáticas**</span><span class="sxs-lookup"><span data-stu-id="69b2b-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




