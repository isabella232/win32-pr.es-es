---
title: Acerca de los objetos MediaCollection y multimedia
description: Acerca de los objetos MediaCollection y multimedia
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Media Player de Windows, objeto MediaCollection
- Modelo de objetos de Media Player de Windows, objeto MediaCollection
- modelo de objetos, MediaCollection (objeto)
- Control ActiveX de Windows Media Player, objeto MediaCollection
- Control ActiveX, objeto MediaCollection
- Control ActiveX de Windows Media Player Mobile, objeto MediaCollection
- Windows Media Player Mobile, objeto MediaCollection
- Objeto MediaCollection
- Windows Media Player, objeto multimedia
- Modelo de objetos de Windows Media Player, objeto multimedia
- modelo de objetos, objeto multimedia
- Control ActiveX de Windows Media Player, objeto multimedia
- Control ActiveX, objeto multimedia
- Control ActiveX móvil de Windows Media Player, objeto multimedia
- Windows Media Player Mobile, objeto multimedia
- Objeto multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695411"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="bd4c8-119">Acerca de los objetos MediaCollection y multimedia</span><span class="sxs-lookup"><span data-stu-id="bd4c8-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="bd4c8-120">Los objetos **MediaCollection** y **multimedia** rigen la colección de medios, que define las ubicaciones de los archivos multimedia digitales a los que puede tener acceso Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="bd4c8-121">Obtiene el objeto **MediaCollection** de la propiedad **MediaCollection** del objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="bd4c8-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="bd4c8-122">La propiedad **mediaCollection** devuelve el objeto **mediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="bd4c8-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="bd4c8-123">Solo puede acceder a las propiedades del objeto **MediaCollection** una vez creado.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="bd4c8-124">Por ejemplo, para agregar un objeto **multimedia** (una canción), use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="bd4c8-125">Ha agregado el archivo Laure. WMA a la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="bd4c8-126">Puede obtener el objeto **multimedia** actual mediante la propiedad **currentMedia** del **reproductor**.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="bd4c8-127">Por ejemplo, este código obtiene la propiedad **Duration** del objeto **multimedia** actual:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="bd4c8-128">Hay muchas maneras de obtener un objeto **multimedia** para poder tener acceso a sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="bd4c8-129">Por ejemplo, si desea tener acceso a la propiedad **Duration** del medio actual, se podría usar cada una de las siguientes líneas de código.</span><span class="sxs-lookup"><span data-stu-id="bd4c8-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="bd4c8-130">Para obtener la duración del contenido multimedia que se está reproduciendo actualmente:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="bd4c8-131">Para obtener la duración del medio actual en una lista de reproducción:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="bd4c8-132">Para obtener la duración del tercer elemento multimedia de una lista de reproducción:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="bd4c8-133">Para obtener la duración del tercer elemento multimedia en un género "Jazz":</span><span class="sxs-lookup"><span data-stu-id="bd4c8-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="bd4c8-134">Para obtener la duración del tercer elemento multimedia en la segunda lista de reproducción:</span><span class="sxs-lookup"><span data-stu-id="bd4c8-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="bd4c8-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd4c8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd4c8-136">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="bd4c8-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bd4c8-137">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="bd4c8-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="bd4c8-138">**Modelo de objetos del reproductor para lenguajes de scripting**</span><span class="sxs-lookup"><span data-stu-id="bd4c8-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




