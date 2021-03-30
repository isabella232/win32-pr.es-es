---
title: Usar listas de reproducción automáticas para organizar el contenido de la biblioteca
description: Usar listas de reproducción automáticas para organizar el contenido de la biblioteca
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player tiendas en línea, listas de reproducción automáticas
- tiendas en línea, listas de reproducción automáticas
- tipo 1 tiendas en línea, listas de reproducción automáticas
- tipo 2 tiendas en línea, listas de reproducción automáticas
- Windows Media Player tiendas en línea, organizar el contenido de la biblioteca
- tiendas en línea, organizar el contenido de la biblioteca
- Escriba 1 tiendas en línea, organizar el contenido de la biblioteca
- tipo 2 tiendas en línea, organizar el contenido de la biblioteca
- Windows Media Player tiendas en línea, organización de contenido de biblioteca
- tiendas en línea, organización de contenido de biblioteca
- tipo 1 almacenes en línea, organización de contenido de biblioteca
- tipo 2 tiendas en línea, organización de contenido de biblioteca
- Biblioteca, organizar contenido
- organizar el contenido de la biblioteca
- listas de reproducción automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532248"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="db617-118">Usar listas de reproducción automáticas para organizar el contenido de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="db617-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="db617-119">Puede usar listas de reproducción automáticas para organizar el contenido premium que proporcione.</span><span class="sxs-lookup"><span data-stu-id="db617-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="db617-120">Por ejemplo, puede utilizar Windows Media Player para crear una lista de reproducción automática que solo contenga el contenido que proporcionó una clasificación de usuario de al menos cuatro estrellas.</span><span class="sxs-lookup"><span data-stu-id="db617-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="db617-121">A continuación, puede Agregar la lista de reproducción automática a la biblioteca en Windows Media Player para que se muestre en el nodo música comprada en el nodo distribuidor de contenido.</span><span class="sxs-lookup"><span data-stu-id="db617-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="db617-122">Para ello, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="db617-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="db617-123">Cree la lista de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="db617-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="db617-124">Con el explorador de Windows, vaya a la lista de reproducción automática y recupere el archivo. wpl.</span><span class="sxs-lookup"><span data-stu-id="db617-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="db617-125">Con el modelo de objetos de Media Player de Windows, agregue la lista de reproducción automática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="db617-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="db617-126">Establezca el atributo **WM/ContentDistributor** para la lista de reproducción en el nombre de clave del distribuidor de contenido.</span><span class="sxs-lookup"><span data-stu-id="db617-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="db617-127">Establezca el atributo **SyncOnly** para la lista de reproducción en true.</span><span class="sxs-lookup"><span data-stu-id="db617-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="db617-128">En el código de ejemplo de JScript siguiente se muestra una función que agrega una lista de reproducción automática denominada "Favorites Favorites" al nodo de Proseware en la biblioteca:</span><span class="sxs-lookup"><span data-stu-id="db617-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="db617-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db617-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db617-130">Acerca de la integración de bibliotecas</span><span class="sxs-lookup"><span data-stu-id="db617-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="db617-131">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="db617-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="db617-132">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="db617-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="db617-133">**Lista de reproducción. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="db617-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="db617-134">**Listas de reproducción estáticas y automáticas**</span><span class="sxs-lookup"><span data-stu-id="db617-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="db617-135">**Atributo SyncOnly**</span><span class="sxs-lookup"><span data-stu-id="db617-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="db617-136">**Atributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="db617-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="db617-137">**Trabajar con la biblioteca**</span><span class="sxs-lookup"><span data-stu-id="db617-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




