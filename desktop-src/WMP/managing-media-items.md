---
title: Administrar elementos multimedia
description: Administrar elementos multimedia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, administrar elementos multimedia
- Biblioteca, administrar elementos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148857"
---
# <a name="managing-media-items"></a><span data-ttu-id="8981e-112">Administrar elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="8981e-112">Managing Media Items</span></span>

<span data-ttu-id="8981e-113">Un objeto **multimedia** representa un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="8981e-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="8981e-114">Tiene propiedades y métodos que puede usar para recuperar información y mostrarla al usuario, o para realizar diferentes acciones en función del valor que recupere.</span><span class="sxs-lookup"><span data-stu-id="8981e-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="8981e-115">Gran parte del trabajo con objetos **multimedia** implica metadatos sobre el contenido del elemento multimedia, denominados atributos.</span><span class="sxs-lookup"><span data-stu-id="8981e-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="8981e-116">El tema [atributos de elemento multimedia](media-item-attributes.md) describe cómo leer y cambiar los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="8981e-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="8981e-117">Además de este tema, consulte las instrucciones de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)) en el sitio web de Microsoft para obtener más información sobre los atributos y su uso.</span><span class="sxs-lookup"><span data-stu-id="8981e-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="8981e-118">El objeto **multimedia** tiene propiedades y métodos que recuperan algunos atributos directamente, como el nombre o la duración del elemento.</span><span class="sxs-lookup"><span data-stu-id="8981e-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="8981e-119">En el caso de los elementos de vídeo, puede recuperar el alto y el ancho de la imagen, y puede recuperar la información del marcador basándose en el nombre o el índice de un marcador.</span><span class="sxs-lookup"><span data-stu-id="8981e-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="8981e-120">También puede determinar si un elemento multimedia determinado se incluye en una lista de reproducción determinada.</span><span class="sxs-lookup"><span data-stu-id="8981e-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="8981e-121">Recuperación de un objeto multimedia</span><span class="sxs-lookup"><span data-stu-id="8981e-121">Retrieving a Media Object</span></span>

<span data-ttu-id="8981e-122">Puede obtener acceso rápidamente al elemento multimedia actual mediante el *reproductor*. propiedad **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="8981e-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="8981e-123">A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8981e-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="8981e-124">En el siguiente ejemplo de C# se recupera un objeto **multimedia** que representa el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="8981e-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="8981e-125">Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital mediante el *reproductor*. método **newMedia** .</span><span class="sxs-lookup"><span data-stu-id="8981e-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="8981e-126">Pasa el método a la ruta de acceso URL a un archivo multimedia digital y devuelve una referencia al nuevo objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="8981e-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="8981e-127">El método no agrega el nuevo objeto a la biblioteca directamente.</span><span class="sxs-lookup"><span data-stu-id="8981e-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="8981e-128">Sin embargo, puede pasar el objeto a la *lista de reproducción*. método **appendItem** o la *lista de reproducción*. método **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="8981e-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="8981e-129">En el siguiente ejemplo de C# se crea un objeto **multimedia** basado en uno de los ejemplos de medios digitales instalados con el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8981e-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="8981e-130">Debe incluir dos barras diagonales inversas ( \) o usar el carácter @ en C#) en una cadena para representar un carácter de barra diagonal inversa real.</span><span class="sxs-lookup"><span data-stu-id="8981e-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="8981e-131">Esto se debe a que C# usa un solo carácter de barra diagonal inversa para definir una secuencia de escape.</span><span class="sxs-lookup"><span data-stu-id="8981e-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="8981e-132">Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital y agregarlo a la biblioteca en un solo paso mediante el *MediaCollection*. **agregue** el método.</span><span class="sxs-lookup"><span data-stu-id="8981e-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="8981e-133">Como el *reproductor*. método **newMedia** , el método **Add** toma una ruta de acceso a un archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="8981e-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="8981e-134">En el siguiente ejemplo de C# se crea un objeto **multimedia** basado en uno de los archivos de ejemplo del SDK y se agrega ese objeto a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8981e-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="8981e-135">Puede recuperar un objeto **multimedia** que representa un elemento multimedia en una lista de reproducción mediante la *lista de reproducción*. método **Item** .</span><span class="sxs-lookup"><span data-stu-id="8981e-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="8981e-136">En el siguiente ejemplo de C# se recupera el sexto elemento multimedia de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="8981e-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="8981e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8981e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8981e-138">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="8981e-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="8981e-139">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="8981e-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="8981e-140">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="8981e-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="8981e-141">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="8981e-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="8981e-142">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="8981e-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="8981e-143">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="8981e-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="8981e-144">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="8981e-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="8981e-145">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="8981e-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




