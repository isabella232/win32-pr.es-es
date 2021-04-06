---
description: La tabla RemoveRegistry contiene la información del registro que la aplicación necesita para eliminar del registro del sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabla RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002198"
---
# <a name="removeregistry-table"></a><span data-ttu-id="3386e-103">Tabla RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="3386e-103">RemoveRegistry Table</span></span>

<span data-ttu-id="3386e-104">La tabla RemoveRegistry contiene la información del registro que la aplicación necesita para eliminar del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="3386e-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="3386e-105">La tabla RemoveRegistry tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3386e-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="3386e-106">Columna</span><span class="sxs-lookup"><span data-stu-id="3386e-106">Column</span></span>         | <span data-ttu-id="3386e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3386e-107">Type</span></span>                         | <span data-ttu-id="3386e-108">Clave</span><span class="sxs-lookup"><span data-stu-id="3386e-108">Key</span></span> | <span data-ttu-id="3386e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="3386e-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="3386e-110">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="3386e-110">RemoveRegistry</span></span> | [<span data-ttu-id="3386e-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="3386e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="3386e-112">Y</span><span class="sxs-lookup"><span data-stu-id="3386e-112">Y</span></span>   | <span data-ttu-id="3386e-113">N</span><span class="sxs-lookup"><span data-stu-id="3386e-113">N</span></span>        |
| <span data-ttu-id="3386e-114">Root</span><span class="sxs-lookup"><span data-stu-id="3386e-114">Root</span></span>           | [<span data-ttu-id="3386e-115">Entero</span><span class="sxs-lookup"><span data-stu-id="3386e-115">Integer</span></span>](integer.md)       | <span data-ttu-id="3386e-116">N</span><span class="sxs-lookup"><span data-stu-id="3386e-116">N</span></span>   | <span data-ttu-id="3386e-117">N</span><span class="sxs-lookup"><span data-stu-id="3386e-117">N</span></span>        |
| <span data-ttu-id="3386e-118">Clave</span><span class="sxs-lookup"><span data-stu-id="3386e-118">Key</span></span>            | [<span data-ttu-id="3386e-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="3386e-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="3386e-120">N</span><span class="sxs-lookup"><span data-stu-id="3386e-120">N</span></span>   | <span data-ttu-id="3386e-121">N</span><span class="sxs-lookup"><span data-stu-id="3386e-121">N</span></span>        |
| <span data-ttu-id="3386e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="3386e-122">Name</span></span>           | [<span data-ttu-id="3386e-123">Formatea</span><span class="sxs-lookup"><span data-stu-id="3386e-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3386e-124">N</span><span class="sxs-lookup"><span data-stu-id="3386e-124">N</span></span>   | <span data-ttu-id="3386e-125">Y</span><span class="sxs-lookup"><span data-stu-id="3386e-125">Y</span></span>        |
| <span data-ttu-id="3386e-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="3386e-126">Component\_</span></span>    | [<span data-ttu-id="3386e-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="3386e-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="3386e-128">N</span><span class="sxs-lookup"><span data-stu-id="3386e-128">N</span></span>   | <span data-ttu-id="3386e-129">N</span><span class="sxs-lookup"><span data-stu-id="3386e-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3386e-130">Columnas</span><span class="sxs-lookup"><span data-stu-id="3386e-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3386e-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="3386e-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="3386e-132">La clave de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="3386e-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="3386e-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raíces</span><span class="sxs-lookup"><span data-stu-id="3386e-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="3386e-134">Clave raíz predefinida para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="3386e-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="3386e-135">Constante</span><span class="sxs-lookup"><span data-stu-id="3386e-135">Constant</span></span>                          | <span data-ttu-id="3386e-136">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3386e-136">Hexadecimal</span></span> | <span data-ttu-id="3386e-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="3386e-137">Decimal</span></span> | <span data-ttu-id="3386e-138">Clave raíz</span><span class="sxs-lookup"><span data-stu-id="3386e-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3386e-139">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="3386e-139">(none)</span></span>                            | <span data-ttu-id="3386e-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="3386e-140">\- 0x001</span></span>    | <span data-ttu-id="3386e-141">-1</span><span class="sxs-lookup"><span data-stu-id="3386e-141">-1</span></span>      | <span data-ttu-id="3386e-142">**HKEY \_ El instalador del \_ usuario actual** establece esta clave mientras realiza una instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="3386e-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="3386e-143">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="3386e-143">(none)</span></span>                            | <span data-ttu-id="3386e-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="3386e-144">-0x001</span></span>      | <span data-ttu-id="3386e-145">-1</span><span class="sxs-lookup"><span data-stu-id="3386e-145">-1</span></span>      | <span data-ttu-id="3386e-146">**HKEY \_ El instalador del \_ equipo local** establece esta clave mientras se realiza una instalación de todos los usuarios con [**AllUsers**](allusers.md) establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="3386e-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="3386e-147">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="3386e-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="3386e-148">0x000</span><span class="sxs-lookup"><span data-stu-id="3386e-148">0x000</span></span>       | <span data-ttu-id="3386e-149">0</span><span class="sxs-lookup"><span data-stu-id="3386e-149">0</span></span>       | <span data-ttu-id="3386e-150">**HKEY \_ CLASES \_ raíz** el instalador quita el valor de la subárbol de **\\ \\ clases de software HKCU** durante las instalaciones en el [contexto de instalación](installation-context.md)por usuario y por equipo.</span><span class="sxs-lookup"><span data-stu-id="3386e-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="3386e-151">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="3386e-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="3386e-152">0x001</span><span class="sxs-lookup"><span data-stu-id="3386e-152">0x001</span></span>       | <span data-ttu-id="3386e-153">1</span><span class="sxs-lookup"><span data-stu-id="3386e-153">1</span></span>       | <span data-ttu-id="3386e-154">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="3386e-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="3386e-155">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="3386e-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="3386e-156">0x002</span><span class="sxs-lookup"><span data-stu-id="3386e-156">0x002</span></span>       | <span data-ttu-id="3386e-157">2</span><span class="sxs-lookup"><span data-stu-id="3386e-157">2</span></span>       | <span data-ttu-id="3386e-158">**HKEY \_ local \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="3386e-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="3386e-159">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="3386e-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="3386e-160">0x003</span><span class="sxs-lookup"><span data-stu-id="3386e-160">0x003</span></span>       | <span data-ttu-id="3386e-161">3</span><span class="sxs-lookup"><span data-stu-id="3386e-161">3</span></span>       | <span data-ttu-id="3386e-162">**\_usuarios HKEY**</span><span class="sxs-lookup"><span data-stu-id="3386e-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="3386e-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="3386e-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="3386e-164">La clave localizable para el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="3386e-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="3386e-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="3386e-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3386e-166">Nombre del valor del registro localizable.</span><span class="sxs-lookup"><span data-stu-id="3386e-166">The localizable registry value name.</span></span>

<span data-ttu-id="3386e-167">La cadena siguiente en la columna Name tiene una importancia especial.</span><span class="sxs-lookup"><span data-stu-id="3386e-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="3386e-168">String</span><span class="sxs-lookup"><span data-stu-id="3386e-168">String</span></span> | <span data-ttu-id="3386e-169">Significado</span><span class="sxs-lookup"><span data-stu-id="3386e-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3386e-170">"-"</span><span class="sxs-lookup"><span data-stu-id="3386e-170">"-"</span></span>    | <span data-ttu-id="3386e-171">La clave se eliminará, si está presente, con todos sus valores y subclaves, cuando se instale el componente.</span><span class="sxs-lookup"><span data-stu-id="3386e-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="3386e-172">Tenga en cuenta que la [tabla del registro](registry-table.md) se debe utilizar para crear o quitar una clave del registro cuando se quita el componente.</span><span class="sxs-lookup"><span data-stu-id="3386e-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="3386e-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="3386e-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="3386e-174">Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la eliminación del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="3386e-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3386e-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3386e-175">Remarks</span></span>

<span data-ttu-id="3386e-176">La información del registro se elimina del registro del sistema cuando se ha seleccionado el componente correspondiente para instalarse localmente o ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="3386e-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="3386e-177">Se hace referencia a esta tabla cuando se ejecuta la [acción RemoveRegistryValues](removeregistryvalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3386e-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="3386e-178">Validación</span><span class="sxs-lookup"><span data-stu-id="3386e-178">Validation</span></span>

<dl>

[<span data-ttu-id="3386e-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="3386e-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3386e-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="3386e-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3386e-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="3386e-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3386e-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="3386e-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3386e-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="3386e-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




