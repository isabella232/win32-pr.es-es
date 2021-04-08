---
description: ICE25 valida que un archivo. msi satisface todas sus dependencias y exclusiones del módulo de combinación internas.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910913"
---
# <a name="ice25"></a><span data-ttu-id="3f35b-103">ICE25</span><span class="sxs-lookup"><span data-stu-id="3f35b-103">ICE25</span></span>

<span data-ttu-id="3f35b-104">ICE25 valida que un archivo. msi satisface todas sus dependencias y exclusiones del [módulo de combinación](merge-modules.md) internas.</span><span class="sxs-lookup"><span data-stu-id="3f35b-104">ICE25 validates that a .msi file satisfies all of its internal [merge module](merge-modules.md) dependencies and exclusions.</span></span> <span data-ttu-id="3f35b-105">ICE valida lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3f35b-105">ICE validates the following:</span></span>

-   <span data-ttu-id="3f35b-106">Que todas las dependencias del módulo de combinación indicadas en la [tabla ModuleDependency](moduledependency-table.md) del archivo. msi se satisfacen mediante al menos un módulo de combinación enumerado en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f35b-106">That all merge module dependencies indicated in the .msi file's [ModuleDependency table](moduledependency-table.md) are satisfied by at least one merge module listed in the [ModuleSignature table](modulesignature-table.md).</span></span>
-   <span data-ttu-id="3f35b-107">Que ninguno de los módulos de combinación excluidos de la [tabla ModuleExclusion](moduleexclusion-table.md) es incompatible con los módulos de combinación enumerados en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f35b-107">That none of the excluded merge modules in the [ModuleExclusion table](moduleexclusion-table.md) are incompatible with the merge modules listed in the [ModuleSignature table](modulesignature-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="3f35b-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="3f35b-108">Result</span></span>

<span data-ttu-id="3f35b-109">ICE25 envía un mensaje de error si el archivo. msi se ha combinado previamente con un módulo de combinación incompatible o si no se ha combinado con un módulo de combinación necesario.</span><span class="sxs-lookup"><span data-stu-id="3f35b-109">ICE25 posts an error message if .msi file has previously been merged with an incompatible merge module or if it has not been merged with a necessary merge module.</span></span>

## <a name="example"></a><span data-ttu-id="3f35b-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f35b-110">Example</span></span>

<span data-ttu-id="3f35b-111">ICE25 expone los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3f35b-111">ICE25 posts the following errors for the example shown.</span></span>

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[<span data-ttu-id="3f35b-112">ModuleSignature (tabla)</span><span class="sxs-lookup"><span data-stu-id="3f35b-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="3f35b-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3f35b-113">ModuleID</span></span> | <span data-ttu-id="3f35b-114">Idioma</span><span class="sxs-lookup"><span data-stu-id="3f35b-114">Language</span></span> | <span data-ttu-id="3f35b-115">Versión</span><span class="sxs-lookup"><span data-stu-id="3f35b-115">Version</span></span> |
|----------|----------|---------|
| <span data-ttu-id="3f35b-116">Móduloa</span><span class="sxs-lookup"><span data-stu-id="3f35b-116">ModuleA</span></span>  | <span data-ttu-id="3f35b-117">0</span><span class="sxs-lookup"><span data-stu-id="3f35b-117">0</span></span>        | <span data-ttu-id="3f35b-118">1.0</span><span class="sxs-lookup"><span data-stu-id="3f35b-118">1.0</span></span>     |
| <span data-ttu-id="3f35b-119">ModuleB</span><span class="sxs-lookup"><span data-stu-id="3f35b-119">ModuleB</span></span>  | <span data-ttu-id="3f35b-120">3082</span><span class="sxs-lookup"><span data-stu-id="3f35b-120">1033</span></span>     | <span data-ttu-id="3f35b-121">1,0</span><span class="sxs-lookup"><span data-stu-id="3f35b-121">1.0</span></span>     |



 

[<span data-ttu-id="3f35b-122">Tabla ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="3f35b-122">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="3f35b-123">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3f35b-123">ModuleID</span></span> | <span data-ttu-id="3f35b-124">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="3f35b-124">ModuleLanguage</span></span> | <span data-ttu-id="3f35b-125">RequiredID</span><span class="sxs-lookup"><span data-stu-id="3f35b-125">RequiredID</span></span> | <span data-ttu-id="3f35b-126">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="3f35b-126">RequiredLanguage</span></span> | <span data-ttu-id="3f35b-127">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="3f35b-127">RequiredVersion</span></span> |
|----------|----------------|------------|------------------|-----------------|
| <span data-ttu-id="3f35b-128">Móduloa</span><span class="sxs-lookup"><span data-stu-id="3f35b-128">ModuleA</span></span>  | <span data-ttu-id="3f35b-129">0</span><span class="sxs-lookup"><span data-stu-id="3f35b-129">0</span></span>              | <span data-ttu-id="3f35b-130">ModuleX</span><span class="sxs-lookup"><span data-stu-id="3f35b-130">ModuleX</span></span>    | <span data-ttu-id="3f35b-131">0</span><span class="sxs-lookup"><span data-stu-id="3f35b-131">0</span></span>                | <span data-ttu-id="3f35b-132">2.0</span><span class="sxs-lookup"><span data-stu-id="3f35b-132">2.0</span></span>             |



 

[<span data-ttu-id="3f35b-133">Tabla ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="3f35b-133">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="3f35b-134">ModuleID</span><span class="sxs-lookup"><span data-stu-id="3f35b-134">ModuleID</span></span> | <span data-ttu-id="3f35b-135">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="3f35b-135">ModuleLanguage</span></span> | <span data-ttu-id="3f35b-136">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="3f35b-136">ExcludedID</span></span> | <span data-ttu-id="3f35b-137">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="3f35b-137">ExcludedLanguage</span></span> | <span data-ttu-id="3f35b-138">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="3f35b-138">ExcludedMinVersion</span></span> | <span data-ttu-id="3f35b-139">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="3f35b-139">ExcludedMaxVersion</span></span> |
|----------|----------------|------------|------------------|--------------------|--------------------|
| <span data-ttu-id="3f35b-140">Móduloa</span><span class="sxs-lookup"><span data-stu-id="3f35b-140">ModuleA</span></span>  | <span data-ttu-id="3f35b-141">0</span><span class="sxs-lookup"><span data-stu-id="3f35b-141">0</span></span>              | <span data-ttu-id="3f35b-142">ModuleB</span><span class="sxs-lookup"><span data-stu-id="3f35b-142">ModuleB</span></span>    | <span data-ttu-id="3f35b-143">3082</span><span class="sxs-lookup"><span data-stu-id="3f35b-143">1033</span></span>             |                    |                    |



 

## <a name="related-topics"></a><span data-ttu-id="3f35b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f35b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f35b-145">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3f35b-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



