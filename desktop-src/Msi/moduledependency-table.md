---
description: La tabla ModuleDependency mantiene una lista de otros módulos de combinación que son necesarios para que este módulo de combinación funcione correctamente.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabla ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678033"
---
# <a name="moduledependency-table"></a><span data-ttu-id="1659d-103">Tabla ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="1659d-103">ModuleDependency Table</span></span>

<span data-ttu-id="1659d-104">La tabla ModuleDependency mantiene una lista de otros módulos de combinación que son necesarios para que este módulo de combinación funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="1659d-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="1659d-105">Esta tabla habilita una herramienta de combinación o comprobación para asegurarse de que los módulos de combinación necesarios se incluyen en realidad en la base de datos del instalador del usuario.</span><span class="sxs-lookup"><span data-stu-id="1659d-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="1659d-106">La herramienta comprueba mediante una referencia cruzada a esta tabla con la tabla ModuleSignature en la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="1659d-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="1659d-107">La tabla ModuleDependency tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1659d-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="1659d-108">Columna</span><span class="sxs-lookup"><span data-stu-id="1659d-108">Column</span></span>           | <span data-ttu-id="1659d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1659d-109">Type</span></span>                         | <span data-ttu-id="1659d-110">Clave</span><span class="sxs-lookup"><span data-stu-id="1659d-110">Key</span></span> | <span data-ttu-id="1659d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="1659d-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="1659d-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="1659d-112">ModuleID</span></span>         | [<span data-ttu-id="1659d-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="1659d-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="1659d-114">Y</span><span class="sxs-lookup"><span data-stu-id="1659d-114">Y</span></span>   | <span data-ttu-id="1659d-115">N</span><span class="sxs-lookup"><span data-stu-id="1659d-115">N</span></span>        |
| <span data-ttu-id="1659d-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="1659d-116">ModuleLanguage</span></span>   | [<span data-ttu-id="1659d-117">Entero</span><span class="sxs-lookup"><span data-stu-id="1659d-117">Integer</span></span>](integer.md)       | <span data-ttu-id="1659d-118">Y</span><span class="sxs-lookup"><span data-stu-id="1659d-118">Y</span></span>   | <span data-ttu-id="1659d-119">N</span><span class="sxs-lookup"><span data-stu-id="1659d-119">N</span></span>        |
| <span data-ttu-id="1659d-120">RequiredID</span><span class="sxs-lookup"><span data-stu-id="1659d-120">RequiredID</span></span>       | [<span data-ttu-id="1659d-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="1659d-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="1659d-122">Y</span><span class="sxs-lookup"><span data-stu-id="1659d-122">Y</span></span>   | <span data-ttu-id="1659d-123">N</span><span class="sxs-lookup"><span data-stu-id="1659d-123">N</span></span>        |
| <span data-ttu-id="1659d-124">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="1659d-124">RequiredLanguage</span></span> | [<span data-ttu-id="1659d-125">Entero</span><span class="sxs-lookup"><span data-stu-id="1659d-125">Integer</span></span>](integer.md)       | <span data-ttu-id="1659d-126">Y</span><span class="sxs-lookup"><span data-stu-id="1659d-126">Y</span></span>   | <span data-ttu-id="1659d-127">N</span><span class="sxs-lookup"><span data-stu-id="1659d-127">N</span></span>        |
| <span data-ttu-id="1659d-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="1659d-128">RequiredVersion</span></span>  | [<span data-ttu-id="1659d-129">Versión</span><span class="sxs-lookup"><span data-stu-id="1659d-129">Version</span></span>](version.md)       |     | <span data-ttu-id="1659d-130">Y</span><span class="sxs-lookup"><span data-stu-id="1659d-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1659d-131">Columnas</span><span class="sxs-lookup"><span data-stu-id="1659d-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1659d-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="1659d-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="1659d-133">Identificador del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="1659d-133">Identifier of the merge module.</span></span> <span data-ttu-id="1659d-134">Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1659d-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1659d-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="1659d-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="1659d-136">IDENTIFICADOR de idioma decimal del módulo de combinación en ModuleID.</span><span class="sxs-lookup"><span data-stu-id="1659d-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="1659d-137">Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="1659d-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="1659d-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span><span class="sxs-lookup"><span data-stu-id="1659d-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="1659d-139">Identificador del módulo de combinación requerido por el módulo de combinación en ModuleID.</span><span class="sxs-lookup"><span data-stu-id="1659d-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="1659d-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="1659d-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="1659d-141">IDENTIFICADOR de idioma numérico del módulo de combinación de RequiredID.</span><span class="sxs-lookup"><span data-stu-id="1659d-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="1659d-142">La columna RequiredLanguage puede especificar el identificador de idioma de un solo idioma, por ejemplo, 1033 para Inglés de EE. UU., o especificar el identificador de idioma de un grupo de idiomas, como 9 para cualquier inglés.</span><span class="sxs-lookup"><span data-stu-id="1659d-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="1659d-143">Si el campo contiene un identificador de idioma de grupo, cualquier módulo de combinación que tenga un código de idioma en ese grupo cumple la dependencia.</span><span class="sxs-lookup"><span data-stu-id="1659d-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="1659d-144">Si RequiredLanguage se establece en 0, cualquier módulo de combinación que llene los demás requisitos satisface la dependencia.</span><span class="sxs-lookup"><span data-stu-id="1659d-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="1659d-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="1659d-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="1659d-146">Versión del módulo de combinación de RequiredID.</span><span class="sxs-lookup"><span data-stu-id="1659d-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="1659d-147">Si este campo es null, cualquier versión rellena la dependencia.</span><span class="sxs-lookup"><span data-stu-id="1659d-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1659d-148">Validación</span><span class="sxs-lookup"><span data-stu-id="1659d-148">Validation</span></span>

<dl>

[<span data-ttu-id="1659d-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="1659d-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1659d-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="1659d-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1659d-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="1659d-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



