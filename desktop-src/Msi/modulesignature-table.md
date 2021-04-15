---
description: La tabla ModuleSignature es una tabla obligatoria.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545683"
---
# <a name="modulesignature-table"></a><span data-ttu-id="b9774-103">ModuleSignature (tabla)</span><span class="sxs-lookup"><span data-stu-id="b9774-103">ModuleSignature Table</span></span>

<span data-ttu-id="b9774-104">La tabla ModuleSignature es una tabla obligatoria.</span><span class="sxs-lookup"><span data-stu-id="b9774-104">The ModuleSignature Table is a required table.</span></span> <span data-ttu-id="b9774-105">Contiene toda la información necesaria para identificar un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="b9774-105">It contains all the information necessary to identify a merge module.</span></span> <span data-ttu-id="b9774-106">La herramienta de combinación agrega esta tabla al archivo. msi si aún no existe una.</span><span class="sxs-lookup"><span data-stu-id="b9774-106">The merge tool adds this table to the .msi file if one does not already exist.</span></span> <span data-ttu-id="b9774-107">La tabla ModuleSignature de un módulo de combinación solo tiene una fila que contiene el valor de ModuleID, el idioma y la versión.</span><span class="sxs-lookup"><span data-stu-id="b9774-107">The ModuleSignature table in a merge module has only one row containing the ModuleID, Language, and Version.</span></span> <span data-ttu-id="b9774-108">Sin embargo, la tabla ModuleSignature de un archivo. msi tiene una fila que contiene esta información para cada archivo. MSM que se ha combinado en él.</span><span class="sxs-lookup"><span data-stu-id="b9774-108">However, the ModuleSignature table in an .msi file has a row containing this information for each .msm file that has been merged into it.</span></span>

<span data-ttu-id="b9774-109">Las herramientas de combinación y comprobación comprueban la tabla ModuleSignature en los archivos. msi para determinar si tienen todos los módulos de combinación dependientes necesarios para el módulo de combinación actual (vea la [tabla ModuleDependency](moduledependency-table.md)) y si el paquete de instalación se combinó previamente con los módulos de combinación conflictivos (vea la [tabla ModuleExclusion](moduleexclusion-table.md)).</span><span class="sxs-lookup"><span data-stu-id="b9774-109">Merge and verification tools check the ModuleSignature table in .msi files to determine if it has all of the dependent merge modules required by the current merge module (see [ModuleDependency Table](moduledependency-table.md)) and whether the installation package was previously merged with any conflicting merge modules (see [ModuleExclusion Table](moduleexclusion-table.md)).</span></span>

<span data-ttu-id="b9774-110">La tabla ModuleSignature tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9774-110">The ModuleSignature table has the following columns.</span></span>



| <span data-ttu-id="b9774-111">Columna</span><span class="sxs-lookup"><span data-stu-id="b9774-111">Column</span></span>   | <span data-ttu-id="b9774-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9774-112">Type</span></span>                         | <span data-ttu-id="b9774-113">Clave</span><span class="sxs-lookup"><span data-stu-id="b9774-113">Key</span></span> | <span data-ttu-id="b9774-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="b9774-114">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="b9774-115">ModuleID</span><span class="sxs-lookup"><span data-stu-id="b9774-115">ModuleID</span></span> | [<span data-ttu-id="b9774-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="b9774-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="b9774-117">Y</span><span class="sxs-lookup"><span data-stu-id="b9774-117">Y</span></span>   | <span data-ttu-id="b9774-118">N</span><span class="sxs-lookup"><span data-stu-id="b9774-118">N</span></span>        |
| <span data-ttu-id="b9774-119">Idioma</span><span class="sxs-lookup"><span data-stu-id="b9774-119">Language</span></span> | [<span data-ttu-id="b9774-120">Entero</span><span class="sxs-lookup"><span data-stu-id="b9774-120">Integer</span></span>](integer.md)       | <span data-ttu-id="b9774-121">Y</span><span class="sxs-lookup"><span data-stu-id="b9774-121">Y</span></span>   | <span data-ttu-id="b9774-122">N</span><span class="sxs-lookup"><span data-stu-id="b9774-122">N</span></span>        |
| <span data-ttu-id="b9774-123">Versión</span><span class="sxs-lookup"><span data-stu-id="b9774-123">Version</span></span>  | [<span data-ttu-id="b9774-124">Versión</span><span class="sxs-lookup"><span data-stu-id="b9774-124">Version</span></span>](version.md)       |     | <span data-ttu-id="b9774-125">N</span><span class="sxs-lookup"><span data-stu-id="b9774-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b9774-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="b9774-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b9774-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="b9774-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="b9774-128">Identificador que identifica de forma única el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="b9774-128">An identifier that uniquely identifies the merge module.</span></span> <span data-ttu-id="b9774-129">Dos módulos de combinación no pueden tener el mismo ModuleID a menos que el módulo de combinación sea totalmente compatible con la predecesora.</span><span class="sxs-lookup"><span data-stu-id="b9774-129">Two merge modules cannot have the same ModuleID unless the merge module is entirely backward compatible with its predecessor.</span></span> <span data-ttu-id="b9774-130">Puede crear un GUID para este campo mediante una utilidad como GUIDGEN.</span><span class="sxs-lookup"><span data-stu-id="b9774-130">You can create a GUID for this field using a utility such as GUIDGEN.</span></span> <span data-ttu-id="b9774-131">La columna ModuleID es una clave principal de la tabla y, por lo tanto, debe seguir la Convención de nomenclatura de [asignar nombres a las claves principales de las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="b9774-131">The ModuleID column is a primary key for the table and therefore it must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="b9774-132">Por ejemplo, si el nombre legible del módulo de combinación es myLibrary y el GUID es {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la entrada de la columna ModuleID se convierte en myLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.</span><span class="sxs-lookup"><span data-stu-id="b9774-132">For example, if the readable name of the merge module is MyLibrary and the GUID is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

</dd> <dt>

<span data-ttu-id="b9774-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo</span><span class="sxs-lookup"><span data-stu-id="b9774-133"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="b9774-134">El identificador de idioma especifica el idioma predeterminado para el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="b9774-134">The Language identifier specifies the default language for the merge module.</span></span> <span data-ttu-id="b9774-135">El identificador de idioma está en formato decimal; por ejemplo, Inglés de EE. UU. es 1033.</span><span class="sxs-lookup"><span data-stu-id="b9774-135">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="b9774-136">El lenguaje utilizado por el módulo de combinación se puede cambiar aplicando una transformación al módulo de combinación antes de la combinación.</span><span class="sxs-lookup"><span data-stu-id="b9774-136">The language used by the merge module can be changed by applying a transform to the merge module before merging.</span></span>

</dd> <dt>

<span data-ttu-id="b9774-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión</span><span class="sxs-lookup"><span data-stu-id="b9774-137"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version</span></span>
</dt> <dd>

<span data-ttu-id="b9774-138">El campo versión contiene una cadena que describe las versiones principal y secundaria del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="b9774-138">The Version field contains a string that describes the major and minor versions of the merge module.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b9774-139">Validación</span><span class="sxs-lookup"><span data-stu-id="b9774-139">Validation</span></span>

<dl>

[<span data-ttu-id="b9774-140">ICE03</span><span class="sxs-lookup"><span data-stu-id="b9774-140">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b9774-141">ICE06</span><span class="sxs-lookup"><span data-stu-id="b9774-141">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b9774-142">ICE25</span><span class="sxs-lookup"><span data-stu-id="b9774-142">ICE25</span></span>](ice25.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="b9774-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9774-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9774-144">Módulos de combinación en varios idiomas</span><span class="sxs-lookup"><span data-stu-id="b9774-144">Multiple Language Merge Modules</span></span>](multiple-language-merge-modules.md)
</dt> </dl>

 

 



