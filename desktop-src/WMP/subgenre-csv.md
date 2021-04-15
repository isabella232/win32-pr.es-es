---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player tiendas en línea, subgenre.csv
- tiendas en línea, subgenre.csv
- Escriba 1 tiendas en línea, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714220"
---
# <a name="subgenrecsv"></a><span data-ttu-id="44270-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="44270-107">subgenre.csv</span></span>

<span data-ttu-id="44270-108">Este archivo contiene una entrada para cada subgénero representado en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="44270-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="44270-109">Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="44270-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="44270-110">Los campos deben aparecer en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="44270-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="44270-111">En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="44270-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="44270-112">No hace referencia al tipo de datos del contenido.</span><span class="sxs-lookup"><span data-stu-id="44270-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="44270-113">Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.</span><span class="sxs-lookup"><span data-stu-id="44270-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="44270-114">Campo</span><span class="sxs-lookup"><span data-stu-id="44270-114">Field</span></span>             | <span data-ttu-id="44270-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="44270-115">Required</span></span> | <span data-ttu-id="44270-116">Formato</span><span class="sxs-lookup"><span data-stu-id="44270-116">Format</span></span>                                                                                            | <span data-ttu-id="44270-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="44270-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44270-118">SubGenreID</span><span class="sxs-lookup"><span data-stu-id="44270-118">SubGenreID</span></span>        | <span data-ttu-id="44270-119">Sí</span><span class="sxs-lookup"><span data-stu-id="44270-119">Yes</span></span>      | <span data-ttu-id="44270-120">Entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="44270-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="44270-121">Identificador del subgénero (ID.), único dentro de subgenre.csv.</span><span class="sxs-lookup"><span data-stu-id="44270-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="44270-122">Se permiten hasta 1024 subgéneros.</span><span class="sxs-lookup"><span data-stu-id="44270-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="44270-123">SubGenreTitle</span><span class="sxs-lookup"><span data-stu-id="44270-123">SubGenreTitle</span></span>     | <span data-ttu-id="44270-124">Sí</span><span class="sxs-lookup"><span data-stu-id="44270-124">Yes</span></span>      | <span data-ttu-id="44270-125">Cadena Unicode. Ejemplo: música inteligente de baile (IDM)</span><span class="sxs-lookup"><span data-stu-id="44270-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="44270-126">Nombre para mostrar del subgénero.</span><span class="sxs-lookup"><span data-stu-id="44270-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="44270-127">SubGenreSubtitle</span><span class="sxs-lookup"><span data-stu-id="44270-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="44270-128">No</span><span class="sxs-lookup"><span data-stu-id="44270-128">No</span></span>       | <span data-ttu-id="44270-129">Cadena Unicode. Ejemplo: nueva música electrónica de percussive que no es tan pura.</span><span class="sxs-lookup"><span data-stu-id="44270-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="44270-130">Describa el significado del nombre para mostrar del subgénero.</span><span class="sxs-lookup"><span data-stu-id="44270-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="44270-131">Debe ser inferior a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="44270-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="44270-132">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="44270-132">FeedsAreAvailable</span></span> | <span data-ttu-id="44270-133">Sí</span><span class="sxs-lookup"><span data-stu-id="44270-133">Yes</span></span>      | <span data-ttu-id="44270-134">Booleano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="44270-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="44270-135">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="44270-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="44270-136">Indica si la "reproducción de radio" es posible al saltar a una fuente.</span><span class="sxs-lookup"><span data-stu-id="44270-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="44270-137">GenreID vinculado \_</span><span class="sxs-lookup"><span data-stu-id="44270-137">Linked\_GenreID</span></span>   | <span data-ttu-id="44270-138">Sí</span><span class="sxs-lookup"><span data-stu-id="44270-138">Yes</span></span>      | <span data-ttu-id="44270-139">Entero no negativo (GenreID). Ejemplo: 12</span><span class="sxs-lookup"><span data-stu-id="44270-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="44270-140">GenreID del género primario.</span><span class="sxs-lookup"><span data-stu-id="44270-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="44270-141">Solo se permite un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="44270-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="44270-142">SortOrderRank</span><span class="sxs-lookup"><span data-stu-id="44270-142">SortOrderRank</span></span>     | <span data-ttu-id="44270-143">Sí</span><span class="sxs-lookup"><span data-stu-id="44270-143">Yes</span></span>      | <span data-ttu-id="44270-144">Entero no negativo. Ejemplo: 23</span><span class="sxs-lookup"><span data-stu-id="44270-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="44270-145">Una clasificación, idealmente única, que se usa para ordenar los subgéneros en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="44270-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="44270-146">Si el género primario tiene 10 subgéneros, podría ser un entero comprendido entre 1 y 10.</span><span class="sxs-lookup"><span data-stu-id="44270-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





