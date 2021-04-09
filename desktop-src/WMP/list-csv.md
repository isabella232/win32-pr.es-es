---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player tiendas en línea, list.csv
- tiendas en línea, list.csv
- Escriba 1 tiendas en línea, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149072"
---
# <a name="listcsv"></a><span data-ttu-id="d1617-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="d1617-107">list.csv</span></span>

<span data-ttu-id="d1617-108">Este archivo contiene una entrada para cada una de las listas que contiene el catálogo.</span><span class="sxs-lookup"><span data-stu-id="d1617-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="d1617-109">Las listas pueden ser listas de pistas, álbumes, intérpretes, géneros, subgéneros o fuentes de radio. o bien, pueden ser listas de otras listas.</span><span class="sxs-lookup"><span data-stu-id="d1617-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="d1617-110">Cada entrada de la lista es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1617-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="d1617-111">Los campos deben aparecer en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="d1617-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="d1617-112">En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1617-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="d1617-113">No hace referencia al tipo de datos del contenido.</span><span class="sxs-lookup"><span data-stu-id="d1617-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="d1617-114">Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.</span><span class="sxs-lookup"><span data-stu-id="d1617-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1617-115">Campo</span><span class="sxs-lookup"><span data-stu-id="d1617-115">Field</span></span></th>
<th><span data-ttu-id="d1617-116">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1617-116">Required</span></span></th>
<th><span data-ttu-id="d1617-117">Formato</span><span class="sxs-lookup"><span data-stu-id="d1617-117">Format</span></span></th>
<th><span data-ttu-id="d1617-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1617-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1617-119">ListID</span><span class="sxs-lookup"><span data-stu-id="d1617-119">ListID</span></span></td>
<td><span data-ttu-id="d1617-120">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-120">Yes</span></span></td>
<td><span data-ttu-id="d1617-121">Entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="d1617-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="d1617-122">Identificador de lista, único en list.csv.</span><span class="sxs-lookup"><span data-stu-id="d1617-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="d1617-123">No debe ser negativo y menor que 2 ^ 32. <strong>Mostrar un nodo de lista en el control de vista de árbol:</strong> Si ListID es 0, 1, 2, 3, 4, 5, 6 o 7, la lista aparecerá como un nodo personalizado en el nodo de nivel superior de la tienda en línea en el control de vista de árbol del reproductor.</span><span class="sxs-lookup"><span data-stu-id="d1617-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="d1617-124">Los nodos personalizados aparecen antes que los nodos estándar en el nodo de nivel superior de la tienda en línea y se colocan en orden ascendente por ListID.</span><span class="sxs-lookup"><span data-stu-id="d1617-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="d1617-125">Por ejemplo, si hay tres nodos personalizados, con Listid de 1, 3 y 5, se mostrarán primero, segundo y tercero en el nodo de nivel superior de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="d1617-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-126">ListTitle</span><span class="sxs-lookup"><span data-stu-id="d1617-126">ListTitle</span></span></td>
<td><span data-ttu-id="d1617-127">No</span><span class="sxs-lookup"><span data-stu-id="d1617-127">No</span></span></td>
<td><span data-ttu-id="d1617-128">Cadena Unicode. Ejemplo: diez golpes principales</span><span class="sxs-lookup"><span data-stu-id="d1617-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="d1617-129">Título de la lista.</span><span class="sxs-lookup"><span data-stu-id="d1617-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-130">ListSubtitle</span><span class="sxs-lookup"><span data-stu-id="d1617-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="d1617-131">No</span><span class="sxs-lookup"><span data-stu-id="d1617-131">No</span></span></td>
<td><span data-ttu-id="d1617-132">Cadena de Unicode</span><span class="sxs-lookup"><span data-stu-id="d1617-132">Unicode string</span></span></td>
<td><span data-ttu-id="d1617-133">Mostrar el título alternativo, que se muestra en la segunda línea de la vista de mosaico.</span><span class="sxs-lookup"><span data-stu-id="d1617-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-134">ListDescription</span><span class="sxs-lookup"><span data-stu-id="d1617-134">ListDescription</span></span></td>
<td><span data-ttu-id="d1617-135">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-135">Yes</span></span></td>
<td><span data-ttu-id="d1617-136">Cadena de Unicode</span><span class="sxs-lookup"><span data-stu-id="d1617-136">Unicode string</span></span></td>
<td><span data-ttu-id="d1617-137">Muestra el texto para mostrar descriptivo (mostrado en páginas de propiedades).</span><span class="sxs-lookup"><span data-stu-id="d1617-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="d1617-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="d1617-139">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-139">Yes</span></span></td>
<td><span data-ttu-id="d1617-140">Cadena Unicode. Formato: [T | P | Un | L | G | S | C</span><span class="sxs-lookup"><span data-stu-id="d1617-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="d1617-141">Ejemplo: T</span><span class="sxs-lookup"><span data-stu-id="d1617-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="d1617-142">Indica el tipo de los elementos vinculados.</span><span class="sxs-lookup"><span data-stu-id="d1617-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="d1617-143">T = pista</span><span class="sxs-lookup"><span data-stu-id="d1617-143">T= Track</span></span></li>
<li><span data-ttu-id="d1617-144">P = rendimiento</span><span class="sxs-lookup"><span data-stu-id="d1617-144">P = Performer</span></span></li>
<li><span data-ttu-id="d1617-145">A = álbum</span><span class="sxs-lookup"><span data-stu-id="d1617-145">A = Album</span></span></li>
<li><span data-ttu-id="d1617-146">L = lista</span><span class="sxs-lookup"><span data-stu-id="d1617-146">L = List</span></span></li>
<li><span data-ttu-id="d1617-147">G = Género</span><span class="sxs-lookup"><span data-stu-id="d1617-147">G = Genre</span></span></li>
<li><span data-ttu-id="d1617-148">S = subgénero</span><span class="sxs-lookup"><span data-stu-id="d1617-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="d1617-149">R = radio</span><span class="sxs-lookup"><span data-stu-id="d1617-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="d1617-150">ListPrice</span></span></td>
<td><span data-ttu-id="d1617-151">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-151">Yes</span></span></td>
<td><span data-ttu-id="d1617-152">Cadena Unicode. Ejemplo: $9,99</span><span class="sxs-lookup"><span data-stu-id="d1617-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="d1617-153">Precio de la lista.</span><span class="sxs-lookup"><span data-stu-id="d1617-153">Price of the list.</span></span> <span data-ttu-id="d1617-154">Se debe incluir el símbolo de moneda. Un cero significa que la lista es gratuita.</span><span class="sxs-lookup"><span data-stu-id="d1617-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="d1617-155">Ningún valor significa que se desconoce el precio.</span><span class="sxs-lookup"><span data-stu-id="d1617-155">No value means the price is unknown.</span></span> <span data-ttu-id="d1617-156">Un guion significa que la lista no se puede comprar.</span><span class="sxs-lookup"><span data-stu-id="d1617-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-157">Popularidad</span><span class="sxs-lookup"><span data-stu-id="d1617-157">Popularity</span></span></td>
<td><span data-ttu-id="d1617-158">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-158">Yes</span></span></td>
<td><span data-ttu-id="d1617-159">Valor entero o decimal. Ejemplo: 1259,3</span><span class="sxs-lookup"><span data-stu-id="d1617-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="d1617-160">Indica la categoría de popularidad cuando esta lista aparece en otras listas.</span><span class="sxs-lookup"><span data-stu-id="d1617-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="d1617-161">Puede ser cero si no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="d1617-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-162">IsRecentlyAdded</span><span class="sxs-lookup"><span data-stu-id="d1617-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="d1617-163">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-163">Yes</span></span></td>
<td><span data-ttu-id="d1617-164">Booleano. formato: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="d1617-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="d1617-165">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d1617-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="d1617-166">Indica si la lista se ha agregado recientemente.</span><span class="sxs-lookup"><span data-stu-id="d1617-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-167">IsFeatured</span><span class="sxs-lookup"><span data-stu-id="d1617-167">IsFeatured</span></span></td>
<td><span data-ttu-id="d1617-168">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-168">Yes</span></span></td>
<td><span data-ttu-id="d1617-169">Booleano. formato: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="d1617-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="d1617-170">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d1617-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="d1617-171">Indica si la lista está destacada.</span><span class="sxs-lookup"><span data-stu-id="d1617-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="d1617-172">Se puede usar para determinar el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="d1617-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-173">EditorialGlyph</span><span class="sxs-lookup"><span data-stu-id="d1617-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="d1617-174">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-174">Yes</span></span></td>
<td><span data-ttu-id="d1617-175">Entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="d1617-175">Non-negative integer.</span></span> <span data-ttu-id="d1617-176">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="d1617-176">Should be 0.</span></span></td>
<td><span data-ttu-id="d1617-177">No se usa en esta versión.</span><span class="sxs-lookup"><span data-stu-id="d1617-177">Not used in this release.</span></span> <span data-ttu-id="d1617-178">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="d1617-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="d1617-179">ViewType</span></span></td>
<td><span data-ttu-id="d1617-180">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-180">Yes</span></span></td>
<td><span data-ttu-id="d1617-181">Cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1617-181">Unicode string.</span></span> <span data-ttu-id="d1617-182">Formato: [I | T | R | L | O] ejemplo: T</span><span class="sxs-lookup"><span data-stu-id="d1617-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="d1617-183">Indica el tipo de vista que se va a utilizar para la lista.</span><span class="sxs-lookup"><span data-stu-id="d1617-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="d1617-184">I = icono</span><span class="sxs-lookup"><span data-stu-id="d1617-184">I = Icon</span></span></li>
<li><span data-ttu-id="d1617-185">T = icono</span><span class="sxs-lookup"><span data-stu-id="d1617-185">T = Tile</span></span></li>
<li><span data-ttu-id="d1617-186">R = informe</span><span class="sxs-lookup"><span data-stu-id="d1617-186">R = Report</span></span></li>
<li><span data-ttu-id="d1617-187">L = lista</span><span class="sxs-lookup"><span data-stu-id="d1617-187">L = List</span></span></li>
<li><span data-ttu-id="d1617-188">O = Lista ordenada</span><span class="sxs-lookup"><span data-stu-id="d1617-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-189">ViewImageSize</span><span class="sxs-lookup"><span data-stu-id="d1617-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="d1617-190">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-190">Yes</span></span></td>
<td><span data-ttu-id="d1617-191">Entero no negativo. Ejemplo: 180</span><span class="sxs-lookup"><span data-stu-id="d1617-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="d1617-192">Tamaño en el que se muestra la imagen de la lista.</span><span class="sxs-lookup"><span data-stu-id="d1617-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="d1617-193">Si es 0, el tamaño se determina automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d1617-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1617-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="d1617-194">GroupBy</span></span></td>
<td><span data-ttu-id="d1617-195">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-195">Yes</span></span></td>
<td><span data-ttu-id="d1617-196">Cadena Unicode. Formato: [-| P | Un | C | R | D</span><span class="sxs-lookup"><span data-stu-id="d1617-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="d1617-197">Ejemplo: P</span><span class="sxs-lookup"><span data-stu-id="d1617-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="d1617-198">Indica el campo que se utiliza para agrupar los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="d1617-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="d1617-199">- = Automático</span><span class="sxs-lookup"><span data-stu-id="d1617-199">- = Automatic</span></span></li>
<li><span data-ttu-id="d1617-200">P = rendimiento</span><span class="sxs-lookup"><span data-stu-id="d1617-200">P = Performer</span></span></li>
<li><span data-ttu-id="d1617-201">A = álbum</span><span class="sxs-lookup"><span data-stu-id="d1617-201">A = Album</span></span></li>
<li><span data-ttu-id="d1617-202">C = compositor</span><span class="sxs-lookup"><span data-stu-id="d1617-202">C = Composer</span></span></li>
<li><span data-ttu-id="d1617-203">R = clasificación</span><span class="sxs-lookup"><span data-stu-id="d1617-203">R = Rating</span></span></li>
<li><span data-ttu-id="d1617-204">D = fecha</span><span class="sxs-lookup"><span data-stu-id="d1617-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1617-205">ListItemsAreDynamic</span><span class="sxs-lookup"><span data-stu-id="d1617-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="d1617-206">Sí</span><span class="sxs-lookup"><span data-stu-id="d1617-206">Yes</span></span></td>
<td><span data-ttu-id="d1617-207">booleano.</span><span class="sxs-lookup"><span data-stu-id="d1617-207">Boolean.</span></span> <span data-ttu-id="d1617-208">Puede ser 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="d1617-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="d1617-209">Indica si la lista se genera dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="d1617-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="d1617-210">Las listas dinámicas no tienen elementos en listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="d1617-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="d1617-211">Si una lista está marcada como dinámica, <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a> proporciona los elementos.</span><span class="sxs-lookup"><span data-stu-id="d1617-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





