---
description: La tabla RemoveFile contiene una lista de archivos que se van a quitar mediante la acción RemoveFiles. La configuración de la columna FileName de esta tabla en NULL admite la eliminación de carpetas vacías.
ms.assetid: 8b3cb0e3-ccc0-4030-8f57-aa124c3b5588
title: Tabla RemoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723e42582821d79842686678c5b310e95cd1e944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911333"
---
# <a name="removefile-table"></a><span data-ttu-id="eb372-104">Tabla RemoveFile</span><span class="sxs-lookup"><span data-stu-id="eb372-104">RemoveFile Table</span></span>

<span data-ttu-id="eb372-105">La tabla RemoveFile contiene una lista de archivos que se van a quitar mediante la [acción RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="eb372-105">The RemoveFile table contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span> <span data-ttu-id="eb372-106">La configuración de la columna FileName de esta tabla en NULL admite la eliminación de carpetas vacías.</span><span class="sxs-lookup"><span data-stu-id="eb372-106">Setting the FileName column of this table to Null supports the removal of empty folders.</span></span>

<span data-ttu-id="eb372-107">La tabla RemoveFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb372-107">The RemoveFile table has the following columns.</span></span>



| <span data-ttu-id="eb372-108">Columna</span><span class="sxs-lookup"><span data-stu-id="eb372-108">Column</span></span>      | <span data-ttu-id="eb372-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb372-109">Type</span></span>                                     | <span data-ttu-id="eb372-110">Clave</span><span class="sxs-lookup"><span data-stu-id="eb372-110">Key</span></span> | <span data-ttu-id="eb372-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="eb372-111">Nullable</span></span> |
|-------------|------------------------------------------|-----|----------|
| <span data-ttu-id="eb372-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="eb372-112">FileKey</span></span>     | [<span data-ttu-id="eb372-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="eb372-113">Identifier</span></span>](identifier.md)             | <span data-ttu-id="eb372-114">Y</span><span class="sxs-lookup"><span data-stu-id="eb372-114">Y</span></span>   | <span data-ttu-id="eb372-115">N</span><span class="sxs-lookup"><span data-stu-id="eb372-115">N</span></span>        |
| <span data-ttu-id="eb372-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="eb372-116">Component\_</span></span> | [<span data-ttu-id="eb372-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="eb372-117">Identifier</span></span>](identifier.md)             | <span data-ttu-id="eb372-118">N</span><span class="sxs-lookup"><span data-stu-id="eb372-118">N</span></span>   | <span data-ttu-id="eb372-119">N</span><span class="sxs-lookup"><span data-stu-id="eb372-119">N</span></span>        |
| <span data-ttu-id="eb372-120">FileName</span><span class="sxs-lookup"><span data-stu-id="eb372-120">FileName</span></span>    | [<span data-ttu-id="eb372-121">WildCardFilename</span><span class="sxs-lookup"><span data-stu-id="eb372-121">WildCardFilename</span></span>](wildcardfilename.md) | <span data-ttu-id="eb372-122">N</span><span class="sxs-lookup"><span data-stu-id="eb372-122">N</span></span>   | <span data-ttu-id="eb372-123">Y</span><span class="sxs-lookup"><span data-stu-id="eb372-123">Y</span></span>        |
| <span data-ttu-id="eb372-124">DirProperty</span><span class="sxs-lookup"><span data-stu-id="eb372-124">DirProperty</span></span> | [<span data-ttu-id="eb372-125">Identificador</span><span class="sxs-lookup"><span data-stu-id="eb372-125">Identifier</span></span>](identifier.md)             | <span data-ttu-id="eb372-126">N</span><span class="sxs-lookup"><span data-stu-id="eb372-126">N</span></span>   | <span data-ttu-id="eb372-127">N</span><span class="sxs-lookup"><span data-stu-id="eb372-127">N</span></span>        |
| <span data-ttu-id="eb372-128">InstallMode</span><span class="sxs-lookup"><span data-stu-id="eb372-128">InstallMode</span></span> | [<span data-ttu-id="eb372-129">Entero</span><span class="sxs-lookup"><span data-stu-id="eb372-129">Integer</span></span>](integer.md)                   | <span data-ttu-id="eb372-130">N</span><span class="sxs-lookup"><span data-stu-id="eb372-130">N</span></span>   | <span data-ttu-id="eb372-131">N</span><span class="sxs-lookup"><span data-stu-id="eb372-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="eb372-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="eb372-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="eb372-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="eb372-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="eb372-134">Clave principal usada para identificar esta entrada de tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="eb372-134">Primary key used to identify this particular table entry.</span></span>

</dd> <dt>

<span data-ttu-id="eb372-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="eb372-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="eb372-136">Clave externa la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb372-136">External key the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="eb372-137">Este campo hace referencia al componente que controla el archivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="eb372-137">This field references the component that controls the file to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="eb372-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión</span><span class="sxs-lookup"><span data-stu-id="eb372-138"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="eb372-139">Esta columna contiene el nombre traducible del archivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="eb372-139">This column contains the localizable name of the file to be removed.</span></span> <span data-ttu-id="eb372-140">Si esta columna es null, se quitará la carpeta especificada si está vacía.</span><span class="sxs-lookup"><span data-stu-id="eb372-140">If this column is null, then the specified folder will be removed if it is empty.</span></span> <span data-ttu-id="eb372-141">Todos los archivos que coinciden con el carácter comodín se quitarán del directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="eb372-141">All of the files that match the wildcard will be removed from the specified directory.</span></span>

</dd> <dt>

<span data-ttu-id="eb372-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span><span class="sxs-lookup"><span data-stu-id="eb372-142"><span id="DirProperty"></span><span id="dirproperty"></span><span id="DIRPROPERTY"></span>DirProperty</span></span>
</dt> <dd>

<span data-ttu-id="eb372-143">Nombre de una propiedad cuyo valor se supone que se va a resolver como la ruta de acceso completa a la carpeta del archivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="eb372-143">Name of a property whose value is assumed to resolve to the full path to the folder of the file to be removed.</span></span> <span data-ttu-id="eb372-144">La propiedad puede ser el nombre de un directorio en la [tabla del directorio](directory-table.md), una propiedad establecida por la [tabla AppSearch](appsearch-table.md)o cualquier otra propiedad que represente una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="eb372-144">The property can be the name of a directory in the [Directory table](directory-table.md), a property set by the [AppSearch table](appsearch-table.md), or any other property that represents a full path.</span></span>

</dd> <dt>

<span data-ttu-id="eb372-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span><span class="sxs-lookup"><span data-stu-id="eb372-145"><span id="InstallMode"></span><span id="installmode"></span><span id="INSTALLMODE"></span>InstallMode</span></span>
</dt> <dd>

<span data-ttu-id="eb372-146">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb372-146">Must be one of the following values.</span></span>



| <span data-ttu-id="eb372-147">Constante</span><span class="sxs-lookup"><span data-stu-id="eb372-147">Constant</span></span>                                | <span data-ttu-id="eb372-148">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="eb372-148">Hexadecimal</span></span> | <span data-ttu-id="eb372-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="eb372-149">Decimal</span></span> | <span data-ttu-id="eb372-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb372-150">Description</span></span>                                                                                                   |
|-----------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb372-151">**msidbRemoveFileInstallModeOnInstall**</span><span class="sxs-lookup"><span data-stu-id="eb372-151">**msidbRemoveFileInstallModeOnInstall**</span></span> | <span data-ttu-id="eb372-152">0x001</span><span class="sxs-lookup"><span data-stu-id="eb372-152">0x001</span></span>       | <span data-ttu-id="eb372-153">1</span><span class="sxs-lookup"><span data-stu-id="eb372-153">1</span></span>       | <span data-ttu-id="eb372-154">Quitar solo cuando se está instalando el componente asociado (msiInstallStateLocal o msiInstallStateSource).</span><span class="sxs-lookup"><span data-stu-id="eb372-154">Remove only when the associated component is being installed (msiInstallStateLocal or msiInstallStateSource).</span></span> |
| <span data-ttu-id="eb372-155">**msidbRemoveFileInstallModeOnRemove**</span><span class="sxs-lookup"><span data-stu-id="eb372-155">**msidbRemoveFileInstallModeOnRemove**</span></span>  | <span data-ttu-id="eb372-156">0x002</span><span class="sxs-lookup"><span data-stu-id="eb372-156">0x002</span></span>       | <span data-ttu-id="eb372-157">2</span><span class="sxs-lookup"><span data-stu-id="eb372-157">2</span></span>       | <span data-ttu-id="eb372-158">Quitar solo cuando se quita el componente asociado (msiInstallStateAbsent).</span><span class="sxs-lookup"><span data-stu-id="eb372-158">Remove only when the associated component is being removed (msiInstallStateAbsent).</span></span>                           |
| <span data-ttu-id="eb372-159">**msidbRemoveFileInstallModeOnBoth**</span><span class="sxs-lookup"><span data-stu-id="eb372-159">**msidbRemoveFileInstallModeOnBoth**</span></span>    | <span data-ttu-id="eb372-160">0x003</span><span class="sxs-lookup"><span data-stu-id="eb372-160">0x003</span></span>       | <span data-ttu-id="eb372-161">3</span><span class="sxs-lookup"><span data-stu-id="eb372-161">3</span></span>       | <span data-ttu-id="eb372-162">Quítelo en cualquiera de los casos anteriores.</span><span class="sxs-lookup"><span data-stu-id="eb372-162">Remove in either of the above cases.</span></span>                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb372-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb372-163">Remarks</span></span>

<span data-ttu-id="eb372-164">La [acción RemoveFiles](removefiles-action.md)procesa las referencias de archivo en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="eb372-164">The file references in this table are processed by the [RemoveFiles action](removefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="eb372-165">Validación</span><span class="sxs-lookup"><span data-stu-id="eb372-165">Validation</span></span>

<dl>

[<span data-ttu-id="eb372-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="eb372-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="eb372-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="eb372-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="eb372-168">ICE18</span><span class="sxs-lookup"><span data-stu-id="eb372-168">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="eb372-169">ICE32</span><span class="sxs-lookup"><span data-stu-id="eb372-169">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="eb372-170">ICE45</span><span class="sxs-lookup"><span data-stu-id="eb372-170">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="eb372-171">ICE64</span><span class="sxs-lookup"><span data-stu-id="eb372-171">ICE64</span></span>](ice64.md)  
</dl>

 

 



