---
title: Ubicación y elemento seleccionado
description: Ubicación y elemento seleccionado
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player tiendas en línea, ubicaciones
- tiendas en línea, ubicaciones
- tipo 1 almacenes en línea, ubicaciones
- Windows Media Player tiendas en línea, ubicaciones de biblioteca
- tiendas en línea, ubicaciones de biblioteca
- tipo 1 almacenes en línea, ubicaciones de biblioteca
- Windows Media Player tiendas en línea, elementos seleccionados
- tiendas en línea, elementos seleccionados
- tipo 1 tiendas en línea, elementos seleccionados
- Biblioteca Media Player de Windows, ubicaciones
- Biblioteca de Media Player de Windows, elementos seleccionados
- Biblioteca, ubicaciones
- Biblioteca, elementos seleccionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268688"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="b40da-116">Ubicación y elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-116">Location and Selected Item</span></span>

<span data-ttu-id="b40da-117">Windows Media Player usa los cinco elementos siguientes para caracterizar su vista actual del contenido de la tienda en línea:</span><span class="sxs-lookup"><span data-stu-id="b40da-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="b40da-118">task</span><span class="sxs-lookup"><span data-stu-id="b40da-118">task</span></span>
-   <span data-ttu-id="b40da-119">tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-119">library location type</span></span>
-   <span data-ttu-id="b40da-120">ID. de ubicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-120">library location ID</span></span>
-   <span data-ttu-id="b40da-121">tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-121">selected item type</span></span>
-   <span data-ttu-id="b40da-122">IDENTIFICADOR del elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-122">selected item ID</span></span>

<span data-ttu-id="b40da-123">Normalmente, puede pensar en la vista de Windows Media Player como un contenedor de elementos.</span><span class="sxs-lookup"><span data-stu-id="b40da-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="b40da-124">El contenedor tiene un tipo y un elemento tiene un tipo.</span><span class="sxs-lookup"><span data-stu-id="b40da-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="b40da-125">Todos los elementos de un contenedor tienen el mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="b40da-125">All the items in a container have the same type.</span></span> <span data-ttu-id="b40da-126">Los tipos de ubicación y los tipos de elemento se especifican mediante las [constantes de ubicación](library-location-constants.md)de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b40da-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="b40da-127">Por ejemplo, si la vista actual muestra un álbum individual, el tipo de ubicación de la biblioteca es CPAlbumID y, dado que un álbum contiene pistas, el tipo de elemento seleccionado es CPTrackID.</span><span class="sxs-lookup"><span data-stu-id="b40da-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="b40da-128">En la tabla siguiente se muestran los tipos de ubicación y elemento de varios contenedores.</span><span class="sxs-lookup"><span data-stu-id="b40da-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="b40da-129">Descripción del contenedor</span><span class="sxs-lookup"><span data-stu-id="b40da-129">Description of container</span></span>                              | <span data-ttu-id="b40da-130">Tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-130">Library location type</span></span> | <span data-ttu-id="b40da-131">Tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="b40da-132">Un álbum que es un contenedor de pistas</span><span class="sxs-lookup"><span data-stu-id="b40da-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="b40da-133">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="b40da-133">CPAlbumID</span></span>             | <span data-ttu-id="b40da-134">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="b40da-134">CPTrackID</span></span>          |
| <span data-ttu-id="b40da-135">Una lista que es un contenedor de pistas</span><span class="sxs-lookup"><span data-stu-id="b40da-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="b40da-136">CPListID</span><span class="sxs-lookup"><span data-stu-id="b40da-136">CPListID</span></span>              | <span data-ttu-id="b40da-137">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="b40da-137">CPTrackID</span></span>          |
| <span data-ttu-id="b40da-138">Una lista que es un contenedor de álbumes</span><span class="sxs-lookup"><span data-stu-id="b40da-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="b40da-139">CPListID</span><span class="sxs-lookup"><span data-stu-id="b40da-139">CPListID</span></span>              | <span data-ttu-id="b40da-140">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="b40da-140">CPAlbumID</span></span>          |
| <span data-ttu-id="b40da-141">Una emisora de radio que es un contenedor de listas</span><span class="sxs-lookup"><span data-stu-id="b40da-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="b40da-142">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="b40da-142">CPRadioID</span></span>             | <span data-ttu-id="b40da-143">CPListID</span><span class="sxs-lookup"><span data-stu-id="b40da-143">CPListID</span></span>           |
| <span data-ttu-id="b40da-144">Conjunto de todos los álbumes, que es un contenedor de álbumes.</span><span class="sxs-lookup"><span data-stu-id="b40da-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="b40da-145">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="b40da-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="b40da-146">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="b40da-146">CPAlbumID</span></span>          |
| <span data-ttu-id="b40da-147">Conjunto de todos los géneros, que es un contenedor de géneros</span><span class="sxs-lookup"><span data-stu-id="b40da-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="b40da-148">AllCPGenreIDs</span><span class="sxs-lookup"><span data-stu-id="b40da-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="b40da-149">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="b40da-149">CPGenreID</span></span>          |



 

<span data-ttu-id="b40da-150">Las pestañas de Windows Media Player representan diferentes tareas.</span><span class="sxs-lookup"><span data-stu-id="b40da-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="b40da-151">El reproductor muestra el contenido de la tienda en línea en tres paneles de tareas diferentes: **biblioteca**, **grabación** y **sincronización**. El panel de tareas biblioteca también se denomina panel de tareas **examinar** .</span><span class="sxs-lookup"><span data-stu-id="b40da-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="b40da-152">A veces, un panel de tareas se denomina *característica*, por lo que puede ver términos como característica de *grabación* y *característica de sincronización* en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="b40da-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="b40da-153">En los siguientes ejemplos se muestra cómo Windows Media Player usa las cinco piezas de información (tarea, tipo de ubicación de biblioteca, identificador de ubicación de biblioteca, tipo de elemento seleccionado, ID. de elemento seleccionado) para caracterizar distintas vistas.</span><span class="sxs-lookup"><span data-stu-id="b40da-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="b40da-154">En el panel de tareas **grabar** , el reproductor muestra un álbum como un contenedor de pistas.</span><span class="sxs-lookup"><span data-stu-id="b40da-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="b40da-155">El álbum tiene un identificador de 250.</span><span class="sxs-lookup"><span data-stu-id="b40da-155">The album has an ID of 250.</span></span> <span data-ttu-id="b40da-156">En la vista, el elemento seleccionado es la pista que tiene un identificador de 800.</span><span class="sxs-lookup"><span data-stu-id="b40da-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="b40da-157">Tenga en cuenta que 800 es el identificador de la pista en el catálogo de la tienda en línea, no el número de la pista en el álbum.</span><span class="sxs-lookup"><span data-stu-id="b40da-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="b40da-158">Elemento</span><span class="sxs-lookup"><span data-stu-id="b40da-158">Item</span></span>                  | <span data-ttu-id="b40da-159">Value</span><span class="sxs-lookup"><span data-stu-id="b40da-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="b40da-160">task</span><span class="sxs-lookup"><span data-stu-id="b40da-160">task</span></span>                  | <span data-ttu-id="b40da-161">Burn</span><span class="sxs-lookup"><span data-stu-id="b40da-161">Burn</span></span>      |
| <span data-ttu-id="b40da-162">tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-162">library location type</span></span> | <span data-ttu-id="b40da-163">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="b40da-163">CPAlbumID</span></span> |
| <span data-ttu-id="b40da-164">ID. de ubicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-164">library location ID</span></span>   | <span data-ttu-id="b40da-165">250</span><span class="sxs-lookup"><span data-stu-id="b40da-165">250</span></span>       |
| <span data-ttu-id="b40da-166">tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-166">selected item type</span></span>    | <span data-ttu-id="b40da-167">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="b40da-167">CPTrackID</span></span> |
| <span data-ttu-id="b40da-168">IDENTIFICADOR del elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-168">selected item ID</span></span>      | <span data-ttu-id="b40da-169">800</span><span class="sxs-lookup"><span data-stu-id="b40da-169">800</span></span>       |



 

<span data-ttu-id="b40da-170">En el panel de tareas de **sincronización** , el reproductor muestra el conjunto de todos los álbumes, que es un contenedor de álbumes.</span><span class="sxs-lookup"><span data-stu-id="b40da-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="b40da-171">En la vista, el elemento seleccionado es el álbum que tiene un identificador de 300.</span><span class="sxs-lookup"><span data-stu-id="b40da-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="b40da-172">Tenga en cuenta que el identificador de ubicación de la biblioteca no es aplicable a esta vista.</span><span class="sxs-lookup"><span data-stu-id="b40da-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="b40da-173">Elemento</span><span class="sxs-lookup"><span data-stu-id="b40da-173">Item</span></span>                  | <span data-ttu-id="b40da-174">Value</span><span class="sxs-lookup"><span data-stu-id="b40da-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="b40da-175">task</span><span class="sxs-lookup"><span data-stu-id="b40da-175">task</span></span>                  | <span data-ttu-id="b40da-176">Sync</span><span class="sxs-lookup"><span data-stu-id="b40da-176">Sync</span></span>          |
| <span data-ttu-id="b40da-177">tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-177">library location type</span></span> | <span data-ttu-id="b40da-178">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="b40da-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="b40da-179">ID. de ubicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-179">library location ID</span></span>   | <span data-ttu-id="b40da-180">N/D</span><span class="sxs-lookup"><span data-stu-id="b40da-180">N/A</span></span>           |
| <span data-ttu-id="b40da-181">tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-181">selected item type</span></span>    | <span data-ttu-id="b40da-182">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="b40da-182">CPAlbumID</span></span>     |
| <span data-ttu-id="b40da-183">IDENTIFICADOR del elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-183">selected item ID</span></span>      | <span data-ttu-id="b40da-184">300</span><span class="sxs-lookup"><span data-stu-id="b40da-184">300</span></span>           |



 

<span data-ttu-id="b40da-185">En el control de vista de árbol, se selecciona el nodo raíz de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="b40da-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="b40da-186">En este caso, no hay ningún contenedor y, por consiguiente, no hay elementos.</span><span class="sxs-lookup"><span data-stu-id="b40da-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="b40da-187">El panel de tareas **biblioteca** completa muestra una página de detección.</span><span class="sxs-lookup"><span data-stu-id="b40da-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="b40da-188">Elemento</span><span class="sxs-lookup"><span data-stu-id="b40da-188">Item</span></span>                  | <span data-ttu-id="b40da-189">Value</span><span class="sxs-lookup"><span data-stu-id="b40da-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="b40da-190">task</span><span class="sxs-lookup"><span data-stu-id="b40da-190">task</span></span>                  | <span data-ttu-id="b40da-191">Examinar</span><span class="sxs-lookup"><span data-stu-id="b40da-191">Browse</span></span>          |
| <span data-ttu-id="b40da-192">tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-192">library location type</span></span> | <span data-ttu-id="b40da-193">RootLocation</span><span class="sxs-lookup"><span data-stu-id="b40da-193">RootLocation</span></span>    |
| <span data-ttu-id="b40da-194">ID. de ubicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-194">library location ID</span></span>   | <span data-ttu-id="b40da-195">N/D</span><span class="sxs-lookup"><span data-stu-id="b40da-195">N/A</span></span>             |
| <span data-ttu-id="b40da-196">tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-196">selected item type</span></span>    | <span data-ttu-id="b40da-197">UnknownLocation</span><span class="sxs-lookup"><span data-stu-id="b40da-197">UnknownLocation</span></span> |
| <span data-ttu-id="b40da-198">IDENTIFICADOR del elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-198">selected item ID</span></span>      | <span data-ttu-id="b40da-199">N/D</span><span class="sxs-lookup"><span data-stu-id="b40da-199">N/A</span></span>             |



 

<span data-ttu-id="b40da-200">En el panel de tareas de **sincronización** , el reproductor muestra el año 2002 como un contenedor de pistas.</span><span class="sxs-lookup"><span data-stu-id="b40da-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="b40da-201">En la vista, el elemento seleccionado es la pista que tiene un identificador de 450.</span><span class="sxs-lookup"><span data-stu-id="b40da-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="b40da-202">Elemento</span><span class="sxs-lookup"><span data-stu-id="b40da-202">Item</span></span>                  | <span data-ttu-id="b40da-203">Value</span><span class="sxs-lookup"><span data-stu-id="b40da-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="b40da-204">task</span><span class="sxs-lookup"><span data-stu-id="b40da-204">task</span></span>                  | <span data-ttu-id="b40da-205">Sync</span><span class="sxs-lookup"><span data-stu-id="b40da-205">Sync</span></span>            |
| <span data-ttu-id="b40da-206">tipo de ubicación de la biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-206">library location type</span></span> | <span data-ttu-id="b40da-207">ReleaseDateYear</span><span class="sxs-lookup"><span data-stu-id="b40da-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="b40da-208">ID. de ubicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="b40da-208">library location ID</span></span>   | <span data-ttu-id="b40da-209">2002</span><span class="sxs-lookup"><span data-stu-id="b40da-209">2002</span></span>            |
| <span data-ttu-id="b40da-210">tipo de elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-210">selected item type</span></span>    | <span data-ttu-id="b40da-211">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="b40da-211">CPTrackID</span></span>       |
| <span data-ttu-id="b40da-212">IDENTIFICADOR del elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="b40da-212">selected item ID</span></span>      | <span data-ttu-id="b40da-213">450</span><span class="sxs-lookup"><span data-stu-id="b40da-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="b40da-214">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b40da-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b40da-215">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="b40da-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="b40da-216">**Páginas de detección**</span><span class="sxs-lookup"><span data-stu-id="b40da-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




