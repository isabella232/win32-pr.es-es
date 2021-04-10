---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player tiendas en línea, genre.csv
- tiendas en línea, genre.csv
- Escriba 1 tiendas en línea, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994438"
---
# <a name="genrecsv"></a><span data-ttu-id="f9c40-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="f9c40-107">genre.csv</span></span>

<span data-ttu-id="f9c40-108">Este archivo contiene una entrada para cada género representado en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="f9c40-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="f9c40-109">Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9c40-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="f9c40-110">Los campos deben aparecer en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="f9c40-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="f9c40-111">Todos los campos de genre.csv son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="f9c40-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="f9c40-112">En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9c40-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="f9c40-113">No hace referencia al tipo de datos del contenido.</span><span class="sxs-lookup"><span data-stu-id="f9c40-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="f9c40-114">Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.</span><span class="sxs-lookup"><span data-stu-id="f9c40-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="f9c40-115">Campo</span><span class="sxs-lookup"><span data-stu-id="f9c40-115">Field</span></span>             | <span data-ttu-id="f9c40-116">Formato</span><span class="sxs-lookup"><span data-stu-id="f9c40-116">Format</span></span>                                                    | <span data-ttu-id="f9c40-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9c40-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c40-118">\_ID. de género</span><span class="sxs-lookup"><span data-stu-id="f9c40-118">Genre\_ID</span></span>         | <span data-ttu-id="f9c40-119">Entero no negativo. Ejemplo: 22</span><span class="sxs-lookup"><span data-stu-id="f9c40-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="f9c40-120">Identificador del género, único en genre.csv.</span><span class="sxs-lookup"><span data-stu-id="f9c40-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="f9c40-121">Debe ser inferior a 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="f9c40-121">Must be less than 2^32.</span></span> <span data-ttu-id="f9c40-122">Es posible un máximo de 64 géneros.</span><span class="sxs-lookup"><span data-stu-id="f9c40-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="f9c40-123">GenreTitle</span><span class="sxs-lookup"><span data-stu-id="f9c40-123">GenreTitle</span></span>        | <span data-ttu-id="f9c40-124">Cadena Unicode. Ejemplo: Rock</span><span class="sxs-lookup"><span data-stu-id="f9c40-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="f9c40-125">Nombre para mostrar del género.</span><span class="sxs-lookup"><span data-stu-id="f9c40-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="f9c40-126">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="f9c40-126">FeedsAreAvailable</span></span> | <span data-ttu-id="f9c40-127">Booleano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="f9c40-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="f9c40-128">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="f9c40-128">Example: 0</span></span><br/> | <span data-ttu-id="f9c40-129">Indica si el comportamiento de reproducción de radio es posible al saltar a una fuente.</span><span class="sxs-lookup"><span data-stu-id="f9c40-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="f9c40-130">HasComposer</span><span class="sxs-lookup"><span data-stu-id="f9c40-130">HasComposer</span></span>       | <span data-ttu-id="f9c40-131">Booleano. formato: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="f9c40-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="f9c40-132">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="f9c40-132">Example: 1</span></span><br/> | <span data-ttu-id="f9c40-133">True si este género debe guardar la información del compositor en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="f9c40-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="f9c40-134">Si no se establece, la información de compositor se omite y no se compila en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="f9c40-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





