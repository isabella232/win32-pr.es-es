---
description: La tabla patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabla de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818558"
---
# <a name="patch-table"></a><span data-ttu-id="f4860-103">Tabla de revisión</span><span class="sxs-lookup"><span data-stu-id="f4860-103">Patch Table</span></span>

<span data-ttu-id="f4860-104">La tabla patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="f4860-104">The Patch table specifies the file that is to receive a particular patch and the physical location of the patch files on the media images.</span></span>

<span data-ttu-id="f4860-105">La tabla patch tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f4860-105">The Patch table has the following columns.</span></span>



| <span data-ttu-id="f4860-106">Columna</span><span class="sxs-lookup"><span data-stu-id="f4860-106">Column</span></span>      | <span data-ttu-id="f4860-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4860-107">Type</span></span>                               | <span data-ttu-id="f4860-108">Clave</span><span class="sxs-lookup"><span data-stu-id="f4860-108">Key</span></span> | <span data-ttu-id="f4860-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f4860-109">Nullable</span></span> |
|-------------|------------------------------------|-----|----------|
| <span data-ttu-id="f4860-110">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="f4860-110">File\_</span></span>      | [<span data-ttu-id="f4860-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="f4860-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="f4860-112">Y</span><span class="sxs-lookup"><span data-stu-id="f4860-112">Y</span></span>   | <span data-ttu-id="f4860-113">N</span><span class="sxs-lookup"><span data-stu-id="f4860-113">N</span></span>        |
| <span data-ttu-id="f4860-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="f4860-114">Sequence</span></span>    | [<span data-ttu-id="f4860-115">Entero</span><span class="sxs-lookup"><span data-stu-id="f4860-115">Integer</span></span>](integer.md)             | <span data-ttu-id="f4860-116">Y</span><span class="sxs-lookup"><span data-stu-id="f4860-116">Y</span></span>   | <span data-ttu-id="f4860-117">N</span><span class="sxs-lookup"><span data-stu-id="f4860-117">N</span></span>        |
| <span data-ttu-id="f4860-118">PatchSize</span><span class="sxs-lookup"><span data-stu-id="f4860-118">PatchSize</span></span>   | [<span data-ttu-id="f4860-119">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="f4860-119">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="f4860-120">N</span><span class="sxs-lookup"><span data-stu-id="f4860-120">N</span></span>   | <span data-ttu-id="f4860-121">N</span><span class="sxs-lookup"><span data-stu-id="f4860-121">N</span></span>        |
| <span data-ttu-id="f4860-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4860-122">Attributes</span></span>  | [<span data-ttu-id="f4860-123">Entero</span><span class="sxs-lookup"><span data-stu-id="f4860-123">Integer</span></span>](integer.md)             | <span data-ttu-id="f4860-124">N</span><span class="sxs-lookup"><span data-stu-id="f4860-124">N</span></span>   | <span data-ttu-id="f4860-125">N</span><span class="sxs-lookup"><span data-stu-id="f4860-125">N</span></span>        |
| <span data-ttu-id="f4860-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4860-126">Header</span></span>      | [<span data-ttu-id="f4860-127">Binario</span><span class="sxs-lookup"><span data-stu-id="f4860-127">Binary</span></span>](binary.md)               | <span data-ttu-id="f4860-128">N</span><span class="sxs-lookup"><span data-stu-id="f4860-128">N</span></span>   | <span data-ttu-id="f4860-129">Y</span><span class="sxs-lookup"><span data-stu-id="f4860-129">Y</span></span>        |
| <span data-ttu-id="f4860-130">StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="f4860-130">StreamRef\_</span></span> | [<span data-ttu-id="f4860-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="f4860-131">Identifier</span></span>](identifier.md)       | <span data-ttu-id="f4860-132">N</span><span class="sxs-lookup"><span data-stu-id="f4860-132">N</span></span>   | <span data-ttu-id="f4860-133">Y</span><span class="sxs-lookup"><span data-stu-id="f4860-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f4860-134">Columnas</span><span class="sxs-lookup"><span data-stu-id="f4860-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f4860-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="f4860-135"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f4860-136">La revisión se aplica al archivo especificado por el identificador en esta columna.</span><span class="sxs-lookup"><span data-stu-id="f4860-136">The patch is applied to the file specified by the identifier in this column.</span></span> <span data-ttu-id="f4860-137">Se trata de una clave principal para la tabla y es una clave externa de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4860-137">This is a primary key for the table and it is a foreign key to the [File table](file-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4860-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="f4860-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="f4860-139">Esta es la posición del archivo de revisión en el orden de secuencia de archivos en las imágenes multimedia.</span><span class="sxs-lookup"><span data-stu-id="f4860-139">This is the position of the patch file in the sequence order of files on the media images.</span></span> <span data-ttu-id="f4860-140">El orden de secuencia debe corresponder al orden de los archivos en el archivo contenedor del paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-140">The sequence order must correspond to the order of the files in the patch package cabinet file.</span></span> <span data-ttu-id="f4860-141">Esta es una clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="f4860-141">This is a primary key for this table.</span></span> <span data-ttu-id="f4860-142">El límite máximo es de 32767 archivos, para crear un paquete de Windows Installer con más archivos, consulte crear [un paquete de gran tamaño](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="f4860-142">The maximum limit is 32767 files, to create a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4860-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span><span class="sxs-lookup"><span data-stu-id="f4860-143"><span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize</span></span>
</dt> <dd>

<span data-ttu-id="f4860-144">Esta columna proporciona el tamaño de la revisión en bytes escritos como un entero largo.</span><span class="sxs-lookup"><span data-stu-id="f4860-144">This column gives the size of the patch in bytes written as a long integer.</span></span>

</dd> <dt>

<span data-ttu-id="f4860-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus</span><span class="sxs-lookup"><span data-stu-id="f4860-145"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f4860-146">Entero que contiene los marcadores de bits que representan los atributos de la revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-146">Integer containing bit flags representing patch attributes.</span></span> <span data-ttu-id="f4860-147">Inserte un valor de 1 en esta columna para indicar que no se ha producido un error grave al aplicar esta revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-147">Insert a value of 1 in this column to indicate that the failure to apply this patch is not a fatal error.</span></span>



| <span data-ttu-id="f4860-148">Constante</span><span class="sxs-lookup"><span data-stu-id="f4860-148">Constant</span></span>                         | <span data-ttu-id="f4860-149">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f4860-149">Hexadecimal</span></span> | <span data-ttu-id="f4860-150">Decimal</span><span class="sxs-lookup"><span data-stu-id="f4860-150">Decimal</span></span> | <span data-ttu-id="f4860-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4860-151">Description</span></span>                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| <span data-ttu-id="f4860-152">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="f4860-152">(none)</span></span>                           | <span data-ttu-id="f4860-153">0x000</span><span class="sxs-lookup"><span data-stu-id="f4860-153">0x000</span></span>       | <span data-ttu-id="f4860-154">0</span><span class="sxs-lookup"><span data-stu-id="f4860-154">0</span></span>       | <span data-ttu-id="f4860-155">Un error grave no se pudo aplicar a esta revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-155">Failure to apply this patch is a fatal error.</span></span>                        |
| <span data-ttu-id="f4860-156">**msidbPatchAttributesNonVital**</span><span class="sxs-lookup"><span data-stu-id="f4860-156">**msidbPatchAttributesNonVital**</span></span> | <span data-ttu-id="f4860-157">0x001</span><span class="sxs-lookup"><span data-stu-id="f4860-157">0x001</span></span>       | <span data-ttu-id="f4860-158">1</span><span class="sxs-lookup"><span data-stu-id="f4860-158">1</span></span>       | <span data-ttu-id="f4860-159">Indica que no se ha producido un error grave al aplicar esta revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-159">Indicates that the failure to apply this patch is not a fatal error.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f4860-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4860-160"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="f4860-161">Esta columna es el encabezado de revisión de la secuencia binaria que se utiliza para la validación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="f4860-161">This column is the binary stream patch header used for patch validation.</span></span> <span data-ttu-id="f4860-162">Esta columna debe ser null si la \_ columna StreamRef no es NULL.</span><span class="sxs-lookup"><span data-stu-id="f4860-162">This column should be null if the StreamRef\_ column is not null.</span></span> <span data-ttu-id="f4860-163">En este caso, la secuencia de encabezado Patch se almacena en la [tabla MsiPatchHeaders](msipatchheaders-table.md) para superar la limitación de nombre de flujo descrita en [limitaciones OLE en las secuencias](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="f4860-163">In this case, the patch header stream is stored in the [MsiPatchHeaders table](msipatchheaders-table.md) to overcome the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4860-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span><span class="sxs-lookup"><span data-stu-id="f4860-164"><span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_</span></span>
</dt> <dd>

<span data-ttu-id="f4860-165">Clave externa en la tabla MsiPatchHeaders que especifica la fila que contiene la secuencia de encabezado patch.</span><span class="sxs-lookup"><span data-stu-id="f4860-165">External key into the MsiPatchHeaders table specifying the row that contains the patch header stream.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4860-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4860-166">Remarks</span></span>

<span data-ttu-id="f4860-167">La [acción PatchFiles](patchfiles-action.md)procesa esta tabla.</span><span class="sxs-lookup"><span data-stu-id="f4860-167">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="f4860-168">Normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="f4860-168">It is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="f4860-169">Normalmente no se crea directamente en un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="f4860-169">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="f4860-170">Validación</span><span class="sxs-lookup"><span data-stu-id="f4860-170">Validation</span></span>

<dl>

[<span data-ttu-id="f4860-171">ICE03</span><span class="sxs-lookup"><span data-stu-id="f4860-171">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f4860-172">ICE06</span><span class="sxs-lookup"><span data-stu-id="f4860-172">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f4860-173">ICE29</span><span class="sxs-lookup"><span data-stu-id="f4860-173">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="f4860-174">ICE45</span><span class="sxs-lookup"><span data-stu-id="f4860-174">ICE45</span></span>](ice45.md)  
</dl>

 

 



