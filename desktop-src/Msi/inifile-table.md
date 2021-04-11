---
description: La tabla IniFile contiene la información. ini que la aplicación necesita para establecer en un archivo. ini.
ms.assetid: fdb1a627-da6b-4da1-87a7-7f1c94d3836e
title: Tabla IniFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d63ae37f7c8ed5c50b9b425b0462b445f7acb5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082534"
---
# <a name="inifile-table"></a><span data-ttu-id="1d456-103">Tabla IniFile</span><span class="sxs-lookup"><span data-stu-id="1d456-103">IniFile Table</span></span>

<span data-ttu-id="1d456-104">La tabla IniFile contiene la información. ini que la aplicación necesita para establecer en un archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="1d456-104">The IniFile table contains the .ini information that the application needs to set in an .ini file.</span></span>

<span data-ttu-id="1d456-105">La tabla IniFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1d456-105">The IniFile table has the following columns.</span></span>



| <span data-ttu-id="1d456-106">Columna</span><span class="sxs-lookup"><span data-stu-id="1d456-106">Column</span></span>      | <span data-ttu-id="1d456-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d456-107">Type</span></span>                         | <span data-ttu-id="1d456-108">Clave</span><span class="sxs-lookup"><span data-stu-id="1d456-108">Key</span></span> | <span data-ttu-id="1d456-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="1d456-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="1d456-110">IniFile</span><span class="sxs-lookup"><span data-stu-id="1d456-110">IniFile</span></span>     | [<span data-ttu-id="1d456-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="1d456-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="1d456-112">Y</span><span class="sxs-lookup"><span data-stu-id="1d456-112">Y</span></span>   | <span data-ttu-id="1d456-113">N</span><span class="sxs-lookup"><span data-stu-id="1d456-113">N</span></span>        |
| <span data-ttu-id="1d456-114">FileName</span><span class="sxs-lookup"><span data-stu-id="1d456-114">FileName</span></span>    | [<span data-ttu-id="1d456-115">FileName</span><span class="sxs-lookup"><span data-stu-id="1d456-115">FileName</span></span>](text.md)         | <span data-ttu-id="1d456-116">N</span><span class="sxs-lookup"><span data-stu-id="1d456-116">N</span></span>   | <span data-ttu-id="1d456-117">N</span><span class="sxs-lookup"><span data-stu-id="1d456-117">N</span></span>        |
| <span data-ttu-id="1d456-118">DirProperty</span><span class="sxs-lookup"><span data-stu-id="1d456-118">DirProperty</span></span> | [<span data-ttu-id="1d456-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="1d456-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="1d456-120">N</span><span class="sxs-lookup"><span data-stu-id="1d456-120">N</span></span>   | <span data-ttu-id="1d456-121">Y</span><span class="sxs-lookup"><span data-stu-id="1d456-121">Y</span></span>        |
| <span data-ttu-id="1d456-122">Sección</span><span class="sxs-lookup"><span data-stu-id="1d456-122">Section</span></span>     | [<span data-ttu-id="1d456-123">Formatea</span><span class="sxs-lookup"><span data-stu-id="1d456-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1d456-124">N</span><span class="sxs-lookup"><span data-stu-id="1d456-124">N</span></span>   | <span data-ttu-id="1d456-125">N</span><span class="sxs-lookup"><span data-stu-id="1d456-125">N</span></span>        |
| <span data-ttu-id="1d456-126">Clave</span><span class="sxs-lookup"><span data-stu-id="1d456-126">Key</span></span>         | [<span data-ttu-id="1d456-127">Formatea</span><span class="sxs-lookup"><span data-stu-id="1d456-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1d456-128">N</span><span class="sxs-lookup"><span data-stu-id="1d456-128">N</span></span>   | <span data-ttu-id="1d456-129">N</span><span class="sxs-lookup"><span data-stu-id="1d456-129">N</span></span>        |
| <span data-ttu-id="1d456-130">Value</span><span class="sxs-lookup"><span data-stu-id="1d456-130">Value</span></span>       | [<span data-ttu-id="1d456-131">Formatea</span><span class="sxs-lookup"><span data-stu-id="1d456-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1d456-132">N</span><span class="sxs-lookup"><span data-stu-id="1d456-132">N</span></span>   | <span data-ttu-id="1d456-133">N</span><span class="sxs-lookup"><span data-stu-id="1d456-133">N</span></span>        |
| <span data-ttu-id="1d456-134">Acción</span><span class="sxs-lookup"><span data-stu-id="1d456-134">Action</span></span>      | [<span data-ttu-id="1d456-135">Entero</span><span class="sxs-lookup"><span data-stu-id="1d456-135">Integer</span></span>](integer.md)       | <span data-ttu-id="1d456-136">N</span><span class="sxs-lookup"><span data-stu-id="1d456-136">N</span></span>   | <span data-ttu-id="1d456-137">N</span><span class="sxs-lookup"><span data-stu-id="1d456-137">N</span></span>        |
| <span data-ttu-id="1d456-138">Componente\_</span><span class="sxs-lookup"><span data-stu-id="1d456-138">Component\_</span></span> | [<span data-ttu-id="1d456-139">Identificador</span><span class="sxs-lookup"><span data-stu-id="1d456-139">Identifier</span></span>](identifier.md) | <span data-ttu-id="1d456-140">N</span><span class="sxs-lookup"><span data-stu-id="1d456-140">N</span></span>   | <span data-ttu-id="1d456-141">N</span><span class="sxs-lookup"><span data-stu-id="1d456-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1d456-142">Columnas</span><span class="sxs-lookup"><span data-stu-id="1d456-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1d456-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span><span class="sxs-lookup"><span data-stu-id="1d456-143"><span id="IniFile"></span><span id="inifile"></span><span id="INIFILE"></span>IniFile</span></span>
</dt> <dd>

<span data-ttu-id="1d456-144">La clave de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="1d456-144">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión</span><span class="sxs-lookup"><span data-stu-id="1d456-145"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="1d456-146">Nombre traducible del archivo. ini en el que se va a escribir la información.</span><span class="sxs-lookup"><span data-stu-id="1d456-146">The localizable name of the .ini file in which to write the information.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="1d456-147"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="1d456-148">Nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa de la carpeta que contiene el archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="1d456-148">Name of a property having a value that resolves to the full path of the folder containing the .ini file.</span></span> <span data-ttu-id="1d456-149">La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="1d456-149">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span> <span data-ttu-id="1d456-150">Si este campo se deja en blanco, se crea el archivo. ini en la carpeta que tiene la ruta de acceso completa especificada por la propiedad [**WindowsFolder**](windowsfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="1d456-150">If this field is left blank, the .ini file is created in the folder having the full path specified by the [**WindowsFolder**](windowsfolder.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal</span><span class="sxs-lookup"><span data-stu-id="1d456-151"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="1d456-152">La sección del archivo. ini localizable.</span><span class="sxs-lookup"><span data-stu-id="1d456-152">The localizable .ini file section.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave</span><span class="sxs-lookup"><span data-stu-id="1d456-153"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="1d456-154">La clave del archivo. ini traducible dentro de la sección.</span><span class="sxs-lookup"><span data-stu-id="1d456-154">The localizable .ini file key within the section.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="1d456-155"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="1d456-156">Valor traducible que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="1d456-156">The localizable value to be written.</span></span>

</dd> <dt>

<span data-ttu-id="1d456-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="1d456-157"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="1d456-158">Tipo de modificación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="1d456-158">The type of modification to be made.</span></span>



| <span data-ttu-id="1d456-159">Constante</span><span class="sxs-lookup"><span data-stu-id="1d456-159">Constant</span></span>                         | <span data-ttu-id="1d456-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="1d456-160">Hexadecimal</span></span> | <span data-ttu-id="1d456-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="1d456-161">Decimal</span></span> | <span data-ttu-id="1d456-162">Modificación</span><span class="sxs-lookup"><span data-stu-id="1d456-162">Modification</span></span>                                                                     |
|----------------------------------|-------------|---------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1d456-163">**msidbIniFileActionAddLine**</span><span class="sxs-lookup"><span data-stu-id="1d456-163">**msidbIniFileActionAddLine**</span></span>    | <span data-ttu-id="1d456-164">0x000</span><span class="sxs-lookup"><span data-stu-id="1d456-164">0x000</span></span>       | <span data-ttu-id="1d456-165">0</span><span class="sxs-lookup"><span data-stu-id="1d456-165">0</span></span>       | <span data-ttu-id="1d456-166">Crea o actualiza una entrada. ini.</span><span class="sxs-lookup"><span data-stu-id="1d456-166">Creates or updates a .ini entry.</span></span>                                                 |
| <span data-ttu-id="1d456-167">**msidbIniFileActionCreateLine**</span><span class="sxs-lookup"><span data-stu-id="1d456-167">**msidbIniFileActionCreateLine**</span></span> | <span data-ttu-id="1d456-168">0x001</span><span class="sxs-lookup"><span data-stu-id="1d456-168">0x001</span></span>       | <span data-ttu-id="1d456-169">1</span><span class="sxs-lookup"><span data-stu-id="1d456-169">1</span></span>       | <span data-ttu-id="1d456-170">Crea una entrada. ini solo si la entrada no existe.</span><span class="sxs-lookup"><span data-stu-id="1d456-170">Creates a .ini entry only if the entry does not already exist.</span></span>                   |
| <span data-ttu-id="1d456-171">**msidbIniFileActionAddTag**</span><span class="sxs-lookup"><span data-stu-id="1d456-171">**msidbIniFileActionAddTag**</span></span>     | <span data-ttu-id="1d456-172">0x003</span><span class="sxs-lookup"><span data-stu-id="1d456-172">0x003</span></span>       | <span data-ttu-id="1d456-173">3</span><span class="sxs-lookup"><span data-stu-id="1d456-173">3</span></span>       | <span data-ttu-id="1d456-174">Crea una nueva entrada o anexa un nuevo valor separado por comas a una entrada existente.</span><span class="sxs-lookup"><span data-stu-id="1d456-174">Creates a new entry or appends a new comma-separated value to an existing entry.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1d456-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="1d456-175"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="1d456-176">Clave externa en la primera columna de la [tabla de componentes](component-table.md) que hace referencia al componente que controla la instalación del valor. ini.</span><span class="sxs-lookup"><span data-stu-id="1d456-176">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the .ini value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d456-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d456-177">Remarks</span></span>

<span data-ttu-id="1d456-178">La información del archivo. ini se escribe cuando se ha seleccionado el componente correspondiente para instalarlo como local o ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="1d456-178">The .ini file information is written out when the corresponding component has been selected to be installed as local or run from source.</span></span>

<span data-ttu-id="1d456-179">Se hace referencia a esta tabla cuando se ejecuta la acción [WriteIniValues](writeinivalues-action.md) o la [acción RemoveIniValues](removeinivalues-action.md) .</span><span class="sxs-lookup"><span data-stu-id="1d456-179">This table is referred to when the [WriteIniValues action](writeinivalues-action.md) or the [RemoveIniValues action](removeinivalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="1d456-180">Validación</span><span class="sxs-lookup"><span data-stu-id="1d456-180">Validation</span></span>

<dl>

[<span data-ttu-id="1d456-181">ICE03</span><span class="sxs-lookup"><span data-stu-id="1d456-181">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1d456-182">ICE06</span><span class="sxs-lookup"><span data-stu-id="1d456-182">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1d456-183">ICE32</span><span class="sxs-lookup"><span data-stu-id="1d456-183">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="1d456-184">ICE46</span><span class="sxs-lookup"><span data-stu-id="1d456-184">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="1d456-185">ICE69</span><span class="sxs-lookup"><span data-stu-id="1d456-185">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="1d456-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="1d456-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="1d456-187">ICE91</span><span class="sxs-lookup"><span data-stu-id="1d456-187">ICE91</span></span>](ice91.md)  
</dl>

 

 



