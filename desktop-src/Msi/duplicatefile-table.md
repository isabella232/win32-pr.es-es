---
description: La tabla DuplicateFile contiene una lista de archivos que se van a duplicar, ya sea en un directorio diferente al del archivo original o en el mismo directorio, pero con un nombre diferente. El archivo original debe ser un archivo instalado por la acción InstallFiles.
ms.assetid: 7fe1b52d-4b06-48cd-afe5-2bd5495bb55e
title: Tabla DuplicateFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 766f28b7984aedfc682a2bf23378d46ee0519c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082783"
---
# <a name="duplicatefile-table"></a><span data-ttu-id="5ba6f-104">Tabla DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="5ba6f-104">DuplicateFile Table</span></span>

<span data-ttu-id="5ba6f-105">La tabla DuplicateFile contiene una lista de archivos que se van a duplicar, ya sea en un directorio diferente al del archivo original o en el mismo directorio, pero con un nombre diferente.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-105">The DuplicateFile table contains a list of files that are to be duplicated, either to a different directory than the original file or to the same directory but with a different name.</span></span> <span data-ttu-id="5ba6f-106">El archivo original debe ser un archivo instalado por la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="5ba6f-106">The original file must be a file installed by the [InstallFiles action](installfiles-action.md).</span></span>

<span data-ttu-id="5ba6f-107">La tabla DuplicateFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-107">The DuplicateFile table has the following columns.</span></span>



| <span data-ttu-id="5ba6f-108">Columna</span><span class="sxs-lookup"><span data-stu-id="5ba6f-108">Column</span></span>      | <span data-ttu-id="5ba6f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ba6f-109">Type</span></span>                         | <span data-ttu-id="5ba6f-110">Clave</span><span class="sxs-lookup"><span data-stu-id="5ba6f-110">Key</span></span> | <span data-ttu-id="5ba6f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5ba6f-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="5ba6f-112">FileKey</span><span class="sxs-lookup"><span data-stu-id="5ba6f-112">FileKey</span></span>     | [<span data-ttu-id="5ba6f-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="5ba6f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ba6f-114">Y</span><span class="sxs-lookup"><span data-stu-id="5ba6f-114">Y</span></span>   | <span data-ttu-id="5ba6f-115">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-115">N</span></span>        |
| <span data-ttu-id="5ba6f-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5ba6f-116">Component\_</span></span> | [<span data-ttu-id="5ba6f-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="5ba6f-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ba6f-118">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-118">N</span></span>   | <span data-ttu-id="5ba6f-119">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-119">N</span></span>        |
| <span data-ttu-id="5ba6f-120">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="5ba6f-120">File\_</span></span>      | [<span data-ttu-id="5ba6f-121">Identificador</span><span class="sxs-lookup"><span data-stu-id="5ba6f-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ba6f-122">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-122">N</span></span>   | <span data-ttu-id="5ba6f-123">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-123">N</span></span>        |
| <span data-ttu-id="5ba6f-124">DestName</span><span class="sxs-lookup"><span data-stu-id="5ba6f-124">DestName</span></span>    | [<span data-ttu-id="5ba6f-125">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="5ba6f-125">Filename</span></span>](filename.md)     | <span data-ttu-id="5ba6f-126">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-126">N</span></span>   | <span data-ttu-id="5ba6f-127">Y</span><span class="sxs-lookup"><span data-stu-id="5ba6f-127">Y</span></span>        |
| <span data-ttu-id="5ba6f-128">DestFolder</span><span class="sxs-lookup"><span data-stu-id="5ba6f-128">DestFolder</span></span>  | [<span data-ttu-id="5ba6f-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="5ba6f-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="5ba6f-130">N</span><span class="sxs-lookup"><span data-stu-id="5ba6f-130">N</span></span>   | <span data-ttu-id="5ba6f-131">Y</span><span class="sxs-lookup"><span data-stu-id="5ba6f-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5ba6f-132">Columnas</span><span class="sxs-lookup"><span data-stu-id="5ba6f-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5ba6f-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="5ba6f-133"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="5ba6f-134">Una clave principal, un token no localizado, que identifica un registro DuplicateFile único.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-134">A primary key, a non-localized token, identifying a unique DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="5ba6f-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="5ba6f-135"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="5ba6f-136">Una clave externa a la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ba6f-136">An external key to the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="5ba6f-137">Si el componente identificado por la clave no está seleccionado para la instalación o la eliminación, no se realiza ninguna acción en este registro DuplicateFile.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-137">If the component identified by the key is not selected for installation or removal, then no action is taken on this DuplicateFile record.</span></span>

</dd> <dt>

<span data-ttu-id="5ba6f-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="5ba6f-138"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="5ba6f-139">Clave externa en la [tabla de archivos](file-table.md) que representa el archivo original que se va a duplicar.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-139">Foreign key into the [File table](file-table.md) representing the original file that is to be duplicated.</span></span>

</dd> <dt>

<span data-ttu-id="5ba6f-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="5ba6f-140"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="5ba6f-141">Nombre traducible que se va a asignar al archivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-141">Localizable name to be given to the duplicate file.</span></span> <span data-ttu-id="5ba6f-142">Si este campo está en blanco, el archivo de destino recibe el mismo nombre que el archivo original.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-142">If this field is blank, then the destination file is given the same name as the original file.</span></span>

</dd> <dt>

<span data-ttu-id="5ba6f-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="5ba6f-143"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="5ba6f-144">Nombre de una propiedad que es la ruta de acceso completa a la que se va a copiar el archivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-144">Name of a property that is the full path to where the duplicate file is to be copied.</span></span> <span data-ttu-id="5ba6f-145">Si este directorio es el mismo que el directorio que contiene el archivo original y el nombre del archivo duplicado propuesto es el mismo que el original, no se realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="5ba6f-145">If this directory is the same as the directory containing the original file and the name for the proposed duplicate file is the same as the original, then no action takes place.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ba6f-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ba6f-146">Remarks</span></span>

<span data-ttu-id="5ba6f-147">La tabla se procesa mediante la [acción DuplicateFiles](duplicatefiles-action.md) y la [acción RemoveDuplicateFiles](removeduplicatefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="5ba6f-147">The table is processed by the [DuplicateFiles action](duplicatefiles-action.md) and the [RemoveDuplicateFiles action](removeduplicatefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="5ba6f-148">Validación</span><span class="sxs-lookup"><span data-stu-id="5ba6f-148">Validation</span></span>

<dl>

[<span data-ttu-id="5ba6f-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="5ba6f-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5ba6f-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="5ba6f-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5ba6f-151">ICE18</span><span class="sxs-lookup"><span data-stu-id="5ba6f-151">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="5ba6f-152">ICE32</span><span class="sxs-lookup"><span data-stu-id="5ba6f-152">ICE32</span></span>](ice32.md)  
</dl>

 

 



