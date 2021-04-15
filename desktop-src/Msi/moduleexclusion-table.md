---
description: La tabla ModuleExclusion mantiene una lista de otros módulos de combinación que no son compatibles con la misma base de datos del instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabla ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424008"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="7c97a-103">Tabla ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="7c97a-103">ModuleExclusion Table</span></span>

<span data-ttu-id="7c97a-104">La tabla ModuleExclusion mantiene una lista de otros módulos de combinación que no son compatibles con la misma base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="7c97a-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="7c97a-105">Esta tabla permite que una herramienta de combinación o comprobación Compruebe que los módulos de mezcla conflictivos no se combinan en la base de datos del instalador del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c97a-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="7c97a-106">La herramienta comprueba mediante la referencia cruzada de esta tabla con la tabla ModuleSignature en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="7c97a-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="7c97a-107">La tabla ModuleExclusion tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c97a-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="7c97a-108">Columna</span><span class="sxs-lookup"><span data-stu-id="7c97a-108">Column</span></span>             | <span data-ttu-id="7c97a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c97a-109">Type</span></span>                         | <span data-ttu-id="7c97a-110">Clave</span><span class="sxs-lookup"><span data-stu-id="7c97a-110">Key</span></span> | <span data-ttu-id="7c97a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7c97a-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="7c97a-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="7c97a-112">ModuleID</span></span>           | [<span data-ttu-id="7c97a-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="7c97a-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="7c97a-114">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-114">Y</span></span>   | <span data-ttu-id="7c97a-115">N</span><span class="sxs-lookup"><span data-stu-id="7c97a-115">N</span></span>        |
| <span data-ttu-id="7c97a-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="7c97a-116">ModuleLanguage</span></span>     | [<span data-ttu-id="7c97a-117">Entero</span><span class="sxs-lookup"><span data-stu-id="7c97a-117">Integer</span></span>](integer.md)       | <span data-ttu-id="7c97a-118">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-118">Y</span></span>   | <span data-ttu-id="7c97a-119">N</span><span class="sxs-lookup"><span data-stu-id="7c97a-119">N</span></span>        |
| <span data-ttu-id="7c97a-120">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="7c97a-120">ExcludedID</span></span>         | [<span data-ttu-id="7c97a-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="7c97a-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="7c97a-122">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-122">Y</span></span>   | <span data-ttu-id="7c97a-123">N</span><span class="sxs-lookup"><span data-stu-id="7c97a-123">N</span></span>        |
| <span data-ttu-id="7c97a-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="7c97a-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="7c97a-125">Entero</span><span class="sxs-lookup"><span data-stu-id="7c97a-125">Integer</span></span>](integer.md)       | <span data-ttu-id="7c97a-126">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-126">Y</span></span>   | <span data-ttu-id="7c97a-127">N</span><span class="sxs-lookup"><span data-stu-id="7c97a-127">N</span></span>        |
| <span data-ttu-id="7c97a-128">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="7c97a-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="7c97a-129">Versión</span><span class="sxs-lookup"><span data-stu-id="7c97a-129">Version</span></span>](version.md)       |     | <span data-ttu-id="7c97a-130">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-130">Y</span></span>        |
| <span data-ttu-id="7c97a-131">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="7c97a-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="7c97a-132">Versión</span><span class="sxs-lookup"><span data-stu-id="7c97a-132">Version</span></span>](version.md)       |     | <span data-ttu-id="7c97a-133">Y</span><span class="sxs-lookup"><span data-stu-id="7c97a-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7c97a-134">Columnas</span><span class="sxs-lookup"><span data-stu-id="7c97a-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7c97a-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="7c97a-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-136">Identificador del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="7c97a-136">Identifier of the merge module.</span></span> <span data-ttu-id="7c97a-137">Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c97a-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c97a-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="7c97a-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-139">IDENTIFICADOR de idioma decimal del módulo de combinación en ModuleID.</span><span class="sxs-lookup"><span data-stu-id="7c97a-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="7c97a-140">Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c97a-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c97a-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span><span class="sxs-lookup"><span data-stu-id="7c97a-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-142">Identificador de un módulo de combinación excluida.</span><span class="sxs-lookup"><span data-stu-id="7c97a-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="7c97a-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="7c97a-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-144">IDENTIFICADOR de idioma numérico del módulo de combinación de ExcludedID.</span><span class="sxs-lookup"><span data-stu-id="7c97a-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="7c97a-145">La columna ExcludedLanguage puede especificar el identificador de idioma de un solo idioma, por ejemplo, 1033 para Inglés de EE. UU., o especificar el identificador de idioma de un grupo de idiomas, como 9 para cualquier inglés.</span><span class="sxs-lookup"><span data-stu-id="7c97a-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="7c97a-146">La columna ExcludedLanguage puede aceptar identificadores de idioma negativos.</span><span class="sxs-lookup"><span data-stu-id="7c97a-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="7c97a-147">El significado del valor de la columna ExcludedLanguage es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c97a-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="7c97a-148">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="7c97a-148">ExcludedLanguage</span></span> | <span data-ttu-id="7c97a-149">Significado</span><span class="sxs-lookup"><span data-stu-id="7c97a-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="7c97a-150">>0</span><span class="sxs-lookup"><span data-stu-id="7c97a-150">> 0</span></span>           | <span data-ttu-id="7c97a-151">Excluya los identificadores de idioma especificados por ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="7c97a-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="7c97a-152">= 0</span><span class="sxs-lookup"><span data-stu-id="7c97a-152">= 0</span></span>              | <span data-ttu-id="7c97a-153">No excluya ningún ID. de idioma.</span><span class="sxs-lookup"><span data-stu-id="7c97a-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="7c97a-154">< 0</span><span class="sxs-lookup"><span data-stu-id="7c97a-154">< 0</span></span>           | <span data-ttu-id="7c97a-155">Excluya todos los identificadores de idioma excepto los especificados por ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="7c97a-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7c97a-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="7c97a-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-157">Versión mínima excluida de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="7c97a-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="7c97a-158">Si el campo ExcludedMinVersion es null, se excluyen todas las versiones anteriores a ExcludedMaxVersion.</span><span class="sxs-lookup"><span data-stu-id="7c97a-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="7c97a-159">Si ExcludedMinVersion y ExcludedMaxVersion son NULL, no hay ninguna exclusión basada en la versión.</span><span class="sxs-lookup"><span data-stu-id="7c97a-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="7c97a-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="7c97a-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="7c97a-161">Versión máxima excluida de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="7c97a-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="7c97a-162">Si el campo ExcludedMaxVersion es null, se excluyen todas las versiones posteriores a ExcludedMinVersion.</span><span class="sxs-lookup"><span data-stu-id="7c97a-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="7c97a-163">Si ExcludedMinVersion y ExcludedMaxVersion son NULL, no hay ninguna exclusión basada en la versión.</span><span class="sxs-lookup"><span data-stu-id="7c97a-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="7c97a-164">Validación</span><span class="sxs-lookup"><span data-stu-id="7c97a-164">Validation</span></span>

<dl>

[<span data-ttu-id="7c97a-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="7c97a-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7c97a-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="7c97a-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7c97a-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="7c97a-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



