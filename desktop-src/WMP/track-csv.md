---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player tiendas en línea, track.csv
- tiendas en línea, track.csv
- Escriba 1 tiendas en línea, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357268"
---
# <a name="trackcsv"></a><span data-ttu-id="1f8ed-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="1f8ed-107">track.csv</span></span>

<span data-ttu-id="1f8ed-108">Este archivo contiene una entrada para cada pista en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="1f8ed-109">Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="1f8ed-110">Los campos deben aparecer en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="1f8ed-111">En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="1f8ed-112">No hace referencia al tipo de datos del contenido.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="1f8ed-113">Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8ed-114">Campo</span><span class="sxs-lookup"><span data-stu-id="1f8ed-114">Field</span></span></th>
<th><span data-ttu-id="1f8ed-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1f8ed-115">Required</span></span></th>
<th><span data-ttu-id="1f8ed-116">Formato</span><span class="sxs-lookup"><span data-stu-id="1f8ed-116">Format</span></span></th>
<th><span data-ttu-id="1f8ed-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f8ed-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8ed-118">Elemento TrackID</span><span class="sxs-lookup"><span data-stu-id="1f8ed-118">TrackID</span></span></td>
<td><span data-ttu-id="1f8ed-119">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-119">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-120">Entero no negativo. Ejemplo: 32789</span><span class="sxs-lookup"><span data-stu-id="1f8ed-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="1f8ed-121">Identificador único proporcionado por el proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="1f8ed-122">Debe ser inferior a 2 ^ 32. sugerencia de rendimiento: si se numeran consecutivamente los identificadores asignados a las pistas del mismo álbum, la compresión del catálogo será más eficaz.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="1f8ed-123">Sin embargo, no se requiere la numeración consecutiva de las pistas de álbum.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-124">TrackTitle</span><span class="sxs-lookup"><span data-stu-id="1f8ed-124">TrackTitle</span></span></td>
<td><span data-ttu-id="1f8ed-125">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-125">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-126">Cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-126">Unicode string.</span></span> <span data-ttu-id="1f8ed-127">Ejemplo: Raygun le Robbers ' Blues '</span><span class="sxs-lookup"><span data-stu-id="1f8ed-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="1f8ed-128">Nombre de la pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-129">Duration</span><span class="sxs-lookup"><span data-stu-id="1f8ed-129">Duration</span></span></td>
<td><span data-ttu-id="1f8ed-130">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-130">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-131">Entero no negativo. Ejemplo: 543</span><span class="sxs-lookup"><span data-stu-id="1f8ed-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="1f8ed-132">Duración de la pista en segundos.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-133">TrackNumber</span><span class="sxs-lookup"><span data-stu-id="1f8ed-133">TrackNumber</span></span></td>
<td><span data-ttu-id="1f8ed-134">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-134">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-135">Entero no negativo. Ejemplo: 7</span><span class="sxs-lookup"><span data-stu-id="1f8ed-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="1f8ed-136">Número de pista en el álbum de la pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-136">Track number on the track's album.</span></span> <span data-ttu-id="1f8ed-137">Los números de seguimiento comienzan en 1 y aumentan entre conjuntos de discos.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="1f8ed-138">El número de pista debe ser inferior a 256.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-138">The track number must be less than 256.</span></span> <span data-ttu-id="1f8ed-139">Un número de pista mayor o igual que 256 producirá un comportamiento inesperado en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-140">TrackPrice</span><span class="sxs-lookup"><span data-stu-id="1f8ed-140">TrackPrice</span></span></td>
<td><span data-ttu-id="1f8ed-141">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-141">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-142">Cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-142">Unicode string.</span></span> <span data-ttu-id="1f8ed-143">Ejemplo: $0,99.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="1f8ed-144">Precio de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-144">Track price.</span></span> <span data-ttu-id="1f8ed-145">Se debe incluir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-145">The currency symbol should be included.</span></span> <span data-ttu-id="1f8ed-146">La cadena vacía, 0 y, tienen un significado especial.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="1f8ed-147">Una cadena vacía indica que se desconoce el precio.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="1f8ed-148">Un cero en este campo significa que la pista es gratuita y un guión (-) indica que no se puede comprar la pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-149">CanStream</span><span class="sxs-lookup"><span data-stu-id="1f8ed-149">CanStream</span></span></td>
<td><span data-ttu-id="1f8ed-150">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-150">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-151">booleano.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-151">Boolean.</span></span> <span data-ttu-id="1f8ed-152">Puede ser 0 o 1. ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1f8ed-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="1f8ed-153">Indica si se puede transmitir por secuencias la pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-154">CanDownload</span><span class="sxs-lookup"><span data-stu-id="1f8ed-154">CanDownload</span></span></td>
<td><span data-ttu-id="1f8ed-155">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-155">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-156">booleano.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-156">Boolean.</span></span> <span data-ttu-id="1f8ed-157">Puede ser 0 o 1. ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1f8ed-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="1f8ed-158">Indica si se puede descargar la pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-159">HasPreviewClip</span><span class="sxs-lookup"><span data-stu-id="1f8ed-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="1f8ed-160">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-160">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-161">booleano.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-161">Boolean.</span></span> <span data-ttu-id="1f8ed-162">Puede ser 0 o 1. ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1f8ed-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="1f8ed-163">Indica si la pista tiene un clip de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-164">HasVideoClip</span><span class="sxs-lookup"><span data-stu-id="1f8ed-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="1f8ed-165">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-165">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-166">booleano.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-166">Boolean.</span></span> <span data-ttu-id="1f8ed-167">Puede ser 0 o 1. ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1f8ed-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="1f8ed-168">Indica si la pista tiene un clip de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-169">ParentalRating</span><span class="sxs-lookup"><span data-stu-id="1f8ed-169">ParentalRating</span></span></td>
<td><span data-ttu-id="1f8ed-170">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-170">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-171">Enumeración.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-171">Enumeration.</span></span> <span data-ttu-id="1f8ed-172">Puede ser N, E o C. ejemplo: N</span><span class="sxs-lookup"><span data-stu-id="1f8ed-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="1f8ed-173">Indica la clasificación del Asesor parental.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="1f8ed-174">Los valores N, E y C tienen como valor normal, Explicit y Clean.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-175">LinkedAlbumID</span><span class="sxs-lookup"><span data-stu-id="1f8ed-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="1f8ed-176">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-176">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-177">Entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-177">Non-negative integer.</span></span> <span data-ttu-id="1f8ed-178">Debe ser el identificador de un álbum.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-178">Must be the ID of an Album.</span></span> <span data-ttu-id="1f8ed-179">Ejemplo: 32423</span><span class="sxs-lookup"><span data-stu-id="1f8ed-179">Example: 32423</span></span></td>
<td><span data-ttu-id="1f8ed-180">IDENTIFICADOR del álbum que contiene esta pista.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f8ed-181">Cada pista debe pertenecer a un álbum.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-181">Every track must belong to an album.</span></span> <span data-ttu-id="1f8ed-182">Es decir, para cada pista, el campo LinkedAlbumID debe ser igual a uno de los identificadores de álbum del archivo album.csv.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="1f8ed-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="1f8ed-184">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-184">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-185">Lista de enteros.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-185">List of integers.</span></span> <span data-ttu-id="1f8ed-186">La lista contiene los identificadores de intérprete, separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="1f8ed-187">Ejemplo: 41322; 12321; 82123;</span><span class="sxs-lookup"><span data-stu-id="1f8ed-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="1f8ed-188">Una lista de identificadores que corresponden a los artistas contribuyentes.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-189">Composer</span><span class="sxs-lookup"><span data-stu-id="1f8ed-189">Composer</span></span></td>
<td><span data-ttu-id="1f8ed-190">No</span><span class="sxs-lookup"><span data-stu-id="1f8ed-190">No</span></span></td>
<td><span data-ttu-id="1f8ed-191">Cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-191">Unicode string.</span></span> <span data-ttu-id="1f8ed-192">Ejemplo: Beethoven</span><span class="sxs-lookup"><span data-stu-id="1f8ed-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="1f8ed-193">Compositor de la pista. Si el género de la pista no tiene establecido el campo HasComposer, se omitirá el valor del campo compositor.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="1f8ed-194">Normalmente solo se usa para pistas jazz o clásicas.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8ed-195">Popularidad</span><span class="sxs-lookup"><span data-stu-id="1f8ed-195">Popularity</span></span></td>
<td><span data-ttu-id="1f8ed-196">Sí</span><span class="sxs-lookup"><span data-stu-id="1f8ed-196">Yes</span></span></td>
<td><span data-ttu-id="1f8ed-197">Entero no negativo o float. ejemplo: 1252,6</span><span class="sxs-lookup"><span data-stu-id="1f8ed-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="1f8ed-198">Determina la posición de la pista en la lista cuando se ordena por popularidad.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="1f8ed-199">Un número menor indica una mayor popularidad.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8ed-200">StarRating</span><span class="sxs-lookup"><span data-stu-id="1f8ed-200">StarRating</span></span></td>
<td><span data-ttu-id="1f8ed-201">No</span><span class="sxs-lookup"><span data-stu-id="1f8ed-201">No</span></span></td>
<td><span data-ttu-id="1f8ed-202">Float. ejemplo: 4,21</span><span class="sxs-lookup"><span data-stu-id="1f8ed-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="1f8ed-203">La clasificación por estrellas se redondeará al 1/4 de Media Player Windows más cercano antes de mostrarse en la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1f8ed-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





