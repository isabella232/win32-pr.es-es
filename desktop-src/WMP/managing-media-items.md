---
title: Administración de elementos multimedia
description: Administración de elementos multimedia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos,library
- object model,library
- Reproductor de Windows Media Móvil,biblioteca para el modelo de objetos
- Reproductor de Windows Media control ActiveX, biblioteca para el modelo de objetos
- Reproductor de Windows Media control ActiveX móvil,biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Reproductor de Windows Media, administrar elementos multimedia
- library,managing media items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386894"
---
# <a name="managing-media-items"></a><span data-ttu-id="68b74-112">Administración de elementos multimedia</span><span class="sxs-lookup"><span data-stu-id="68b74-112">Managing Media Items</span></span>

<span data-ttu-id="68b74-113">Un **objeto Media** representa un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="68b74-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="68b74-114">Tiene propiedades y métodos que puede usar para recuperar información y mostrarla al usuario, o para realizar diferentes acciones en función del valor que recupere.</span><span class="sxs-lookup"><span data-stu-id="68b74-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="68b74-115">Gran parte del trabajo con objetos **Multimedia** implica metadatos sobre el contenido del elemento multimedia, denominados atributos.</span><span class="sxs-lookup"><span data-stu-id="68b74-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="68b74-116">En el tema [Atributos de elementos multimedia](media-item-attributes.md) se describe cómo leer y cambiar los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="68b74-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="68b74-117">Además de este tema, consulte las Directrices de uso de metadatos de [Windows Media](/previous-versions/ms867702(v=msdn.10)) en el sitio web de Microsoft para obtener más información sobre los atributos y su uso.</span><span class="sxs-lookup"><span data-stu-id="68b74-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="68b74-118">El **objeto** Media tiene propiedades y métodos que recuperan algunos atributos directamente, como el nombre o la duración del elemento.</span><span class="sxs-lookup"><span data-stu-id="68b74-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="68b74-119">En el caso de los elementos de vídeo, puede recuperar el alto y el ancho de la imagen, y puede recuperar información de marcador basada en el nombre o índice de un marcador.</span><span class="sxs-lookup"><span data-stu-id="68b74-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="68b74-120">También puede determinar si un elemento multimedia determinado está incluido en una lista de reproducción determinada.</span><span class="sxs-lookup"><span data-stu-id="68b74-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="68b74-121">Recuperar un objeto multimedia</span><span class="sxs-lookup"><span data-stu-id="68b74-121">Retrieving a Media Object</span></span>

<span data-ttu-id="68b74-122">Puede acceder rápidamente al elemento multimedia actual mediante el Reproductor *de*. **propiedad currentMedia.**</span><span class="sxs-lookup"><span data-stu-id="68b74-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="68b74-123">A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="68b74-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="68b74-124">En el siguiente ejemplo de C# se recupera un **objeto Media** que representa el elemento actual.</span><span class="sxs-lookup"><span data-stu-id="68b74-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="68b74-125">Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital mediante el *Reproductor de*. **método newMedia.**</span><span class="sxs-lookup"><span data-stu-id="68b74-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="68b74-126">Se pasa al método la ruta de acceso url a un archivo multimedia digital y se devuelve una referencia al nuevo **objeto Media.**</span><span class="sxs-lookup"><span data-stu-id="68b74-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="68b74-127">El método no agrega directamente el nuevo objeto a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="68b74-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="68b74-128">Sin embargo, puede pasar el objeto a la lista de *reproducción*. **Método appendItem** o lista *de reproducción*. **Método insertItem.**</span><span class="sxs-lookup"><span data-stu-id="68b74-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="68b74-129">En el siguiente ejemplo de C# se crea un **objeto Media** basado en uno de los ejemplos de medios digitales instalados con Reproductor de Windows Media SDK.</span><span class="sxs-lookup"><span data-stu-id="68b74-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="68b74-130">Debe incluir dos caracteres de barra diagonal inversa ( ) (o usar el carácter @ en C#) en una cadena para representar un carácter de barra diagonal \\ inversa real.</span><span class="sxs-lookup"><span data-stu-id="68b74-130">You must include two backslash (\\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="68b74-131">Esto se debe a que C# usa un único carácter de barra diagonal inversa para definir una secuencia de escape.</span><span class="sxs-lookup"><span data-stu-id="68b74-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="68b74-132">Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital y agregarlo a la biblioteca en un paso mediante *MediaCollection*. **add** method.</span><span class="sxs-lookup"><span data-stu-id="68b74-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="68b74-133">Al igual que *el reproductor*. **método newMedia,** el **método add** toma una ruta de acceso a un archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="68b74-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="68b74-134">En el siguiente ejemplo de C# se crea un **objeto Media** basado en uno de los archivos de ejemplo del SDK y se agrega ese objeto a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="68b74-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="68b74-135">Puede recuperar un objeto **Media que representa** un elemento multimedia en una lista de reproducción mediante la lista de *reproducción*. **método item.**</span><span class="sxs-lookup"><span data-stu-id="68b74-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="68b74-136">En el siguiente ejemplo de C# se recupera el sexto elemento multimedia de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="68b74-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="68b74-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68b74-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68b74-138">**Controls.currentItem**</span><span class="sxs-lookup"><span data-stu-id="68b74-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="68b74-139">**Administración de listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="68b74-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="68b74-140">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="68b74-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="68b74-141">**MediaCollection.add**</span><span class="sxs-lookup"><span data-stu-id="68b74-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="68b74-142">**Player.currentMedia**</span><span class="sxs-lookup"><span data-stu-id="68b74-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="68b74-143">**Player.newMedia**</span><span class="sxs-lookup"><span data-stu-id="68b74-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="68b74-144">**Playlist.item**</span><span class="sxs-lookup"><span data-stu-id="68b74-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="68b74-145">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="68b74-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




