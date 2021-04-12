---
title: Usar el modelo de objetos de Windows Media Player 7 o posterior
description: Usar el modelo de objetos de Windows Media Player 7 o posterior
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, versión 7 o posterior
- modelo de objetos, versión 7 o posterior
- Windows Media Player control ActiveX, versión 7 o posterior
- Control ActiveX, versión 7 o posterior
- Windows Media Player Mobile ActiveX Control, versión 7 o posterior
- Windows Media Player Mobile, modelo de objetos
- Guía de migración, versión 7 o posterior
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357280"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="aefb9-112">Usar el modelo de objetos de Windows Media Player 7 o posterior</span><span class="sxs-lookup"><span data-stu-id="aefb9-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="aefb9-113">La mayoría de las tareas que se pueden haber realizado con el modelo de objetos de control ActiveX de Windows Media Player 6,4 requerirán un enfoque nuevo.</span><span class="sxs-lookup"><span data-stu-id="aefb9-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="aefb9-114">En muchos casos, los nombres de las propiedades, métodos y eventos han cambiado en el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="aefb9-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="aefb9-115">Por ejemplo, para especificar la ruta de acceso del archivo en el modelo de objetos de la versión 6,4, establezca la propiedad **Player6. FileName** :</span><span class="sxs-lookup"><span data-stu-id="aefb9-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="aefb9-116">Al usar el modelo de objetos de Windows Media Player 7 o posterior, debe establecer la propiedad **Player. URL** :</span><span class="sxs-lookup"><span data-stu-id="aefb9-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="aefb9-117">También puede usar el modelo de objetos 10 para obtener un objeto **multimedia** de la biblioteca y, a continuación, establecer la propiedad **Player. currentMedia** :</span><span class="sxs-lookup"><span data-stu-id="aefb9-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="aefb9-118">Gran parte de la funcionalidad del modelo de objetos de Windows Media Player 7 o posterior se obtiene acceso a través de la jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="aefb9-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="aefb9-119">Como se mostró en el ejemplo anterior, puede obtener un objeto de **lista de reproducción** con el método **GetAll** del objeto **mediaCollection** , al que se tiene acceso a través del objeto **reproductor** raíz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="aefb9-120">A continuación, puede obtener un objeto **multimedia** determinado del objeto de **lista de reproducción** mediante el método **Item** del objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="aefb9-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="aefb9-121">Hay cinco métodos adicionales accesibles a través del objeto **mediaCollection** que devuelven un objeto de **lista de reproducción** : cada método permite recuperar el objeto basándose en criterios específicos, como el género o el álbum.</span><span class="sxs-lookup"><span data-stu-id="aefb9-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="aefb9-122">La estructura jerárquica del modelo de objetos de control ActiveX de Windows Media Player 7 o posterior proporciona un enfoque más lógico para organizar las propiedades, los métodos y los eventos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="aefb9-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="aefb9-123">Toda la funcionalidad de los controles del reproductor está contenida en el objeto **Controls** , toda la funcionalidad de la conexión de red del reproductor está contenida en el objeto de **red** , etc.</span><span class="sxs-lookup"><span data-stu-id="aefb9-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="aefb9-124">Por ejemplo, para iniciar la reproducción de contenido con el modelo de objetos de la versión 6,4, se usa el método **Player6. Play** :</span><span class="sxs-lookup"><span data-stu-id="aefb9-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="aefb9-125">Al usar el modelo de objetos de Windows Media Player 7 o posterior, debe tener acceso al método **Play** mediante el objeto **Controls** :</span><span class="sxs-lookup"><span data-stu-id="aefb9-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="aefb9-126">La profundidad del modelo de objetos, sin embargo, puede dar lugar a instrucciones de script muy largas:</span><span class="sxs-lookup"><span data-stu-id="aefb9-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="aefb9-127">Las instrucciones como la anterior se pueden hacer mucho más sencillas y legibles si se trabaja con objetos con nombre individuales.</span><span class="sxs-lookup"><span data-stu-id="aefb9-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="aefb9-128">En el ejemplo siguiente se reemplaza la instrucción de código anterior con la sintaxis mediante variables de objeto independientes:</span><span class="sxs-lookup"><span data-stu-id="aefb9-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



<span data-ttu-id="aefb9-129">Este estilo de codificación requiere más líneas de script, pero es mucho más fácil de seguir, especialmente con los comentarios agregados.</span><span class="sxs-lookup"><span data-stu-id="aefb9-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="aefb9-130">Existe otra ventaja: el objeto **currentPlaylist** es fácil de volver a usar porque se almacena en la variable pl.</span><span class="sxs-lookup"><span data-stu-id="aefb9-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="aefb9-131">Muchas de las propiedades, métodos y eventos del modelo de objetos de Windows Media Player 7 o posterior establecen o recuperan valores diferentes, o devuelven valores de un tipo o número diferente, en comparación con la funcionalidad correspondiente en el modelo de objetos de la versión 6,4.</span><span class="sxs-lookup"><span data-stu-id="aefb9-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="aefb9-132">Por ejemplo, cuando **Player6. openState** recupera 2, ese valor corresponde a la constante Visual Basic **nsLoadingNSC**, lo que significa que el reproductor está cargando un archivo de estación con la extensión de nombre de archivo. NSC.</span><span class="sxs-lookup"><span data-stu-id="aefb9-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="aefb9-133">Pero cuando el modelo de objetos de Windows Media Player 7 o posterior **Player. openState** recupera 2, ese valor corresponde al estado PlaylistLocating, lo que significa que Windows Media Player está intentando buscar una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="aefb9-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="aefb9-134">Además, la propiedad **Player6. openState** puede recuperar siete valores diferentes, mientras que la propiedad **Player. openState** de Windows Media Player 7 o posterior puede recuperar 22 valores distintos.</span><span class="sxs-lookup"><span data-stu-id="aefb9-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="aefb9-135">Asegúrese de consultar la sección referencia del modelo de objetos para scripting del SDK de Windows Media Player al revisar el código para usar una versión de modelo de objetos diferente.</span><span class="sxs-lookup"><span data-stu-id="aefb9-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aefb9-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aefb9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aefb9-137">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="aefb9-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="aefb9-138">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="aefb9-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="aefb9-139">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="aefb9-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




