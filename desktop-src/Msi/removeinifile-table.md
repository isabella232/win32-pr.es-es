---
description: La tabla RemoveIniFile contiene la información que debe eliminar una aplicación de un archivo. ini.
ms.assetid: 702cf86e-02f4-4ea7-8573-b500ac550aae
title: Tabla RemoveIniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57b4ba6f2c42ee636f1b9e21e798e27665f102a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669801"
---
# <a name="removeinifile-table"></a><span data-ttu-id="86064-103">Tabla RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="86064-103">RemoveIniFile Table</span></span>

<span data-ttu-id="86064-104">La tabla RemoveIniFile contiene la información que debe eliminar una aplicación de un archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="86064-104">The RemoveIniFile table contains the information an application needs to delete from a .ini file.</span></span>

<span data-ttu-id="86064-105">La tabla RemoveIniFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="86064-105">The RemoveIniFile table has the following columns.</span></span>



| <span data-ttu-id="86064-106">Columna</span><span class="sxs-lookup"><span data-stu-id="86064-106">Column</span></span>        | <span data-ttu-id="86064-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="86064-107">Type</span></span>                         | <span data-ttu-id="86064-108">Clave</span><span class="sxs-lookup"><span data-stu-id="86064-108">Key</span></span> | <span data-ttu-id="86064-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="86064-109">Nullable</span></span> |
|---------------|------------------------------|-----|----------|
| <span data-ttu-id="86064-110">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="86064-110">RemoveIniFile</span></span> | [<span data-ttu-id="86064-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="86064-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="86064-112">Y</span><span class="sxs-lookup"><span data-stu-id="86064-112">Y</span></span>   | <span data-ttu-id="86064-113">N</span><span class="sxs-lookup"><span data-stu-id="86064-113">N</span></span>        |
| <span data-ttu-id="86064-114">FileName</span><span class="sxs-lookup"><span data-stu-id="86064-114">FileName</span></span>      | [<span data-ttu-id="86064-115">FileName</span><span class="sxs-lookup"><span data-stu-id="86064-115">FileName</span></span>](text.md)         | <span data-ttu-id="86064-116">N</span><span class="sxs-lookup"><span data-stu-id="86064-116">N</span></span>   | <span data-ttu-id="86064-117">N</span><span class="sxs-lookup"><span data-stu-id="86064-117">N</span></span>        |
| <span data-ttu-id="86064-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="86064-118">DirProperty</span></span>   | [<span data-ttu-id="86064-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="86064-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="86064-120">N</span><span class="sxs-lookup"><span data-stu-id="86064-120">N</span></span>   | <span data-ttu-id="86064-121">Y</span><span class="sxs-lookup"><span data-stu-id="86064-121">Y</span></span>        |
| <span data-ttu-id="86064-122">Sección</span><span class="sxs-lookup"><span data-stu-id="86064-122">Section</span></span>       | [<span data-ttu-id="86064-123">Formatea</span><span class="sxs-lookup"><span data-stu-id="86064-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="86064-124">N</span><span class="sxs-lookup"><span data-stu-id="86064-124">N</span></span>   | <span data-ttu-id="86064-125">N</span><span class="sxs-lookup"><span data-stu-id="86064-125">N</span></span>        |
| <span data-ttu-id="86064-126">Clave</span><span class="sxs-lookup"><span data-stu-id="86064-126">Key</span></span>           | [<span data-ttu-id="86064-127">Formatea</span><span class="sxs-lookup"><span data-stu-id="86064-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="86064-128">N</span><span class="sxs-lookup"><span data-stu-id="86064-128">N</span></span>   | <span data-ttu-id="86064-129">N</span><span class="sxs-lookup"><span data-stu-id="86064-129">N</span></span>        |
| <span data-ttu-id="86064-130">Value</span><span class="sxs-lookup"><span data-stu-id="86064-130">Value</span></span>         | [<span data-ttu-id="86064-131">Formatea</span><span class="sxs-lookup"><span data-stu-id="86064-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="86064-132">N</span><span class="sxs-lookup"><span data-stu-id="86064-132">N</span></span>   | <span data-ttu-id="86064-133">Y</span><span class="sxs-lookup"><span data-stu-id="86064-133">Y</span></span>        |
| <span data-ttu-id="86064-134">Acción</span><span class="sxs-lookup"><span data-stu-id="86064-134">Action</span></span>        | [<span data-ttu-id="86064-135">Entero</span><span class="sxs-lookup"><span data-stu-id="86064-135">Integer</span></span>](integer.md)       | <span data-ttu-id="86064-136">N</span><span class="sxs-lookup"><span data-stu-id="86064-136">N</span></span>   | <span data-ttu-id="86064-137">N</span><span class="sxs-lookup"><span data-stu-id="86064-137">N</span></span>        |
| <span data-ttu-id="86064-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="86064-138">Component\_</span></span>   | [<span data-ttu-id="86064-139">Identificador</span><span class="sxs-lookup"><span data-stu-id="86064-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="86064-140">N</span><span class="sxs-lookup"><span data-stu-id="86064-140">N</span></span>   | <span data-ttu-id="86064-141">N</span><span class="sxs-lookup"><span data-stu-id="86064-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="86064-142">Columnas</span><span class="sxs-lookup"><span data-stu-id="86064-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="86064-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="86064-143"><span id="RemoveIniFile"></span><span id="removeinifile"></span><span id="REMOVEINIFILE"></span>RemoveIniFile</span></span>
</dt> <dd>

<span data-ttu-id="86064-144">La clave de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="86064-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="86064-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión</span><span class="sxs-lookup"><span data-stu-id="86064-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="86064-146">Nombre del archivo. ini en el que se va a eliminar la información.</span><span class="sxs-lookup"><span data-stu-id="86064-146">The .ini file name in which to delete the information.</span></span>

</dd> <dt>

<span data-ttu-id="86064-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="86064-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="86064-148">Nombre de una propiedad cuyo valor se supone que se va a resolver como la ruta de acceso completa a la carpeta del archivo. ini que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="86064-148">Name of a property whose value is assumed to resolve to the full path to the folder of the .ini file to be removed.</span></span> <span data-ttu-id="86064-149">La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="86064-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="86064-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal</span><span class="sxs-lookup"><span data-stu-id="86064-150"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="86064-151">La sección del archivo. ini localizable.</span><span class="sxs-lookup"><span data-stu-id="86064-151">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="86064-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="86064-152"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="86064-153">La clave del archivo. ini traducible debajo de la sección.</span><span class="sxs-lookup"><span data-stu-id="86064-153">The localizable .ini file key below the section.</span></span>

</dd> <dt>

<span data-ttu-id="86064-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="86064-154"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="86064-155">Valor traducible que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="86064-155">The localizable value to be deleted.</span></span> <span data-ttu-id="86064-156">El valor es necesario cuando la acción es 4.</span><span class="sxs-lookup"><span data-stu-id="86064-156">The value is required when Action is 4.</span></span>

</dd> <dt>

<span data-ttu-id="86064-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="86064-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="86064-158">Tipo de modificación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="86064-158">The type of modification to be made.</span></span>



| <span data-ttu-id="86064-159">Constante</span><span class="sxs-lookup"><span data-stu-id="86064-159">Constant</span></span>                         | <span data-ttu-id="86064-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="86064-160">Hexadecimal</span></span> | <span data-ttu-id="86064-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="86064-161">Decimal</span></span> | <span data-ttu-id="86064-162">Significado</span><span class="sxs-lookup"><span data-stu-id="86064-162">Meaning</span></span>                          |
|----------------------------------|-------------|---------|----------------------------------|
| <span data-ttu-id="86064-163">**msidbIniFileActionRemoveLine**</span><span class="sxs-lookup"><span data-stu-id="86064-163">**msidbIniFileActionRemoveLine**</span></span> | <span data-ttu-id="86064-164">0x002</span><span class="sxs-lookup"><span data-stu-id="86064-164">0x002</span></span>       | <span data-ttu-id="86064-165">2</span><span class="sxs-lookup"><span data-stu-id="86064-165">2</span></span>       | <span data-ttu-id="86064-166">Elimina la entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="86064-166">Deletes .ini entry.</span></span>              |
| <span data-ttu-id="86064-167">**msidbIniFileActionRemoveTag**</span><span class="sxs-lookup"><span data-stu-id="86064-167">**msidbIniFileActionRemoveTag**</span></span>  | <span data-ttu-id="86064-168">0x004</span><span class="sxs-lookup"><span data-stu-id="86064-168">0x004</span></span>       | <span data-ttu-id="86064-169">4</span><span class="sxs-lookup"><span data-stu-id="86064-169">4</span></span>       | <span data-ttu-id="86064-170">Elimina una etiqueta de una entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="86064-170">Deletes a tag from a .ini entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="86064-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="86064-171"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="86064-172">Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la eliminación del valor. ini.</span><span class="sxs-lookup"><span data-stu-id="86064-172">External key into first column of the [Component table](component-table.md) referencing the component that controls the deletion of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86064-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86064-173">Remarks</span></span>

<span data-ttu-id="86064-174">La información del archivo. ini se elimina cuando se selecciona la instalación del componente correspondiente, ya sea de forma local o se ejecuta desde el origen.</span><span class="sxs-lookup"><span data-stu-id="86064-174">The .ini file information is deleted when the corresponding Component has been selected to be installed, either locally or run from source.</span></span>

<span data-ttu-id="86064-175">Se hace referencia a esta tabla cuando se ejecuta la [acción RemoveIniValues](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="86064-175">This table is referred to when the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

<span data-ttu-id="86064-176">Si la columna de directorio \_ se especifica como null, la ubicación del archivo ini es la ubicación estándar de Windows ini, que es el directorio de Windows de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="86064-176">If the Directory\_ column is specified as null, the ini file location is the standard Windows ini location which is the Windows directory by default.</span></span>

<span data-ttu-id="86064-177">Al quitar el último valor de una sección, se elimina esa sección.</span><span class="sxs-lookup"><span data-stu-id="86064-177">Removing the last value from a section deletes that section.</span></span> <span data-ttu-id="86064-178">No hay ninguna otra manera de eliminar una sección completa que no sea la eliminación de todos sus valores.</span><span class="sxs-lookup"><span data-stu-id="86064-178">There is no other way to delete an entire section other than removing all its values.</span></span>

## <a name="validation"></a><span data-ttu-id="86064-179">Validación</span><span class="sxs-lookup"><span data-stu-id="86064-179">Validation</span></span>

<dl>

[<span data-ttu-id="86064-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="86064-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="86064-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="86064-181">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="86064-182">ICE32</span><span class="sxs-lookup"><span data-stu-id="86064-182">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="86064-183">ICE40</span><span class="sxs-lookup"><span data-stu-id="86064-183">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="86064-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="86064-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="86064-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="86064-185">ICE69</span></span>](ice69.md)  
</dl>

 

 



