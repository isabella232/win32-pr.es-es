---
description: Esta tabla contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado a un directorio de destino especificado.
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: Tabla MoveFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818579"
---
# <a name="movefile-table"></a><span data-ttu-id="7a670-103">Tabla MoveFile</span><span class="sxs-lookup"><span data-stu-id="7a670-103">MoveFile Table</span></span>

<span data-ttu-id="7a670-104">Esta tabla contiene una lista de archivos que se mueven o copian desde un directorio de origen especificado a un directorio de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="7a670-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="7a670-105">La tabla MoveFile tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7a670-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="7a670-106">Columna</span><span class="sxs-lookup"><span data-stu-id="7a670-106">Column</span></span>       | <span data-ttu-id="7a670-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a670-107">Type</span></span>                         | <span data-ttu-id="7a670-108">Clave</span><span class="sxs-lookup"><span data-stu-id="7a670-108">Key</span></span> | <span data-ttu-id="7a670-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="7a670-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="7a670-110">FileKey</span><span class="sxs-lookup"><span data-stu-id="7a670-110">FileKey</span></span>      | [<span data-ttu-id="7a670-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a670-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a670-112">Y</span><span class="sxs-lookup"><span data-stu-id="7a670-112">Y</span></span>   | <span data-ttu-id="7a670-113">N</span><span class="sxs-lookup"><span data-stu-id="7a670-113">N</span></span>        |
| <span data-ttu-id="7a670-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7a670-114">Component\_</span></span>  | [<span data-ttu-id="7a670-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a670-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a670-116">N</span><span class="sxs-lookup"><span data-stu-id="7a670-116">N</span></span>   | <span data-ttu-id="7a670-117">N</span><span class="sxs-lookup"><span data-stu-id="7a670-117">N</span></span>        |
| <span data-ttu-id="7a670-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="7a670-118">SourceName</span></span>   | [<span data-ttu-id="7a670-119">Texto</span><span class="sxs-lookup"><span data-stu-id="7a670-119">Text</span></span>](text.md)             | <span data-ttu-id="7a670-120">N</span><span class="sxs-lookup"><span data-stu-id="7a670-120">N</span></span>   | <span data-ttu-id="7a670-121">Y</span><span class="sxs-lookup"><span data-stu-id="7a670-121">Y</span></span>        |
| <span data-ttu-id="7a670-122">DestName</span><span class="sxs-lookup"><span data-stu-id="7a670-122">DestName</span></span>     | [<span data-ttu-id="7a670-123">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="7a670-123">Filename</span></span>](filename.md)     | <span data-ttu-id="7a670-124">N</span><span class="sxs-lookup"><span data-stu-id="7a670-124">N</span></span>   | <span data-ttu-id="7a670-125">Y</span><span class="sxs-lookup"><span data-stu-id="7a670-125">Y</span></span>        |
| <span data-ttu-id="7a670-126">Carpetadeorigen</span><span class="sxs-lookup"><span data-stu-id="7a670-126">SourceFolder</span></span> | [<span data-ttu-id="7a670-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a670-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a670-128">N</span><span class="sxs-lookup"><span data-stu-id="7a670-128">N</span></span>   | <span data-ttu-id="7a670-129">Y</span><span class="sxs-lookup"><span data-stu-id="7a670-129">Y</span></span>        |
| <span data-ttu-id="7a670-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="7a670-130">DestFolder</span></span>   | [<span data-ttu-id="7a670-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a670-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a670-132">N</span><span class="sxs-lookup"><span data-stu-id="7a670-132">N</span></span>   | <span data-ttu-id="7a670-133">N</span><span class="sxs-lookup"><span data-stu-id="7a670-133">N</span></span>        |
| <span data-ttu-id="7a670-134">Opciones</span><span class="sxs-lookup"><span data-stu-id="7a670-134">Options</span></span>      | [<span data-ttu-id="7a670-135">Entero</span><span class="sxs-lookup"><span data-stu-id="7a670-135">Integer</span></span>](integer.md)       | <span data-ttu-id="7a670-136">N</span><span class="sxs-lookup"><span data-stu-id="7a670-136">N</span></span>   | <span data-ttu-id="7a670-137">N</span><span class="sxs-lookup"><span data-stu-id="7a670-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7a670-138">Columnas</span><span class="sxs-lookup"><span data-stu-id="7a670-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7a670-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="7a670-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="7a670-140">Clave principal que identifica de forma única un registro MoveFile determinado.</span><span class="sxs-lookup"><span data-stu-id="7a670-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="7a670-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="7a670-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="7a670-142">Clave externa en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a670-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="7a670-143">Si el componente al que hace referencia esta clave no está seleccionado para la instalación o la eliminación, no se realiza ninguna acción en esta entrada MoveFile.</span><span class="sxs-lookup"><span data-stu-id="7a670-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="7a670-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="7a670-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="7a670-145">Esta columna contiene el nombre traducible de los archivos de origen que se van a copiar o copiar.</span><span class="sxs-lookup"><span data-stu-id="7a670-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="7a670-146">Esta columna puede dejarse en blanco.</span><span class="sxs-lookup"><span data-stu-id="7a670-146">This column may be left blank.</span></span> <span data-ttu-id="7a670-147">Vea la descripción de la columna Carpetadeorigen.</span><span class="sxs-lookup"><span data-stu-id="7a670-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="7a670-148">Este campo debe contener un nombre de archivo largo y puede contener caracteres comodín ( \* y?).</span><span class="sxs-lookup"><span data-stu-id="7a670-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="7a670-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="7a670-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="7a670-150">Esta columna contiene el nombre traducible que se va a asignar al archivo original una vez que se ha copiado o copiado.</span><span class="sxs-lookup"><span data-stu-id="7a670-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="7a670-151">Si este campo está en blanco, el archivo de destino recibe el mismo nombre que el archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="7a670-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="7a670-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>Carpetadeorigen</span><span class="sxs-lookup"><span data-stu-id="7a670-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="7a670-153">Esta columna contiene el nombre de una propiedad que tiene un valor que se resuelve en la ruta de acceso completa al directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="7a670-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="7a670-154">Si la columna SourceName se deja en blanco, se supone que la propiedad denominada en la columna Carpetadeorigen contiene la ruta de acceso completa al archivo de código fuente (incluido el nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="7a670-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="7a670-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="7a670-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="7a670-156">Nombre de una propiedad cuyo valor se resuelve en la ruta de acceso completa al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="7a670-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="7a670-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opciones</span><span class="sxs-lookup"><span data-stu-id="7a670-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="7a670-158">Valor entero que especifica el modo de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="7a670-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="7a670-159">Constante</span><span class="sxs-lookup"><span data-stu-id="7a670-159">Constant</span></span>                     | <span data-ttu-id="7a670-160">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7a670-160">Hexadecimal</span></span> | <span data-ttu-id="7a670-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a670-161">Decimal</span></span> | <span data-ttu-id="7a670-162">Significado</span><span class="sxs-lookup"><span data-stu-id="7a670-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="7a670-163">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="7a670-163">(none)</span></span>                       | <span data-ttu-id="7a670-164">0x000</span><span class="sxs-lookup"><span data-stu-id="7a670-164">0x000</span></span>       | <span data-ttu-id="7a670-165">0</span><span class="sxs-lookup"><span data-stu-id="7a670-165">0</span></span>       | <span data-ttu-id="7a670-166">Copie el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="7a670-166">Copy the source file.</span></span> |
| <span data-ttu-id="7a670-167">**msidbMoveFileOptionsMove**</span><span class="sxs-lookup"><span data-stu-id="7a670-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="7a670-168">0x001</span><span class="sxs-lookup"><span data-stu-id="7a670-168">0x001</span></span>       | <span data-ttu-id="7a670-169">1</span><span class="sxs-lookup"><span data-stu-id="7a670-169">1</span></span>       | <span data-ttu-id="7a670-170">Mueva el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="7a670-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a670-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a670-171">Remarks</span></span>

<span data-ttu-id="7a670-172">Si \* se escribe un carácter comodín "" en la columna SourceName de la tabla MoveFile y se especifica un nombre de archivo de destino en la columna DestName, todos los archivos que se han copiado o copiado conservan los nombres en los orígenes.</span><span class="sxs-lookup"><span data-stu-id="7a670-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="7a670-173">La [acción MoveFiles](movefiles-action.md)procesa esta tabla.</span><span class="sxs-lookup"><span data-stu-id="7a670-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7a670-174">Validación</span><span class="sxs-lookup"><span data-stu-id="7a670-174">Validation</span></span>

<dl>

[<span data-ttu-id="7a670-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="7a670-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7a670-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="7a670-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7a670-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="7a670-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="7a670-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="7a670-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7a670-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="7a670-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="7a670-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="7a670-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



