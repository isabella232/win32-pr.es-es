---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player tiendas en línea, artist.csv
- tiendas en línea, artist.csv
- Escriba 1 tiendas en línea, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357710"
---
# <a name="artistcsv"></a><span data-ttu-id="e46d0-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="e46d0-107">artist.csv</span></span>

<span data-ttu-id="e46d0-108">Este archivo contiene una entrada para cada artista en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="e46d0-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="e46d0-109">Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e46d0-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="e46d0-110">Los campos deben aparecer en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="e46d0-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="e46d0-111">Todos los campos de artist.csv son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="e46d0-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="e46d0-112">En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="e46d0-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="e46d0-113">No hace referencia al tipo de datos del contenido.</span><span class="sxs-lookup"><span data-stu-id="e46d0-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="e46d0-114">Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.</span><span class="sxs-lookup"><span data-stu-id="e46d0-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="e46d0-115">Campo</span><span class="sxs-lookup"><span data-stu-id="e46d0-115">Field</span></span>                  | <span data-ttu-id="e46d0-116">Formato</span><span class="sxs-lookup"><span data-stu-id="e46d0-116">Format</span></span>                                            | <span data-ttu-id="e46d0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e46d0-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e46d0-118">ArtistID</span><span class="sxs-lookup"><span data-stu-id="e46d0-118">ArtistID</span></span>               | <span data-ttu-id="e46d0-119">Entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="e46d0-119">Non-negative integer.</span></span> <span data-ttu-id="e46d0-120">Ejemplo: 65832</span><span class="sxs-lookup"><span data-stu-id="e46d0-120">Example: 65832</span></span>              | <span data-ttu-id="e46d0-121">Identificador único para el artista, único en artist.csv.</span><span class="sxs-lookup"><span data-stu-id="e46d0-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="e46d0-122">Debe ser inferior a 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="e46d0-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="e46d0-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="e46d0-123">ArtistName</span></span>             | <span data-ttu-id="e46d0-124">Cadena Unicode. Ejemplo: Don funk</span><span class="sxs-lookup"><span data-stu-id="e46d0-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="e46d0-125">Nombre para mostrar del intérprete.</span><span class="sxs-lookup"><span data-stu-id="e46d0-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="e46d0-126">LinkedGenreID</span><span class="sxs-lookup"><span data-stu-id="e46d0-126">LinkedGenreID</span></span>          | <span data-ttu-id="e46d0-127">Entero no negativo. Ejemplo: 313</span><span class="sxs-lookup"><span data-stu-id="e46d0-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="e46d0-128">GenreID del género principal del artista.</span><span class="sxs-lookup"><span data-stu-id="e46d0-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="e46d0-129">Debe ser un género principal y no un subgénero.</span><span class="sxs-lookup"><span data-stu-id="e46d0-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="e46d0-130">Solo se permite un valor.</span><span class="sxs-lookup"><span data-stu-id="e46d0-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="e46d0-131">LinkedSimilarArtistIDs</span><span class="sxs-lookup"><span data-stu-id="e46d0-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="e46d0-132">N/D</span><span class="sxs-lookup"><span data-stu-id="e46d0-132">N/A</span></span>                                               | <span data-ttu-id="e46d0-133">No se usa en esta versión.</span><span class="sxs-lookup"><span data-stu-id="e46d0-133">Not used in this release.</span></span> <span data-ttu-id="e46d0-134">Debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="e46d0-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="e46d0-135">Popularidad</span><span class="sxs-lookup"><span data-stu-id="e46d0-135">Popularity</span></span>             | <span data-ttu-id="e46d0-136">Puede ser un valor entero o decimal.</span><span class="sxs-lookup"><span data-stu-id="e46d0-136">Can be integer or decimal value.</span></span> <span data-ttu-id="e46d0-137">Ejemplo: 1252,25</span><span class="sxs-lookup"><span data-stu-id="e46d0-137">Example: 1252.25</span></span> | <span data-ttu-id="e46d0-138">Clasificación de popularidad.</span><span class="sxs-lookup"><span data-stu-id="e46d0-138">Popularity ranking.</span></span> <span data-ttu-id="e46d0-139">Puede ser la posición en la lista cuando se ordene por popularidad.</span><span class="sxs-lookup"><span data-stu-id="e46d0-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="e46d0-140">FeedsAvailable</span><span class="sxs-lookup"><span data-stu-id="e46d0-140">FeedsAvailable</span></span>         | <span data-ttu-id="e46d0-141">booleano.</span><span class="sxs-lookup"><span data-stu-id="e46d0-141">Boolean.</span></span> <span data-ttu-id="e46d0-142">Formato: \[ 0 \| 1 \] ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="e46d0-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="e46d0-143">No se usa en esta versión.</span><span class="sxs-lookup"><span data-stu-id="e46d0-143">Not used in this release.</span></span> <span data-ttu-id="e46d0-144">Debe estar vacío.</span><span class="sxs-lookup"><span data-stu-id="e46d0-144">Should be empty.</span></span>                                                                 |



 

 

 





