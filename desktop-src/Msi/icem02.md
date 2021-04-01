---
description: ICEM02 comprueba que todas las dependencias del módulo y las exclusiones están relacionadas con el módulo actual.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275760"
---
# <a name="icem02"></a><span data-ttu-id="63d96-103">ICEM02</span><span class="sxs-lookup"><span data-stu-id="63d96-103">ICEM02</span></span>

<span data-ttu-id="63d96-104">ICEM02 comprueba que todas las dependencias del módulo y las exclusiones están relacionadas con el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="63d96-104">ICEM02 verifies that all the module dependencies and exclusions are related to the current module.</span></span>

<span data-ttu-id="63d96-105">El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="63d96-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="63d96-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="63d96-106">Result</span></span>

<span data-ttu-id="63d96-107">ICEM02 envía mensajes de error si la base de datos del módulo intenta especificar dependencias o exclusiones que no se relacionan con el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="63d96-107">ICEM02 posts error messages if the module database attempts to specify dependencies or exclusions that do not relate to the current module.</span></span> <span data-ttu-id="63d96-108">ICEM02 envía un mensaje de error si la base de datos del módulo intenta especificar el módulo actual como dependiente o como excluido por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="63d96-108">ICEM02 posts an error message if the module database attempts to specify the current module as dependent or as excluded by itself.</span></span>

## <a name="example"></a><span data-ttu-id="63d96-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63d96-109">Example</span></span>

<span data-ttu-id="63d96-110">ICEM02 publicaría los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="63d96-110">ICEM02 would post the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[<span data-ttu-id="63d96-111">ModuleSignature (tabla)</span><span class="sxs-lookup"><span data-stu-id="63d96-111">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="63d96-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="63d96-112">ModuleID</span></span>         | <span data-ttu-id="63d96-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="63d96-113">Language</span></span> | <span data-ttu-id="63d96-114">Versión</span><span class="sxs-lookup"><span data-stu-id="63d96-114">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="63d96-115">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="63d96-115">MyModule.*GUID1*</span></span> | <span data-ttu-id="63d96-116">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-116">1033</span></span>     | <span data-ttu-id="63d96-117">1,0</span><span class="sxs-lookup"><span data-stu-id="63d96-117">1.0</span></span>     |



 

[<span data-ttu-id="63d96-118">Tabla ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="63d96-118">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="63d96-119">ModuleID</span><span class="sxs-lookup"><span data-stu-id="63d96-119">ModuleID</span></span>            | <span data-ttu-id="63d96-120">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="63d96-120">ModuleLanguage</span></span> | <span data-ttu-id="63d96-121">RequiredID</span><span class="sxs-lookup"><span data-stu-id="63d96-121">RequiredID</span></span>          | <span data-ttu-id="63d96-122">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="63d96-122">RequiredLanguage</span></span> | <span data-ttu-id="63d96-123">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="63d96-123">RequiredVersion</span></span> |
|---------------------|----------------|---------------------|------------------|-----------------|
| <span data-ttu-id="63d96-124">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="63d96-124">OtherModule.*GUID2*</span></span> | <span data-ttu-id="63d96-125">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-125">1033</span></span>           | <span data-ttu-id="63d96-126">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="63d96-126">OtherModule.*GUID3*</span></span> | <span data-ttu-id="63d96-127">0</span><span class="sxs-lookup"><span data-stu-id="63d96-127">0</span></span>                | <span data-ttu-id="63d96-128">1.0</span><span class="sxs-lookup"><span data-stu-id="63d96-128">1.0</span></span>             |
| <span data-ttu-id="63d96-129">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="63d96-129">MyModule.*GUID1*</span></span>    | <span data-ttu-id="63d96-130">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-130">1033</span></span>           | <span data-ttu-id="63d96-131">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="63d96-131">MyModule.*GUID1*</span></span>    | <span data-ttu-id="63d96-132">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-132">1033</span></span>             | <span data-ttu-id="63d96-133">1.2</span><span class="sxs-lookup"><span data-stu-id="63d96-133">1.2</span></span>             |



 

<span data-ttu-id="63d96-134">[Tabla ModuleExclusion](moduleexclusion-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="63d96-134">[ModuleExclusion Table](moduleexclusion-table.md) (partial)</span></span>



| <span data-ttu-id="63d96-135">ModuleID</span><span class="sxs-lookup"><span data-stu-id="63d96-135">ModuleID</span></span>            | <span data-ttu-id="63d96-136">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="63d96-136">ModuleLanguage</span></span> | <span data-ttu-id="63d96-137">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="63d96-137">ExcludedID</span></span>          | <span data-ttu-id="63d96-138">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="63d96-138">ExcludedLanguage</span></span> |
|---------------------|----------------|---------------------|------------------|
| <span data-ttu-id="63d96-139">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="63d96-139">OtherModule.*GUID2*</span></span> | <span data-ttu-id="63d96-140">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-140">1033</span></span>           | <span data-ttu-id="63d96-141">OtherModule. *GUID3*</span><span class="sxs-lookup"><span data-stu-id="63d96-141">OtherModule.*GUID3*</span></span> | <span data-ttu-id="63d96-142">0</span><span class="sxs-lookup"><span data-stu-id="63d96-142">0</span></span>                |
| <span data-ttu-id="63d96-143">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="63d96-143">MyModule.*GUID1*</span></span>    | <span data-ttu-id="63d96-144">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-144">1033</span></span>           | <span data-ttu-id="63d96-145">MyModule. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="63d96-145">MyModule.*GUID1*</span></span>    | <span data-ttu-id="63d96-146">3082</span><span class="sxs-lookup"><span data-stu-id="63d96-146">1033</span></span>             |



 

<span data-ttu-id="63d96-147">El módulo de combinación ICE envía el primer error porque el de la primera fila de la tabla ModuleDependency, que no especifica una dependencia necesaria para el módulo actual especificado en la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="63d96-147">The merge module ICE posts the first error because the of the first row in the ModuleDependency table, which does not specify a required dependency for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="63d96-148">Las dependencias de un módulo solo se pueden especificar en su propia tabla ModuleDependency.</span><span class="sxs-lookup"><span data-stu-id="63d96-148">The dependencies of a module can only be specified in its own ModuleDependency table.</span></span> <span data-ttu-id="63d96-149">Si OtherModule. El módulo actual requiere *GUID3* , reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="63d96-149">If OtherModule.*GUID3* is required by the current module, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="63d96-150">Si OtherModule. *GUID3* no es necesario para este módulo, elimine esta fila.</span><span class="sxs-lookup"><span data-stu-id="63d96-150">If OtherModule.*GUID3* is not required by this module, delete this row.</span></span>

<span data-ttu-id="63d96-151">El módulo de combinación ICE envía el segundo error porque un módulo no puede especificar una dependencia en sí mismo.</span><span class="sxs-lookup"><span data-stu-id="63d96-151">The merge module ICE posts the second error because a module cannot specify a dependency upon itself.</span></span>

<span data-ttu-id="63d96-152">El módulo de combinación ICE envía el tercer error debido a la primera fila de la tabla ModuleExclusion, que no especifica una exclusión necesaria para el módulo actual especificado en la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="63d96-152">The merge module ICE posts the third error because of the first row in the ModuleExclusion table, which does not specify a required exclusion for the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="63d96-153">Las exclusiones de un módulo solo se pueden especificar en su propia tabla ModuleExclusion.</span><span class="sxs-lookup"><span data-stu-id="63d96-153">The exclusions of a module can only be specified in its own ModuleExclusion table.</span></span> <span data-ttu-id="63d96-154">Si el módulo actual excluye OtherModule. *GUID3*, reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="63d96-154">If the current module excludes OtherModule.*GUID3*, replace the first two columns of the row with the data from the ModuleSignature table.</span></span> <span data-ttu-id="63d96-155">Si el módulo actual no excluye OtherModule. *GUID3*, elimine esta fila.</span><span class="sxs-lookup"><span data-stu-id="63d96-155">If the current module does not exclude OtherModule.*GUID3*, delete this row.</span></span>

<span data-ttu-id="63d96-156">El módulo de combinación ICE envía el cuarto error porque un módulo no puede especificar que se excluya a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="63d96-156">The merge module ICE posts the fourth error because a module cannot specify that it exclude itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63d96-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63d96-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d96-158">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="63d96-158">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



