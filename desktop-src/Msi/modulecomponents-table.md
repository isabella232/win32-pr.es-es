---
description: La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabla ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652959"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="ec793-103">Tabla ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="ec793-103">ModuleComponents Table</span></span>

<span data-ttu-id="ec793-104">La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="ec793-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="ec793-105">La tabla ModuleComponents tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ec793-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="ec793-106">Columna</span><span class="sxs-lookup"><span data-stu-id="ec793-106">Column</span></span>    | <span data-ttu-id="ec793-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec793-107">Type</span></span>                         | <span data-ttu-id="ec793-108">Clave</span><span class="sxs-lookup"><span data-stu-id="ec793-108">Key</span></span> | <span data-ttu-id="ec793-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ec793-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ec793-110">Componente</span><span class="sxs-lookup"><span data-stu-id="ec793-110">Component</span></span> | [<span data-ttu-id="ec793-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="ec793-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ec793-112">Y</span><span class="sxs-lookup"><span data-stu-id="ec793-112">Y</span></span>   | <span data-ttu-id="ec793-113">N</span><span class="sxs-lookup"><span data-stu-id="ec793-113">N</span></span>        |
| <span data-ttu-id="ec793-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="ec793-114">ModuleID</span></span>  | [<span data-ttu-id="ec793-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="ec793-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ec793-116">Y</span><span class="sxs-lookup"><span data-stu-id="ec793-116">Y</span></span>   | <span data-ttu-id="ec793-117">N</span><span class="sxs-lookup"><span data-stu-id="ec793-117">N</span></span>        |
| <span data-ttu-id="ec793-118">Idioma</span><span class="sxs-lookup"><span data-stu-id="ec793-118">Language</span></span>  | [<span data-ttu-id="ec793-119">Entero</span><span class="sxs-lookup"><span data-stu-id="ec793-119">Integer</span></span>](integer.md)       | <span data-ttu-id="ec793-120">Y</span><span class="sxs-lookup"><span data-stu-id="ec793-120">Y</span></span>   | <span data-ttu-id="ec793-121">N</span><span class="sxs-lookup"><span data-stu-id="ec793-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ec793-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="ec793-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ec793-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Pone</span><span class="sxs-lookup"><span data-stu-id="ec793-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="ec793-124">Identificador que hace referencia a un componente en el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="ec793-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="ec793-125">La columna componente es una clave externa de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec793-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="ec793-126">La entrada de la columna componente debe seguir la Convención de nomenclatura de [asignar nombres a las claves principales de las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="ec793-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec793-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="ec793-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="ec793-128">Identificador del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="ec793-128">The identifier for the merge module.</span></span> <span data-ttu-id="ec793-129">Se trata de una clave externa de la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec793-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec793-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo</span><span class="sxs-lookup"><span data-stu-id="ec793-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="ec793-131">El identificador de idioma describe el idioma predeterminado del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="ec793-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="ec793-132">El identificador de idioma está en formato decimal; por ejemplo, Inglés de EE. UU. es 1033.</span><span class="sxs-lookup"><span data-stu-id="ec793-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="ec793-133">Clave externa para la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec793-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec793-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec793-134">Remarks</span></span>

<span data-ttu-id="ec793-135">Las transformaciones del lenguaje deben ser capaces de actualizar esta tabla si el módulo de combinación admite varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="ec793-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



