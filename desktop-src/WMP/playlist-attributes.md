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
# <a name="playlist-attributes"></a><span data-ttu-id="2c60c-114">Atributos de lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="2c60c-114">Playlist Attributes</span></span>

<span data-ttu-id="2c60c-115">Las listas de reproducción tienen información de metadatos denominada atributos, del mismo modo que los elementos multimedia tienen atributos.</span><span class="sxs-lookup"><span data-stu-id="2c60c-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="2c60c-116">Puede recuperar los nombres y valores de los atributos de la lista de reproducción y mostrarlos en la interfaz de usuario, o bien el código puede realizar acciones basadas en el valor de un atributo.</span><span class="sxs-lookup"><span data-stu-id="2c60c-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="2c60c-117">Las listas de reproducción se definen en archivos organizados en formato XML y los elementos concretos del archivo definen los atributos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2c60c-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="2c60c-118">Algunos elementos de atributo son conocidos; el autor del metarchivo también puede definir atributos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="2c60c-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="2c60c-119">Para obtener más información sobre los elementos de atributo en los archivos de lista de reproducción, vea [recuperar metadatos](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="2c60c-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="2c60c-120">La biblioteca puede proporcionar atributos adicionales de la lista de reproducción, como **SourceURL** o **UserLastPlayedTime**.</span><span class="sxs-lookup"><span data-stu-id="2c60c-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="2c60c-121">Para obtener más información acerca de los atributos de la lista de reproducción de la biblioteca, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2c60c-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="2c60c-122">*Lista de reproducción*. la propiedad **attributeCount** recupera el número de atributos asociados a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2c60c-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="2c60c-123">*Lista de reproducción*. la propiedad **attributeName** recupera el nombre de un atributo basándose en su índice y en la *lista de reproducción*. el método **getItemInfo** recupera el valor de un atributo basándose en su nombre.</span><span class="sxs-lookup"><span data-stu-id="2c60c-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="2c60c-124">Puede modificar el valor de un atributo de la lista de reproducción actual con la *lista de reproducción*. método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="2c60c-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="2c60c-125">Un uso especial del método **setItemInfo** es ordenar los elementos de la lista de reproducción mediante el atributo **SortAttribute** .</span><span class="sxs-lookup"><span data-stu-id="2c60c-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="2c60c-126">En el siguiente ejemplo de C# se ordena una lista de reproducción por los valores del atributo **UserLastPlayedTime** .</span><span class="sxs-lookup"><span data-stu-id="2c60c-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="2c60c-127">La *lista de reproducción* de variables es una referencia a un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="2c60c-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="2c60c-128">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2c60c-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="2c60c-129">En el siguiente código de ejemplo de C# se muestra cómo recuperar los atributos de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2c60c-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="2c60c-130">La primera función, ShowPlaylists, rellena un control ListBox con los nombres de las listas de reproducción disponibles.</span><span class="sxs-lookup"><span data-stu-id="2c60c-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="2c60c-131">La segunda parte es el controlador de eventos del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2c60c-131">The second part is the list box event handler.</span></span> <span data-ttu-id="2c60c-132">Cuando el usuario hace clic en un nombre de lista de reproducción, este código recupera los atributos de la lista de reproducción y muestra esos atributos en un segundo cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2c60c-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


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



<span data-ttu-id="2c60c-133">Se llama al evento SelectedIndexChanged para el control ListBox cada vez que el usuario selecciona un nombre de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2c60c-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="2c60c-134">El siguiente controlador de eventos rellena un segundo cuadro de lista con los nombres de atributo y los valores correspondientes a la selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="2c60c-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2c60c-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c60c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c60c-136">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="2c60c-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="2c60c-137">**Atributos de elemento multimedia**</span><span class="sxs-lookup"><span data-stu-id="2c60c-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c60c-138">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="2c60c-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




